---
description: textPs=实施了一种专有的复制拟合算法，该算法将自动调整字体大小以使用文本以最佳方式填充文本区域，在避免溢出的同时最大限度地减少底部的额外空间。
solution: Experience Manager
title: 复制拟合
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# 复制拟合{#copy-fitting}

textPs=实施了一种专有的复制拟合算法，该算法将自动调整字体大小以使用文本以最佳方式填充文本区域，在避免溢出的同时最大限度地减少底部的额外空间。

可以基于段落为整个文本层集体启用和控制复制拟合，甚至对于单个文本范围也是如此。

指定最小字体大小 `\fs` 以及 `\copyfit`. 同一RTF字符串中允许任意数量的范围。 所有范围的大小都会按比例变化，从而确保保持所需的字体大小比。

`\copyfit` 被视为字符格式命令，并具有 `\fs` 和 `\b`.

通过指定 `\copyfit` ，其大小等于或小于 `\fs`.

## 限制行数 {#section-e5aee0f039e04842afc3d6884ed681ac}

除了指定字体大小的范围外，还可以通过 `\copyfitlines` 或 `\copyfitmaxlines` 命令，以限制算法将生成的行数。 两个命令都接受行计数参数或0，以不限制复制拟合区域中的行数。

`\copyfitlines` 当文本不适合指定的行数时，允许文本溢出到其他行。 始终遵循要复制的文本区段中的显式换行符。

`\copyfitmaxlines` 始终截断超出指定限制的额外输出行。 即使存在明确的换行符，也永远不会超出指定的行数。 对于此版本的图像提供，不超过N-1 `\line` 标记可以存在于已复制的文本范围中。 如果超出此限制，则未定义行为。

## 示例 {#section-f4ddbbfade444560be30a813d90c2c1b}

以下示例假定文本正文中提供了名为 *[!DNL $A$]*, *[!DNL $B$]*&#x200B;和 *[!DNL $C$]*.

**在整个范围内保持字体大小之间的相同比率：**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* 将始终呈现为文本其余部分的两倍大。 指定了大量文本后， *[!DNL $A$]* 和 *[!DNL $C$]* 呈现为 `\fs10` 和 *[!DNL $B$]* with `\fs20`. 有些文字， *[!DNL $A$]* 和 *[!DNL $C$]* 将使用 `\fs100` 和 *[!DNL $B$]* `\fs200`.

**如果只绘制了少量文本，则会收敛到通用的大字体大小：**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

在范围的最小端， *[!DNL $B$]* 呈现为 `\fs20`，是的两倍 *[!DNL $A$]* 和 *[!DNL $C$]* at `\fs10`. 所有文本都在 `\fs100` （50点）。

**如果要渲染大量文本，则会收敛到通用的小字体大小：**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

所有文本在范围的小端使用\fs10绘制，而在最大端使用\fs10绘制， *[!DNL $A$]* 和 *[!DNL $C$]* 呈现为 `\fs100` 和 *[!DNL $B$]* with `\fs200`.

**禁用内文本范围的复制拟合：**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

的字体大小 *[!DNL $A$]* 和 *[!DNL $C$]* 可能介于10到100之间，而 *[!DNL $B$]* 始终通过 `\fs50`.

**将输出限制为单行，即使有更多的垂直空间，但如果指定的文本过多以适合位于 `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**将输出限制为单行，即使有更多垂直空间也是如此。 如果指定的文本过多，以致于无法放入 `\fs10` 它被截断：**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
