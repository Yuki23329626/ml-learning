# auto downloader for images
  
## Environment  
  
系統環境: Ubuntu 16.04  
套件管理工具: anaconda  
python: 3.7  
需安裝之套件包: selenium  
  
## 1、執行程式  
  
直接執行 image-downloader  
會從搜狗瀏覽器裡面下載風景照，聽說 google 會偵測爬蟲鎖 IP  
目前處於測試階段，主要目的是用來下載"分辨圖中是否有芒果的分類器"使用的資料圖片  
尚未確認下載下來的圖片可能有哪些種類、大小等等  
目前是用"風景"當作搜尋字串  

之後打算訓練出"分辨圖中是否有芒果的分類器"，  
用來做"把圖案中的芒果框起來的 regression model"，用回歸分析找出框芒果的四個點  
不確定是否可行  
框物件如果可行的話，之後想嘗試輸出只含芒果部分的圖片，  
如果可以做到這一步，應該可以搭上最初做的分類器，以高準度辨別出芒果的品質  
時間上可能不太夠，需要及早進行測試與訓練  

備案，如果時間上真的不夠，可能需要手工對照片做處理，  
例如手動把圖案中不是芒果的部分去除  
用這種方式，來輸出只含有芒果的部分，再拿去做等級分類  

reference:  
1. 圖案去背景 Mask CNN:  
  https://matters.news/@tony_guo/%E5%88%A9%E7%94%A8mask-rcnn%E7%82%BA%E5%9C%96%E7%89%87%E5%8E%BB%E9%99%A4%E8%83%8C%E6%99%AF-zdpuAsEDBdrVrTawVqqeUuiJhCAAVUVdWvNZsxGTi2q3jXA1L  

```bash  
python image-downloader  
```  

## 2、離開  
  
```bash  
conda deactivate  
```  