# EPG Test PVR
KODIのPVRアドオンです。

## 概要
EPGStationをTVサーバーとして、KODI上でTV視聴、録画予約、そして録画再生をサポートします。

## 特徴
 - 予約はEPG、又は時刻を指定して作成できます。
 - ルールとルール予約は、有効無効の切替のみできます。
 - 録画のドロップ情報をダイアログで表示できます。
 - 重複禁止（isOverlap）されている予約は表示されません。
 - 番組名、エピソード情報は番組名から生成します。

## 対応サーバー
 - EPGStation v2

## 対応OS
 - Windows
 - Raspberry Pi

## 設定項目
### 基本
| 項目 | 機能 |
----|----
| WUIのURL | サーバーのURLを記述します。<br>例 HTTP://192.168.1.101:8888 |
| timeshiftを使う | timeshiftの使用を切替えます。 |

### 予約
| 項目 | 機能 |
----|----
| 録画頭切れ防止 | EPGStationのallowEndLack設定を切替えます。 |

### 再生
| 項目 | 機能 |
----|----
| m2tsモード番号 | ライブ視聴時のモードを指定します。 |
 
## 予約、録画の注意点
### アドオンによる情報の更新
| タイミング | 更新情報 | 遅延時間 |
----|----|----
予約登録 | 予約一覧	| -
録画開始 | 予約一覧	| -
録画終了 | 予約一覧	| 20秒
録画終了 + 遅延 | 録画一覧 | 5秒

### ルール
 - TVサーバー上のルールは表示しますが作成できません。
 - 不要なルールは削除の代りに無効を使います。

### ルール予約
 - 不要なルール予約は削除の代りに無効を使います。

### 予約の異常
 - 予約終了時刻から60秒を経過してもTVサーバーに存在する予約を異常とします。

### 時刻指定予約
 - 時刻指定予約の実際の録画時刻が、指定した時刻より60秒程遅れます。
