因為2024/3/4組務會議有同仁提到用照片搜尋歷史影像平台中的資料，組長提到希望由google 以圖找圖的方式可以被找到，於是發想用chatGPT 產生以圖找圖的程式，而且歷史影像平台有提供API給民眾共享及應用，讓使用者可以很方便的應用政府資料。

但是，https://photo.ardswc.gov.tw/api/phototags 中的所有SourceUrl 都還是舊的DomainName swcb.gov.tw，後來發現API位址: https://photo.ardswc.gov.tw/api/Media 也沒有包含全部的照片，只有1000筆資料。
![註解 2024-03-06 081423](https://github.com/max866-elephant/compareImage/assets/111369614/84482a0f-bea5-481c-b50b-72992801f0c9)
![註解 2024-03-06 081401](https://github.com/max866-elephant/compareImage/assets/111369614/67415afc-c646-4423-aedd-a7cd9b0b6e7a)

最後只好先從API 已經有提供的位址中找一張當範例(https://photo.ardswc.gov.tw/Repository/ViewEvent/637922656702584819 )，請chatGPT 產生以圖找圖的程式，放到colab(https://colab.research.google.com/drive/1OmIdm6_kXD5VKHu1smTpM48Ep0ac0VS-?usp=sharing )上跑，確認可以找到後，再分享給同仁使用。
![messageImage_1709643117649](https://github.com/max866-elephant/compareImage/assets/111369614/aa8171b1-b7dc-43a0-a5e0-54e69d26b08c)
![messageImage_1709643221941](https://github.com/max866-elephant/compareImage/assets/111369614/c7118a22-2c05-4999-bc4e-18391932e846)
  
效能上程式使用多執行緒比對，1000張找下來大約要花6分鐘尋找，大大節省人力和時間。
![messageImage_1709648752501](https://github.com/max866-elephant/compareImage/assets/111369614/b0538952-bb0d-419f-ade1-ef59cac7067c)

