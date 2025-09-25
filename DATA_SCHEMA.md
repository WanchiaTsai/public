# `data.json` 結構說明

這個檔案詳細說明 `data.json` 檔案的結構以及每個欄位的意義。

`data.json` 是一個包含多個「行程物件」（leg object）的 JSON 陣列。每一個物件代表旅行中的一個獨立區段。

## 行程物件欄位說明

| 欄位名稱        | 資料類型 | 說明                                                                 | 範例                                                                   |
| :-------------- | :------- | :------------------------------------------------------------------- | :--------------------------------------------------------------------- |
| `from`          | `String` | 行程的起點。                                                         | `"TPE 桃園國際機場"`                                                   |
| `to`            | `String` | 行程的終點。                                                         | `"AXT 秋田機場 (あきたくうこう)"`                                        |
| `distance`      | `Number` | 這段行程的距離，單位為公里（km）。                                   | `2780`                                                                 |
| `duration`      | `String` | 這段行程所需的時間。                                                 | `"4時間20分"`                                                          |
| `route`         | `String` | 路線的簡要說明或航班號碼等資訊。                                     | `"航班號碼: IT256"`                                                    |
| `date`          | `String` | 行程發生的日期。                                                     | `"9月28日"`                                                            |
| `departureTime` | `String` | 出發時間。                                                           | `"08:00 AM"`                                                           |
| `travelMode`    | `String` | 交通方式。可能的值包括：`flight`, `driving`, `walking`, `boat`, `bus`, `ropeway`, `stay`, `airport_service`。 | `"flight"`                                                             |
| `navigationLink`| `String` | (選填) 提供導航用的連結，通常是 Google Maps 或類似服務的路線連結。 | `"https://www.google.com/maps/dir/..."` |
| `infoLink`      | `String` | (選填) 提供額外資訊的連結，例如住宿網站、參考資料或官方網站。   | `"https://maps.app.goo.gl/xYy6kR25EYDUyB4a9"` |
| `airline`       | `String` | (選填) 航空公司的名稱，僅在 `travelMode` 為 `flight` 時使用。        | `"tigersmart"`                                                         |
| `flightNumber`  | `String` | (選填) 航班號碼，僅在 `travelMode` 為 `flight` 時使用。              | `"IT256"`                                                              |
| `isRoundTrip`   | `Boolean`| (選填) 標示這是否為一個往返行程，主要用於登山等活動。                | `true`                                                                 |
