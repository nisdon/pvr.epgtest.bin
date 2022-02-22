# EPG Test PVR
KODIのPVRアドオンです。

## 概要
EPGStationをTVサーバーとして、KODI上でTV視聴、録画予約、そして録画再生をサポートします。

## 特徴
 - 録画メニューから、録画のドロップ情報をダイアログで表示できます。
 - チャンネルメニューから、tsモードを切替えることができます。

## 対応サーバー
 - EPGStation v2
 - 動作確認バージョン 2.6.7

## 対応OS
 - Windows
 - Raspberry Pi

## 依存モジュール
 - libcurl

## 設定項目
### 基本
| 項目 | 機能 |
----|----
| WUIのURL | サーバーのURLを記述します。<br>例 HTTP://192.168.1.101:8888 |

### 予約
| 項目 | 機能 |
----|----
| 録画頭切れ防止 | EPGStationのallowEndLack設定を切替えます。 |

### 再生
| 項目 | 機能 |
----|----
| m2tsモード番号 | ライブ視聴時のメインモードを指定します。 |
| m2tsサブモード番号 | ライブ視聴時のサブモードを指定します。 |

### 番組表
| 項目 | 機能 |
----|----
| 非同期で取得 | 番組情報を非同期で取得します。 |

## 番組表について
### 先の表示日数
 - 1日から6日の範囲で設定が有効です。

## 予約、録画について
### 情報通知のタイミング
| 通知内容 | 更新情報 | 遅延時間 |
----|----|----
予約登録 | 予約一覧	| -
録画開始 | 予約一覧	| -
録画終了 | 予約一覧	| 20秒
録画終了 + 遅延 | 録画一覧 | 5秒

### ルール
 - ルール作成機能は未対応です。

### ルール予約
 - ルールによる予約は無効でも終了時間まで表示されます。（EPGStation 2.6.7対応）
