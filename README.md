# EPG Test PVR
KODIのPVRアドオンです。

## 概要
EPGStationをTVサーバーとして、KODI上でTV視聴、録画予約、そして録画再生をサポートします。

## 特徴
 - 録画メニューから、録画のドロップ情報をダイアログで表示できます。
 - チャンネルメニューから、m2tsモードを切替えることができます。

## 対応サーバー
 - EPGStation v2
 - 動作確認バージョン 2.6.7

## 対応OS
 - Windows
 - Raspberry Pi
 - Android

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
| m2tsモード番号 | デフォルトのm2tsモードを指定します。 |

### 番組表
| 項目 | 機能 |
----|----
| 非同期で取得 | 番組情報を非同期で取得します。 |

### 録画
| 項目 | 機能 |
----|----
| 録画リストの更新 | 録画終了からリスト更新までの時間（秒）を指定します。 |
| ディレクトリ表示 | 全ての録画に対してディレクトリ表示します。 |

## 番組表について
### 先の表示日数
 - 1日から6日の範囲で設定が有効です。

## 予約について
### ルール
 - ルール作成機能は未対応です。

### ルール予約
 - ルールによる予約は無効でも終了時間まで表示されます。（EPGStation 2.6.7対応）

### サーバーとクライアント間の時差
 - kodi側時間が早い場合、タイマー終了時にタイマーステータスを「完了」にします。
 - EPGStation側時間が早い場合、タイマー終了と同時にアイテムは削除されます。

## 再生について
### ライブ視聴
 - m2ts配信のみです。

### 録画ビデオ視聴
 - ダウンロードのみです。
