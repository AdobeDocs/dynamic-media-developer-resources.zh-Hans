---
description: 影像轉換公用程式。
solution: Experience Manager
title: ic
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 2%

---

# ic {#ic}

影像轉換公用程式。

`ic` 是一個命令列工具，可將影像檔案轉換為最佳化的金字塔TIFF格式(PTIFF)。 雖然「影像伺服」可以處理影像而不轉換，但建議您將所有大於512x512畫素的影像轉換為PTIFF。 此轉換可確保最佳伺服器效能和資源使用率，並將回應時間縮到最短。

建議包含像片內容的PTIFF檔案使用JPEG編碼(指定 `-jpegcompress`)。 電腦產生的內容可以受益於無失真壓縮（以下兩種方式之一） `-deflatecompress` 或 `-lzwcompress`)。 除非需要進行色彩轉換或畫素型別轉換，否則會將JPEG來源影像資料傳輸至PTIFF而不進行解碼，以避免品質降低。 在此情況下，指定的壓縮選項只會套用至解析度較低的金字塔層次。

如果您不轉換大型影像，您就不需要設定控制要使用多少記憶體的引數。 不過，如果您確實如此，請 `ic` 使用 `-maxmem` 設定如下所述。 計算所需記憶體量的經驗法則是將影像寬度乘以影像高度，再乘以色版數量。 例如，Alpha乘以3的RGB影像為4。 此外，如果通道是每個元件16位元，而不是8位元，則會使最終結果加倍。

## 使用 {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>選項</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>命令選項（請參閱下文）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>來源檔案</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>單一輸入影像檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>單一輸出PTIFF檔案（如果與SourceDirectory一起使用則無效）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>包含輸入影像的資料夾。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>將輸出PTIFF檔案寫入其中的資料夾。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-36a2dcfa39824d29b69547c432366219}

如果成功，則為0。 如果發生錯誤，則會傳回非零值，並將錯誤詳細資料傳送至 `stderr`.

## 选项 {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -未压缩的 </span> </p> </td> 
   <td colname="col2"> <p>請勿壓縮輸出影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>使用deflate (zip)壓縮（預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>使用Lempel-Ziv-Welch (LZW)壓縮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>使用JPEG編碼。 忽略條件 <span class="codeph"> <span class="varname"> 來源檔案 </span> </span> 包含alpha資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> 品質 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>JPEG品質（0-100；預設為95）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">  — 完整範例許可權 </span> </p> </td> 
   <td colname="col2"> <p>停用JPEG色度縮減取樣（可以改善色彩文字和圖形的品質）。 這對CMYK或灰階的輸出影像沒有影響。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> 金額 </span>&gt; &lt; <span class="varname"> 半徑 </span>&gt; &lt; <span class="varname"> 臨界值 </span>&gt; &lt; <span class="varname"> 單色 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>將遮色片銳利化調整套用至取樣不足的金字塔色階。 另請參閱 <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> 以取得詳細資訊。 （未套用至完整解析度的影像。） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>使用來源檔案中的剪裁路徑（如果有的話）來建立關聯的Alpha資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>列印解析度(dpi) <span class="codeph"> <span class="varname"> destFile </span> </span>；若未指定，則列印解析度為 <span class="codeph"> srcFile </span> 已複製到 <span class="codeph"> <span class="varname"> destFile </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop &lt; <span class="varname"> 轉角 </span>&gt; &lt; <span class="varname"> 模式 </span>&gt; &lt; <span class="varname"> 容許度 </span>&gt; &lt; <span class="varname"> infoFile </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>計算裁切矩形以將純色背景最小化。 如果自動裁切演演算法會導致整個影像被裁切，則不會輸出裁切資訊。 </p> <p>若要計算裁切矩形而不轉換影像，請指定 <span class="codeph"> -autocrop </span> 不含 <span class="codeph"> -convert </span> 和沒有 <span class="codeph"> <span class="varname"> destFile。</span> </span></p>

<p><i><b>轉角</b></i> - ul | ur | ll | lr </p>
   <p> 指定要使用種子點的影像轉角。 如果模式為1，則忽略。</p>
   <p><i><b>模式</b></i> - 0 | 1</p>
   <p>設定為0可根據指定角點畫素的顏色裁切；如果Alpha資料與來源影像相關聯，則適用於預乘顏色資料。</p>
   <p>設定為1可根據Alpha資料裁切；會忽略轉角，且0一律為種子值；如果沒有Alpha資料與來源影像相關聯，則不會套用裁切。</p> 
   <p><i><b>容許度</b></i>  — 相符公差。 從0.0到1.0的實數值。指定符合畫素元件值的公差。 若完全相符，則設為0。</p>
   <p><i><b>infoFile</b></i>  — 寫入裁切資訊資料的XML輸出檔案的路徑和名稱。</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>複製XMP中繼資料（如果有的話）來源 <span class="codeph"> <span class="varname"> 來源檔案 </span> </span> 至 <span class="codeph"> <span class="varname"> destFile </span> </span> 而不修改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> 將ICC色彩設定檔內嵌於 <span class="codeph"> <span class="varname"> destFile </span> </span>，若有的話（預設不會嵌入任何設定檔）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> 檔案 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICC設定檔的路徑和名稱。 定義色彩空間 <span class="codeph"> <span class="varname"> 來源檔案 </span> </span> 和必須與其畫素型別相符。 只有在未內嵌設定檔時，才應指定 <span class="codeph"> <span class="varname"> 來源檔案 </span> </span>，因為這會覆寫內嵌設定檔。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> 檔案 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICC設定檔的路徑和名稱。 定義畫素型別和色域 <span class="codeph"> <span class="varname"> destFile </span> </span>. IC會轉換成此設定檔，如果 <span class="codeph"> <span class="varname"> 來源檔案 </span> </span> 具有內嵌設定檔，或者 <span class="codeph"> -imageprofile </span> 也會指定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual </span> </p> </td> 
   <td colname="col2"> <p>色彩空間轉換的感應式演算色彩比對方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric </span> </p> </td> 
   <td colname="col2"> <p> 色彩空間轉換的相對色彩演算比對方式（預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric </span> </p> </td> 
   <td colname="col2"> <p>色彩空間轉換的絕對色彩比對方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>色彩空間轉換的飽和度演算色彩比對方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>停用特定色彩轉換的黑點補償 </p> <p>默认启动. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>色彩轉換時停用遞色（錯誤擴散）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> 停用從CMYK到RGB的自動轉換。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>強制對JPEG輸入影像進行解碼和重新編碼。 </p> <p> <b>注意：</b> 套用此選項可能會降低影像品質。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>使用標準品質（雙線性）重新取樣濾鏡。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>使用較高品質（Lanczos視窗）重新取樣濾鏡（預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>使用更高品質(FlashPix)重新取樣濾鏡。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>使用Photoshop樣式的8x8雙立方銳利化濾鏡縮減取樣。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage </span> </p> </td> 
   <td colname="col2"> <p> 當指定為第一個選項時，遇到無效選項時會隱藏使用狀況資訊的輸出。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -覆盖 </span> </p> </td> 
   <td colname="col2"> <p>允許覆寫現有的 <span class="codeph"> <span class="varname"> destFile </span> </span>. 依預設，會在檔案名稱后面附加數值尾碼，以防止覆寫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden </span> </p> </td> 
   <td colname="col2"> <p>忽略隱藏的來源檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror </span> </p> </td> 
   <td colname="col2"> <p>發生錯誤時，請勿停止處理。 只有在處理多個檔案時才有效。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt; <span class="varname"> 檔案 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>記錄檔的路徑和名稱(預設為 <span class="codeph"> stdout </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> level </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>記錄層級。 </p> 
   <p>&lt; 0 — 停用記錄。</p>
   <p>0 — 列出要處理的檔案。</p>
   <p>1 — 為不需要的檔案新增報告。</p>
   <p>2 — 新增進度報告。</p>
   <p>3 — 新增每個檔案的報告。</p>
   <p>4 — 在檔案層級新增進度報告。</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>附加至記錄檔（預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>覆寫記錄檔。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec &lt; <span class="varname"> 毫秒 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>記錄層級2和更高層級的記錄間隔（以毫秒為單位） （預設值為3000）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname"> 位元組 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>記憶體使用量限制。 至少必須是10 MB。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> 百分比 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>記憶體使用量限制。 預設為實體記憶體的25%。 如果兩者都不 <span class="codeph"> 最大 </span> 也不 <span class="codeph"> maxmempercent </span> 明確設定時使用maxmempercent預設值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -版本 </span> </p> </td> 
   <td colname="col2"> <p> 傳回此公用程式的版本資訊。 指定而不使用其他選項。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 支援的輸入影像格式 {#section-ab13d941d6724e65b9f84b62d949d31c}

下表列出IC支援的影像檔案格式和格式選項。

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> 格式</b> </p> </th> 
   <th class="entry"> <p> <b> 畫素型別</b> <b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> 压缩</b> </p> </th> 
   <th class="entry"> <p> <b> 说明</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> （Windows點陣圖） </p> </td> 
   <td> <p> RGB |已索引 </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> 未壓縮 | RLE </p> </td> 
   <td> <p> 5/6位元/通道表示支援16位元RGB（5-5-5和5-6-5位元/通道）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> （封裝的Postscript） </p> </td> 
   <td> <p> CMYK |RGB |灰色 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 |二進位 |JPEG </p> </td> 
   <td> <p> 僅支援Photoshop產生的EPS檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> <p> CompuServe </p> <b>GIF</b> </td> 
   <td> <p> 已索引 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> 如果存在，調色盤中的透明度值會轉換為Alpha。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK |RGB |灰色 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK |奇姆卡 |RGB | RGBA |灰色 | grayA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 未壓縮 |已壓縮 </p> </td> 
   <td> <p> 僅限合併的影像；會忽略圖層和額外的色版。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> 僅限點陣圖資料；會忽略向量資料。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA |灰色 | grayA |已索引 </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> 压缩的 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK |奇姆卡 |RGB | RGBA |灰色 | grayA |已索引 </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 未壓縮 | ZIP | LZW |JPEG |核心規則 |中信泰富G3 |中信泰富G4 | Packbits </p> </td> 
   <td> <p> 除了第一個關聯的Alpha色版以外，會忽略額外的色版。 </p> </td> 
  </tr> 
 </tbody> 
</table>

內嵌ICC設定檔可在EPS、JPG、PSD、PNG和TIFF檔案中辨識。

EPS、JPG、PSD和TIFF檔案可辨識內嵌路徑和XMP中繼資料。

## 示例 {#section-3c1986b30315431989bd76b1ee5bef6d}

以最佳品質轉換單一影像，並將其儲存在相同的資料夾中：

`ic -convert src/myFile.png src/myFile.tif`

轉換所有影像 *`srcFolder`* JPEG編碼的金字塔TIFF並置於 *`destFolder`*：

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

轉換所有影像 *`srcFolder`*. JPG檔案的編碼影像資料用於完整解析度層級、無遺失的LZW壓縮，用於這些影像的影像金字塔的其餘部分，以及所有非JPG輸入檔案的整個輸出影像。 畫素型別、內嵌色彩設定檔、XMP中繼資料等。 會進行維護。

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
