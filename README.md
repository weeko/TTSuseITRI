# TTSuseITRI
call ITRI Web Service API, in http://tts.itri.org.tw/development/web_service_api.php ,have 3 way to transform text to voice file, Web Service API,Web Service Tools and JavaScript API.

Web Service API
本服務使用UTF-8之格式，提供SOAP（Simple Object Access Protocol）協議的TTS Web Service Servers，並提供合成音檔下載網址。
Web Service Tools
本服務提供程式開發者對於一般網頁訊息發佈時，可以網頁上聆聽合成效果並且將音檔下載至指定資料夾。
JavaScript API
本服務提供JavaScript範例程式供一般使用者使用於html環境(非php、asp等)下使用。

here are Web Service API:
本服務使用UTF-8之格式，提供SOAP（Simple Object Access Protocol）協議的TTS Web Service Servers，並提供合成音檔下載網址，供使用自行下載。
Web Service API提供函式(ConvertSimple, ConvertText, ConvertAdvancedText)的傳回值皆為String型態，其回傳值格式為resultCode&resultString&result，以〝&〞區隔開來，唯有resultCode等於0(Success)時，才會有result(Convert ID)的值產生。下方表格（表一）為執行狀況代碼 (resultCode)與說明(resultString)之對照值。
另外，在GetConvertStatus函式中，提供TTS合成的狀態，其格式為 resultCode&resultString&statusCode&status &result，以〝&〞區隔開來，當statusCode為2(completed)時，result的值為download音檔的位置；當statusCode為1(processing)時，result的值為waiting X Sec(X等於等待的秒數)；當statusCode為0(queued)時，代表程式尚未處理到這筆資料，請稍待片刻再來詢問目前合成的狀態。下方表格（表二）為狀態代碼(statusCode)與說明(status)之對照值。
下方表格（表三）中，為系統提供的所有語音合成聲音，必需使用ConvertText或者ConvertAdvancedText函式，才能設定不同的TTS Speaker。中英統合是指，使用單一語者聲音，即可針對含有中英文語句進行語音合成，而中英切換則是使用雙語者聲音來進行語音合成。
