# rsyslog
socket protocol.

## プロトコル
udp

## port
514(デフォ)

## config

`/etc/rsyslog.conf`

## log フォーマット

Use template.

#### rsyslog.conf
```
$template mytemplate,"%timegenerated%,%msg%\n"
local6.*var/log/custom.log;mytemplate
```

途中改行してもおｋ
```
$template
mytemplate,"%timegenerated%,%msg%\n"
local6.*var/log/custom.log;mytemplate
```

#### facility

`%msg, %timegenerated and more...`


| Facility | 用途 |
|:---------|:----|
| msg      | ログ |
| hostname | ログ出したホスト名  |
| fromhost | ログを受け取ったホスト名 |
| programname | プログラム名 |
| syslogfacility | ファシリティ(数字) |
| syslogfacility-text | ファシリティ(テキスト) |
| syslogseverity | プライオリティ（数字） |
| syslogseverity-text | プライオリティ（テキスト） |
| syslogpriority | syslogseverityと同等 |
| syslogpriority-text | syslogseverity-textと同等 |
| timegenerated | ログを受け取った日時 |
| timereported | ログが出力された日時  |
| timestamp | timereportedと同等  |
| `$now` | 現在時刻（書式：YYYY-MM-DD） |
| `$year` | 現在の年（4けた）  |
| `$month` | 現在の月（2けた）  |
| `$day` | 現在の日（2けた）  |
| `$hour` | 現在の時（24時間表記、2けた）  |
| `$minute` | 現在の分（2けた）  |
