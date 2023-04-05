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
| timeshiftを使う | timeshiftの使用を切替えます。 |

### 予約
| 項目 | 機能 |
----|----
| 録画頭切れ防止 | EPGStationのallowEndLack設定を切替えます。 |

### 再生
| 項目 | 機能 |
----|----
| m2tsモード番号 | デフォルトのm2tsモードを指定します。 |

#### 録画再生の優先順位
エンコードされたファイルが優先されます。

### 番組表
| 項目 | 機能 |
----|----
| 非同期で取得 | 番組情報を非同期で取得します。 |
| グループ指定 | 指定したチャンネルグループを使用します。 |
| グループファイル | 使用するxmlファイルを指定します。 |

#### グループファイル
```xml
<groups>
  <group>
	<groupName>GP1</groupName>
	<channels>
	  <sid>40960</sid>
	  <sid>2056</sid>
	</channels>
  </group>
  <group>
	<groupName>GP2</groupName>
	<channels>
	  <sid>101</sid>
	  <sid>103</sid>
	</channels>
  </group>
</groups>
```

### 録画
| 項目 | 機能 |
----|----
| ディレクトリ表示 | 全ての録画に対してディレクトリ表示します。 |

