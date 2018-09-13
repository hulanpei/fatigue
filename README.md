# Fatigue Detection

疲勞偵測工作內容

## 主要技術

```
OpenCV, Object Detection, Image Process, Python
```

## 專利

因本專案限定使用 Webcam 又要將影像傳輸到使用者瀏覽器，所以本人申請了兼具辨識與傳輸功能之 Webcam 專利：

![](https://github.com/hulanpei/fatigue/blob/master/resources/architecture.png)

* 本發明係以 Webcam 建構兼具影像處理與影像傳輸功能之系統架構，遠端只要有瀏覽器，不須而外安裝其他軟體，即可觀看即時影像及並進行影像處理。
* 一般影像處理程式須具備一台電腦，若還需將影像傳輸到遠端，則影像來源需採用 IP CAM，影像處理程式及遠端影像監控都是透過 IP CAM 所傳輸的影像；但與 Webcam 相比，IP CAM 成本較高、體型較龐大；若能用 Webcam 取代 IP CAM，則產品將更具有競爭力。
* 若使用 Webcam，則除了原來的影像處理程式外，還須具有影像傳輸程式，但 Webcam 只能讓一個程式佔有，因此想要供影像處理及影像傳輸程式同時使用是無法達成。
* 本發明之系統架構包括一Webcam，一影像處理程式，一將影像編碼成 JPEG 格式的 HTTP Servr 程式，一台提供該 Webcam、影像處理程式及HTTP Server程式使用之電腦，一台裝有瀏覽器、能上網之電腦。
* 本系統架構是 Webcam 由影像處理程式佔有，尤其處理最原始、未編碼的影像資料，在其讀取影像資料時，將其讀取之資料屬性設成公用，使其可供其他程式使用；HTTP Servr 程式就可使用此公用屬性資料，將其編碼成JPEG 格式，傳輸到遠端瀏覽器。
