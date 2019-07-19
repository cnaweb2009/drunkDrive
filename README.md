# 中央通訊社[〈治酒駕用重典？49萬筆判決書的罪與罰〉](https://cna.com.tw/20190719-drunkdriving/index.html)專題

#### 最後更新時間：2019/7/18

## 數據抓取及篩選

- 應撈判決約59萬筆：自[司法院判決書網站](https://law.judicial.gov.tw/FJUD/default.aspx)蒐集全國22個地方法院，自2000年至2019年1月所有可能的酒駕刑事判決；以判決書全文出現「酒精」二字，作為最初的蒐集標準。
- 初篩資料約51萬筆：由於資料包含許多雜訊，未必精準指涉酒駕事件。如因偵測到「酒精燈」、「酒精濃度測試單」而撈入，或是當事人酒後傷害他人等。我們透過相關字詞的排列組合，篩選出真正的「酒駕」案件。相關字詞包括「刑法第185條之3」、「不能安全駕駛」、「吐氣所含酒精濃度達每公升零點二五毫克以上」、「服用酒類」等。
- 一般酒駕案件約48.8萬筆：除了上述確保為酒駕的關鍵字組合外，我們還排除主文含「死、傷」字眼的判決，「處」字出現次數也不能超過2次，希望讓這部分留下單純的「不能安全駕駛」案件。
- 酒駕致死案件約2800筆：除了套用酒駕關鍵字組合外，我們也以「致人於死」作為篩選依據，辨識出約2800筆。值得注意的是，歷次修法會影響案件主文寫法，例如從「過失致人於死」變為「不能安全駕駛動力交通工具而駕駛，因而致人於死」；若單純以「過失致人於死」為篩選依據，可能就會有缺漏。
- 酒駕致傷案件約5200筆：我們以主文出現「過失傷害」作為篩選依據。

## 擬定問題，將判決書結構化

進行分析之前，我們以人工檢視判決書特性，找出可分析的欄位，再將文字資料結構化。

接著拆分出判決日期、所屬地院、是否累犯、是否易科罰金、不能安全駕駛刑度、不能安全駕駛罰金值、酒駕致死刑度、酒駕過失傷害刑度、是否緩刑、教育程度、車種、酒精濃度等欄位。

## 反覆清洗，進行探索式資料分析

要將文字化為可分析的欄位並非一次到位，而是反覆經歷資料的探索，慢慢收斂出合適的製作方向，和精準的清洗規則。

清洗過程中的挑戰包括：將複雜的罪刑結構化。例如酒駕除了不能安全駕駛罪外，許多案件還可能牽涉過失致死、過失傷害、偽造文書、肇事逃逸、妨害公務等罪，最終也有一「合併執行」刑度；本專題以單一罪名之刑度為分析依據。

此外，各地院判決書寫法各異，文字、數字、甚至符號寫法多元，例如「一」與「壹」之分、數字的全半形差異，都是資料清洗的挑戰。

*有關數據清洗程式碼，可見[negligent.ipynb](https://github.com/cnaweb2009/drunkDrive/blob/master/negligent.ipynb)。*

## 限制

以下為本專題研究方法可能的限制：

- 資料集為地院刑事判決書，不包括上訴、地檢署緩起訴及酒駕自撞身亡案件。近年「緩起訴」處分約占地檢署酒駕案件四分之一。
- 判決書撈取過程，資料可能有遺漏或重複。
- 透過關鍵字組合，篩選一般酒駕、致死、致傷資料集，仍可能有所遺漏。
- 部分判決書文字出現亂碼，無法精準辨識。
- 判決書寫法差異大，各欄位未必能完全精準辨識。
- 【判決書數量】案件多寡未必等同於嚴重度，需考量人為因素。例如第一線攔檢頻率、案件到地院時是否給予緩起訴，都是可能影響因子。
- 【地區】分析是以地院為單位，台北、基隆、新北、士林、高雄、橋頭地院之轄區和實際行政區劃有別。又板橋地院2013年改制為新北地院，橋頭地院於2016年9月成立，分擔高雄地區業務量。
- 【濃度】未具體寫明酒精濃度者，以判決書提到之最低門檻為準。
- 【刑度】分析是以單一罪名的宣告刑為依據，然實際上當事人可能以易科罰金方式執行；當事人亦可能觸犯其他罪，而有合併執行刑度。
- 【公訴不受理】過失傷害罪屬於告訴乃論，若主文寫到該部分公訴不受理，當庭和解是可能原因之一，而非唯一。

## Open Data

司法院判決書經中央社數據處理的版本如下表所示。
*資料清理過程並非完美，可能仍有雜訊或不符的資料，使用或詮釋上請務必留意。*

| 一般酒駕 | 酒駕致死 | 酒駕致傷 |
| :----: | :----: |:----: |
|  [2000](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2000.csv) [2001](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2001.csv)| bbbbbb | ccccc |

### 一般酒駕案件
- [2000](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2000.csv)
- [2001](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2001.csv)
- [2002](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2002.csv)
- [2003](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2003.csv)
- [2004](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2004.csv)
- [2005](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2005.csv)
- [2006](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2006.csv)
- [2007](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2007.csv)
- [2008](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2008.csv)
- [2009](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2009.csv)
- [2010](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2010.csv)
- [2011](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2011.csv)
- [2012](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2012.csv)
- [2013](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2013.csv)
- [2014](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2014.csv)
- [2015](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2015.csv)
- [2016](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2016.csv)
- [2017](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2017.csv)
- [2018](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2018.csv)
- [2019(僅至1月)](https://www.cna.com.tw/project/drunkdrivingDownload/drunkDrive_2019.csv)

### 酒駕致死案件
- [2000-201901](https://www.cna.com.tw/project/drunkdrivingDownload/fatal_export.csv)
### 酒駕致傷案件
- [2000-201901](https://www.cna.com.tw/project/drunkdrivingDownload/hurt_export.csv)

## License

