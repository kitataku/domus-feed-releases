# セキュリティレポート
本アプリケーションの配布物については以下のセキュリティチェックを実施しています。

セキュリティに関する問題を発見した場合は、[GitHub Issues](https://github.com/kitataku/domus-feed-releases/issues)にご連絡ください。

## Virus Total
配布している実行ファイルについて[VirusTotal](https://www.virustotal.com/gui/home/)によるスキャンを実施しています。

### スキャン結果
|ファイル名|スキャン結果|
|---|---|
|domusfeed.exe|[スキャン結果](https://www.virustotal.com/gui/file/9ef6961abe37958fa4b1f3eba2160e3f04c86f54aca0d501fe53b1a57d6548bd/detection)|

### スキャン結果の解釈
スキャン結果のうち、Trapmine が `Malicious.high.ml.score` を報告しています。これは機械学習モデルによるヒューリスティック検出であり、同様に機械学習解析を行う Acronis (Static ML) が Undetected を示していることからも、誤検知と判断しています。本アプリケーションは v2.0 よりバックエンドを Rust (Tauri) に刷新しており、従来の Python + PyInstaller 構成に由来する誤検知は解消されました。現在報告されている検出は、未署名の実行ファイルに対する機械学習エンジン固有の誤反応と考えられます。

## Cargo Audit
確認時点で発生している警告・脆弱性はいずれもTauriまたはsqlxが内部で使用している依存関係によるものです。特にrsa 0.9.10（RUSTSEC-2023-0071）はsqlxのMySQL用ドライバ経由で混入していますが、本アプリはSQLiteのみを使用しているためRSA演算は実行されません。現状のアプリケーション独自のコードに起因する脆弱性は確認されておりません。

### 実行結果
```
Crate:     rsa
Version:   0.9.10
Title:     Marvin Attack: potential key recovery through timing sidechannels
Date:      2023-11-22
ID:        RUSTSEC-2023-0071
URL:       https://rustsec.org/advisories/RUSTSEC-2023-0071
Severity:  5.9 (medium)
Solution:  No fixed upgrade is available!
Dependency tree:
rsa 0.9.10
└── sqlx-mysql 0.8.6
    ├── sqlx-macros-core 0.8.6
    │   └── sqlx-macros 0.8.6
    │       └── sqlx 0.8.6
    │           └── domusfeed 2.0.0
    └── sqlx 0.8.6

Crate:     atk
Version:   0.18.2
Warning:   unmaintained
Title:     gtk-rs GTK3 bindings - no longer maintained
Date:      2024-03-04
ID:        RUSTSEC-2024-0413
URL:       https://rustsec.org/advisories/RUSTSEC-2024-0413
Dependency tree:
atk 0.18.2
└── gtk 0.18.2
    ├── wry 0.53.5
    │   └── tauri-runtime-wry 2.9.3
    │       └── tauri 2.9.5
    │           ├── tauri-plugin-opener 2.5.2
    │           │   └── domusfeed 2.0.0
    │           └── domusfeed 2.0.0
    ├── webkit2gtk 2.0.1
    │   ├── wry 0.53.5
    │   ├── tauri-runtime-wry 2.9.3
    │   ├── tauri-runtime 2.9.2
    │   │   ├── tauri-runtime-wry 2.9.3
    │   │   └── tauri 2.9.5
    │   └── tauri 2.9.5
    ├── tauri-runtime-wry 2.9.3
    ├── tauri-runtime 2.9.2
    ├── tauri 2.9.5
    ├── tao 0.34.5
    │   └── tauri-runtime-wry 2.9.3
    ├── muda 0.17.1
    │   ├── tray-icon 0.21.2
    │   │   └── tauri 2.9.5
    │   └── tauri 2.9.5
    └── libappindicator 0.9.0
        └── tray-icon 0.21.2

Crate:     atk-sys
Version:   0.18.2
Warning:   unmaintained
Title:     gtk-rs GTK3 bindings - no longer maintained
Date:      2024-03-04
ID:        RUSTSEC-2024-0416
URL:       https://rustsec.org/advisories/RUSTSEC-2024-0416
Dependency tree:
atk-sys 0.18.2
├── gtk-sys 0.18.2
│   ├── webkit2gtk-sys 2.0.1
│   │   ├── wry 0.53.5
│   │   │   └── tauri-runtime-wry 2.9.3
│   │   │       └── tauri 2.9.5
│   │   │           ├── tauri-plugin-opener 2.5.2
│   │   │           │   └── domusfeed 2.0.0
│   │   │           └── domusfeed 2.0.0
│   │   └── webkit2gtk 2.0.1
│   │       ├── wry 0.53.5
│   │       ├── tauri-runtime-wry 2.9.3
│   │       ├── tauri-runtime 2.9.2
│   │       │   ├── tauri-runtime-wry 2.9.3
│   │       │   └── tauri 2.9.5
│   │       └── tauri 2.9.5
│   ├── webkit2gtk 2.0.1
│   ├── libappindicator-sys 0.9.0
│   │   └── libappindicator 0.9.0
│   │       └── tray-icon 0.21.2
│   │           └── tauri 2.9.5
│   ├── libappindicator 0.9.0
│   └── gtk 0.18.2
│       ├── wry 0.53.5
│       ├── webkit2gtk 2.0.1
│       ├── tauri-runtime-wry 2.9.3
│       ├── tauri-runtime 2.9.2
│       ├── tauri 2.9.5
│       ├── tao 0.34.5
│       │   └── tauri-runtime-wry 2.9.3
│       ├── muda 0.17.1
│       │   ├── tray-icon 0.21.2
│       │   └── tauri 2.9.5
│       └── libappindicator 0.9.0
└── atk 0.18.2
    └── gtk 0.18.2

Crate:     fxhash
Version:   0.2.1
Warning:   unmaintained
Title:     fxhash - no longer maintained
Date:      2025-09-05
ID:        RUSTSEC-2025-0057
URL:       https://rustsec.org/advisories/RUSTSEC-2025-0057
Dependency tree:
fxhash 0.2.1
└── selectors 0.24.0
    └── kuchikiki 0.8.8-speedreader
        ├── wry 0.53.5
        │   └── tauri-runtime-wry 2.9.3
        │       └── tauri 2.9.5
        │           ├── tauri-plugin-opener 2.5.2
        │           │   └── domusfeed 2.0.0
        │           └── domusfeed 2.0.0
        └── tauri-utils 2.8.1
            ├── tauri-runtime-wry 2.9.3
            ├── tauri-runtime 2.9.2
            │   ├── tauri-runtime-wry 2.9.3
            │   └── tauri 2.9.5
            ├── tauri-plugin 2.5.2
            │   └── tauri-plugin-opener 2.5.2
            ├── tauri-macros 2.5.2
            │   └── tauri 2.9.5
            ├── tauri-codegen 2.5.2
            │   └── tauri-macros 2.5.2
            ├── tauri-build 2.5.3
            │   ├── tauri 2.9.5
            │   └── domusfeed 2.0.0
            └── tauri 2.9.5

Crate:     gdk
Version:   0.18.2
Warning:   unmaintained
Title:     gtk-rs GTK3 bindings - no longer maintained
Date:      2024-03-04
ID:        RUSTSEC-2024-0412
URL:       https://rustsec.org/advisories/RUSTSEC-2024-0412
Dependency tree:
gdk 0.18.2
├── webkit2gtk 2.0.1
│   ├── wry 0.53.5
│   │   └── tauri-runtime-wry 2.9.3
│   │       └── tauri 2.9.5
│   │           ├── tauri-plugin-opener 2.5.2
│   │           │   └── domusfeed 2.0.0
│   │           └── domusfeed 2.0.0
│   ├── tauri-runtime-wry 2.9.3
│   ├── tauri-runtime 2.9.2
│   │   ├── tauri-runtime-wry 2.9.3
│   │   └── tauri 2.9.5
│   └── tauri 2.9.5
├── gtk 0.18.2
│   ├── wry 0.53.5
│   ├── webkit2gtk 2.0.1
│   ├── tauri-runtime-wry 2.9.3
│   ├── tauri-runtime 2.9.2
│   ├── tauri 2.9.5
│   ├── tao 0.34.5
│   │   └── tauri-runtime-wry 2.9.3
│   ├── muda 0.17.1
│   │   ├── tray-icon 0.21.2
│   │   │   └── tauri 2.9.5
│   │   └── tauri 2.9.5
│   └── libappindicator 0.9.0
│       └── tray-icon 0.21.2
└── gdkx11 0.18.2
    └── wry 0.53.5

Crate:     gdk-sys
Version:   0.18.2
Warning:   unmaintained
Title:     gtk-rs GTK3 bindings - no longer maintained
Date:      2024-03-04
ID:        RUSTSEC-2024-0418
URL:       https://rustsec.org/advisories/RUSTSEC-2024-0418
Dependency tree:
gdk-sys 0.18.2
├── webkit2gtk-sys 2.0.1
│   ├── wry 0.53.5
│   │   └── tauri-runtime-wry 2.9.3
│   │       └── tauri 2.9.5
│   │           ├── tauri-plugin-opener 2.5.2
│   │           │   └── domusfeed 2.0.0
│   │           └── domusfeed 2.0.0
│   └── webkit2gtk 2.0.1
│       ├── wry 0.53.5
│       ├── tauri-runtime-wry 2.9.3
│       ├── tauri-runtime 2.9.2
│       │   ├── tauri-runtime-wry 2.9.3
│       │   └── tauri 2.9.5
│       └── tauri 2.9.5
├── webkit2gtk 2.0.1
├── gtk-sys 0.18.2
│   ├── webkit2gtk-sys 2.0.1
│   ├── webkit2gtk 2.0.1
│   ├── libappindicator-sys 0.9.0
│   │   └── libappindicator 0.9.0
│   │       └── tray-icon 0.21.2
│   │           └── tauri 2.9.5
│   ├── libappindicator 0.9.0
│   └── gtk 0.18.2
│       ├── wry 0.53.5
│       ├── webkit2gtk 2.0.1
│       ├── tauri-runtime-wry 2.9.3
│       ├── tauri-runtime 2.9.2
│       ├── tauri 2.9.5
│       ├── tao 0.34.5
│       │   └── tauri-runtime-wry 2.9.3
│       ├── muda 0.17.1
│       │   ├── tray-icon 0.21.2
│       │   └── tauri 2.9.5
│       └── libappindicator 0.9.0
├── gdkx11-sys 0.18.2
│   ├── tao 0.34.5
│   └── gdkx11 0.18.2
│       └── wry 0.53.5
├── gdkwayland-sys 0.18.2
│   └── tao 0.34.5
└── gdk 0.18.2
    ├── webkit2gtk 2.0.1
    ├── gtk 0.18.2
    └── gdkx11 0.18.2

Crate:     gdkwayland-sys
Version:   0.18.2
Warning:   unmaintained
Title:     gtk-rs GTK3 bindings - no longer maintained
Date:      2024-03-04
ID:        RUSTSEC-2024-0411
URL:       https://rustsec.org/advisories/RUSTSEC-2024-0411
Dependency tree:
gdkwayland-sys 0.18.2
└── tao 0.34.5
    └── tauri-runtime-wry 2.9.3
        └── tauri 2.9.5
            ├── tauri-plugin-opener 2.5.2
            │   └── domusfeed 2.0.0
            └── domusfeed 2.0.0

Crate:     gdkx11
Version:   0.18.2
Warning:   unmaintained
Title:     gtk-rs GTK3 bindings - no longer maintained
Date:      2024-03-04
ID:        RUSTSEC-2024-0417
URL:       https://rustsec.org/advisories/RUSTSEC-2024-0417
Dependency tree:
gdkx11 0.18.2
└── wry 0.53.5
    └── tauri-runtime-wry 2.9.3
        └── tauri 2.9.5
            ├── tauri-plugin-opener 2.5.2
            │   └── domusfeed 2.0.0
            └── domusfeed 2.0.0

Crate:     gdkx11-sys
Version:   0.18.2
Warning:   unmaintained
Title:     gtk-rs GTK3 bindings - no longer maintained
Date:      2024-03-04
ID:        RUSTSEC-2024-0414
URL:       https://rustsec.org/advisories/RUSTSEC-2024-0414
Dependency tree:
gdkx11-sys 0.18.2
├── tao 0.34.5
│   └── tauri-runtime-wry 2.9.3
│       └── tauri 2.9.5
│           ├── tauri-plugin-opener 2.5.2
│           │   └── domusfeed 2.0.0
│           └── domusfeed 2.0.0
└── gdkx11 0.18.2
    └── wry 0.53.5
        └── tauri-runtime-wry 2.9.3

Crate:     gtk
Version:   0.18.2
Warning:   unmaintained
Title:     gtk-rs GTK3 bindings - no longer maintained
Date:      2024-03-04
ID:        RUSTSEC-2024-0415
URL:       https://rustsec.org/advisories/RUSTSEC-2024-0415
Dependency tree:
gtk 0.18.2
├── wry 0.53.5
│   └── tauri-runtime-wry 2.9.3
│       └── tauri 2.9.5
│           ├── tauri-plugin-opener 2.5.2
│           │   └── domusfeed 2.0.0
│           └── domusfeed 2.0.0
├── webkit2gtk 2.0.1
│   ├── wry 0.53.5
│   ├── tauri-runtime-wry 2.9.3
│   ├── tauri-runtime 2.9.2
│   │   ├── tauri-runtime-wry 2.9.3
│   │   └── tauri 2.9.5
│   └── tauri 2.9.5
├── tauri-runtime-wry 2.9.3
├── tauri-runtime 2.9.2
├── tauri 2.9.5
├── tao 0.34.5
│   └── tauri-runtime-wry 2.9.3
├── muda 0.17.1
│   ├── tray-icon 0.21.2
│   │   └── tauri 2.9.5
│   └── tauri 2.9.5
└── libappindicator 0.9.0
    └── tray-icon 0.21.2

Crate:     gtk-sys
Version:   0.18.2
Warning:   unmaintained
Title:     gtk-rs GTK3 bindings - no longer maintained
Date:      2024-03-04
ID:        RUSTSEC-2024-0420
URL:       https://rustsec.org/advisories/RUSTSEC-2024-0420
Dependency tree:
gtk-sys 0.18.2
├── webkit2gtk-sys 2.0.1
│   ├── wry 0.53.5
│   │   └── tauri-runtime-wry 2.9.3
│   │       └── tauri 2.9.5
│   │           ├── tauri-plugin-opener 2.5.2
│   │           │   └── domusfeed 2.0.0
│   │           └── domusfeed 2.0.0
│   └── webkit2gtk 2.0.1
│       ├── wry 0.53.5
│       ├── tauri-runtime-wry 2.9.3
│       ├── tauri-runtime 2.9.2
│       │   ├── tauri-runtime-wry 2.9.3
│       │   └── tauri 2.9.5
│       └── tauri 2.9.5
├── webkit2gtk 2.0.1
├── libappindicator-sys 0.9.0
│   └── libappindicator 0.9.0
│       └── tray-icon 0.21.2
│           └── tauri 2.9.5
├── libappindicator 0.9.0
└── gtk 0.18.2
    ├── wry 0.53.5
    ├── webkit2gtk 2.0.1
    ├── tauri-runtime-wry 2.9.3
    ├── tauri-runtime 2.9.2
    ├── tauri 2.9.5
    ├── tao 0.34.5
    │   └── tauri-runtime-wry 2.9.3
    ├── muda 0.17.1
    │   ├── tray-icon 0.21.2
    │   └── tauri 2.9.5
    └── libappindicator 0.9.0

Crate:     gtk3-macros
Version:   0.18.2
Warning:   unmaintained
Title:     gtk-rs GTK3 bindings - no longer maintained
Date:      2024-03-04
ID:        RUSTSEC-2024-0419
URL:       https://rustsec.org/advisories/RUSTSEC-2024-0419
Dependency tree:
gtk3-macros 0.18.2
└── gtk 0.18.2
    ├── wry 0.53.5
    │   └── tauri-runtime-wry 2.9.3
    │       └── tauri 2.9.5
    │           ├── tauri-plugin-opener 2.5.2
    │           │   └── domusfeed 2.0.0
    │           └── domusfeed 2.0.0
    ├── webkit2gtk 2.0.1
    │   ├── wry 0.53.5
    │   ├── tauri-runtime-wry 2.9.3
    │   ├── tauri-runtime 2.9.2
    │   │   ├── tauri-runtime-wry 2.9.3
    │   │   └── tauri 2.9.5
    │   └── tauri 2.9.5
    ├── tauri-runtime-wry 2.9.3
    ├── tauri-runtime 2.9.2
    ├── tauri 2.9.5
    ├── tao 0.34.5
    │   └── tauri-runtime-wry 2.9.3
    ├── muda 0.17.1
    │   ├── tray-icon 0.21.2
    │   │   └── tauri 2.9.5
    │   └── tauri 2.9.5
    └── libappindicator 0.9.0
        └── tray-icon 0.21.2

Crate:     proc-macro-error
Version:   1.0.4
Warning:   unmaintained
Title:     proc-macro-error is unmaintained
Date:      2024-09-01
ID:        RUSTSEC-2024-0370
URL:       https://rustsec.org/advisories/RUSTSEC-2024-0370
Dependency tree:
proc-macro-error 1.0.4
├── gtk3-macros 0.18.2
│   └── gtk 0.18.2
│       ├── wry 0.53.5
│       │   └── tauri-runtime-wry 2.9.3
│       │       └── tauri 2.9.5
│       │           ├── tauri-plugin-opener 2.5.2
│       │           │   └── domusfeed 2.0.0
│       │           └── domusfeed 2.0.0
│       ├── webkit2gtk 2.0.1
│       │   ├── wry 0.53.5
│       │   ├── tauri-runtime-wry 2.9.3
│       │   ├── tauri-runtime 2.9.2
│       │   │   ├── tauri-runtime-wry 2.9.3
│       │   │   └── tauri 2.9.5
│       │   └── tauri 2.9.5
│       ├── tauri-runtime-wry 2.9.3
│       ├── tauri-runtime 2.9.2
│       ├── tauri 2.9.5
│       ├── tao 0.34.5
│       │   └── tauri-runtime-wry 2.9.3
│       ├── muda 0.17.1
│       │   ├── tray-icon 0.21.2
│       │   │   └── tauri 2.9.5
│       │   └── tauri 2.9.5
│       └── libappindicator 0.9.0
│           └── tray-icon 0.21.2
└── glib-macros 0.18.5
    └── glib 0.18.5
        ├── webkit2gtk 2.0.1
        ├── soup3 0.5.0
        │   ├── wry 0.53.5
        │   └── webkit2gtk 2.0.1
        ├── pango 0.18.3
        │   ├── gtk 0.18.2
        │   └── gdk 0.18.2
        │       ├── webkit2gtk 2.0.1
        │       ├── gtk 0.18.2
        │       └── gdkx11 0.18.2
        │           └── wry 0.53.5
        ├── libappindicator 0.9.0
        ├── javascriptcore-rs 1.1.2
        │   ├── wry 0.53.5
        │   └── webkit2gtk 2.0.1
        ├── gtk 0.18.2
        ├── gio 0.18.4
        │   ├── webkit2gtk 2.0.1
        │   ├── soup3 0.5.0
        │   ├── pango 0.18.3
        │   ├── gtk 0.18.2
        │   ├── gdkx11 0.18.2
        │   ├── gdk-pixbuf 0.18.5
        │   │   ├── gtk 0.18.2
        │   │   └── gdk 0.18.2
        │   └── gdk 0.18.2
        ├── gdkx11 0.18.2
        ├── gdk-pixbuf 0.18.5
        ├── gdk 0.18.2
        ├── cairo-rs 0.18.5
        │   ├── webkit2gtk 2.0.1
        │   ├── gtk 0.18.2
        │   └── gdk 0.18.2
        └── atk 0.18.2
            └── gtk 0.18.2

Crate:     unic-char-property
Version:   0.9.0
Warning:   unmaintained
Title:     `unic-char-property` is unmaintained
Date:      2025-10-18
ID:        RUSTSEC-2025-0081
URL:       https://rustsec.org/advisories/RUSTSEC-2025-0081
Dependency tree:
unic-char-property 0.9.0
└── unic-ucd-ident 0.9.0
    └── urlpattern 0.3.0
        └── tauri-utils 2.8.1
            ├── tauri-runtime-wry 2.9.3
            │   └── tauri 2.9.5
            │       ├── tauri-plugin-opener 2.5.2
            │       │   └── domusfeed 2.0.0
            │       └── domusfeed 2.0.0
            ├── tauri-runtime 2.9.2
            │   ├── tauri-runtime-wry 2.9.3
            │   └── tauri 2.9.5
            ├── tauri-plugin 2.5.2
            │   └── tauri-plugin-opener 2.5.2
            ├── tauri-macros 2.5.2
            │   └── tauri 2.9.5
            ├── tauri-codegen 2.5.2
            │   └── tauri-macros 2.5.2
            ├── tauri-build 2.5.3
            │   ├── tauri 2.9.5
            │   └── domusfeed 2.0.0
            └── tauri 2.9.5

Crate:     unic-char-range
Version:   0.9.0
Warning:   unmaintained
Title:     `unic-char-range` is unmaintained
Date:      2025-10-18
ID:        RUSTSEC-2025-0075
URL:       https://rustsec.org/advisories/RUSTSEC-2025-0075
Dependency tree:
unic-char-range 0.9.0
├── unic-ucd-ident 0.9.0
│   └── urlpattern 0.3.0
│       └── tauri-utils 2.8.1
│           ├── tauri-runtime-wry 2.9.3
│           │   └── tauri 2.9.5
│           │       ├── tauri-plugin-opener 2.5.2
│           │       │   └── domusfeed 2.0.0
│           │       └── domusfeed 2.0.0
│           ├── tauri-runtime 2.9.2
│           │   ├── tauri-runtime-wry 2.9.3
│           │   └── tauri 2.9.5
│           ├── tauri-plugin 2.5.2
│           │   └── tauri-plugin-opener 2.5.2
│           ├── tauri-macros 2.5.2
│           │   └── tauri 2.9.5
│           ├── tauri-codegen 2.5.2
│           │   └── tauri-macros 2.5.2
│           ├── tauri-build 2.5.3
│           │   ├── tauri 2.9.5
│           │   └── domusfeed 2.0.0
│           └── tauri 2.9.5
└── unic-char-property 0.9.0
    └── unic-ucd-ident 0.9.0

Crate:     unic-common
Version:   0.9.0
Warning:   unmaintained
Title:     `unic-common` is unmaintained
Date:      2025-10-18
ID:        RUSTSEC-2025-0080
URL:       https://rustsec.org/advisories/RUSTSEC-2025-0080
Dependency tree:
unic-common 0.9.0
└── unic-ucd-version 0.9.0
    └── unic-ucd-ident 0.9.0
        └── urlpattern 0.3.0
            └── tauri-utils 2.8.1
                ├── tauri-runtime-wry 2.9.3
                │   └── tauri 2.9.5
                │       ├── tauri-plugin-opener 2.5.2
                │       │   └── domusfeed 2.0.0
                │       └── domusfeed 2.0.0
                ├── tauri-runtime 2.9.2
                │   ├── tauri-runtime-wry 2.9.3
                │   └── tauri 2.9.5
                ├── tauri-plugin 2.5.2
                │   └── tauri-plugin-opener 2.5.2
                ├── tauri-macros 2.5.2
                │   └── tauri 2.9.5
                ├── tauri-codegen 2.5.2
                │   └── tauri-macros 2.5.2
                ├── tauri-build 2.5.3
                │   ├── tauri 2.9.5
                │   └── domusfeed 2.0.0
                └── tauri 2.9.5

Crate:     unic-ucd-ident
Version:   0.9.0
Warning:   unmaintained
Title:     `unic-ucd-ident` is unmaintained
Date:      2025-10-18
ID:        RUSTSEC-2025-0100
URL:       https://rustsec.org/advisories/RUSTSEC-2025-0100
Dependency tree:
unic-ucd-ident 0.9.0
└── urlpattern 0.3.0
    └── tauri-utils 2.8.1
        ├── tauri-runtime-wry 2.9.3
        │   └── tauri 2.9.5
        │       ├── tauri-plugin-opener 2.5.2
        │       │   └── domusfeed 2.0.0
        │       └── domusfeed 2.0.0
        ├── tauri-runtime 2.9.2
        │   ├── tauri-runtime-wry 2.9.3
        │   └── tauri 2.9.5
        ├── tauri-plugin 2.5.2
        │   └── tauri-plugin-opener 2.5.2
        ├── tauri-macros 2.5.2
        │   └── tauri 2.9.5
        ├── tauri-codegen 2.5.2
        │   └── tauri-macros 2.5.2
        ├── tauri-build 2.5.3
        │   ├── tauri 2.9.5
        │   └── domusfeed 2.0.0
        └── tauri 2.9.5

Crate:     unic-ucd-version
Version:   0.9.0
Warning:   unmaintained
Title:     `unic-ucd-version` is unmaintained
Date:      2025-10-18
ID:        RUSTSEC-2025-0098
URL:       https://rustsec.org/advisories/RUSTSEC-2025-0098
Dependency tree:
unic-ucd-version 0.9.0
└── unic-ucd-ident 0.9.0
    └── urlpattern 0.3.0
        └── tauri-utils 2.8.1
            ├── tauri-runtime-wry 2.9.3
            │   └── tauri 2.9.5
            │       ├── tauri-plugin-opener 2.5.2
            │       │   └── domusfeed 2.0.0
            │       └── domusfeed 2.0.0
            ├── tauri-runtime 2.9.2
            │   ├── tauri-runtime-wry 2.9.3
            │   └── tauri 2.9.5
            ├── tauri-plugin 2.5.2
            │   └── tauri-plugin-opener 2.5.2
            ├── tauri-macros 2.5.2
            │   └── tauri 2.9.5
            ├── tauri-codegen 2.5.2
            │   └── tauri-macros 2.5.2
            ├── tauri-build 2.5.3
            │   ├── tauri 2.9.5
            │   └── domusfeed 2.0.0
            └── tauri 2.9.5

Crate:     glib
Version:   0.18.5
Warning:   unsound
Title:     Unsoundness in `Iterator` and `DoubleEndedIterator` impls for `glib::VariantStrIter`
Date:      2024-03-30
ID:        RUSTSEC-2024-0429
URL:       https://rustsec.org/advisories/RUSTSEC-2024-0429
Dependency tree:
glib 0.18.5
├── webkit2gtk 2.0.1
│   ├── wry 0.53.5
│   │   └── tauri-runtime-wry 2.9.3
│   │       └── tauri 2.9.5
│   │           ├── tauri-plugin-opener 2.5.2
│   │           │   └── domusfeed 2.0.0
│   │           └── domusfeed 2.0.0
│   ├── tauri-runtime-wry 2.9.3
│   ├── tauri-runtime 2.9.2
│   │   ├── tauri-runtime-wry 2.9.3
│   │   └── tauri 2.9.5
│   └── tauri 2.9.5
├── soup3 0.5.0
│   ├── wry 0.53.5
│   └── webkit2gtk 2.0.1
├── pango 0.18.3
│   ├── gtk 0.18.2
│   │   ├── wry 0.53.5
│   │   ├── webkit2gtk 2.0.1
│   │   ├── tauri-runtime-wry 2.9.3
│   │   ├── tauri-runtime 2.9.2
│   │   ├── tauri 2.9.5
│   │   ├── tao 0.34.5
│   │   │   └── tauri-runtime-wry 2.9.3
│   │   ├── muda 0.17.1
│   │   │   ├── tray-icon 0.21.2
│   │   │   │   └── tauri 2.9.5
│   │   │   └── tauri 2.9.5
│   │   └── libappindicator 0.9.0
│   │       └── tray-icon 0.21.2
│   └── gdk 0.18.2
│       ├── webkit2gtk 2.0.1
│       ├── gtk 0.18.2
│       └── gdkx11 0.18.2
│           └── wry 0.53.5
├── libappindicator 0.9.0
├── javascriptcore-rs 1.1.2
│   ├── wry 0.53.5
│   └── webkit2gtk 2.0.1
├── gtk 0.18.2
├── gio 0.18.4
│   ├── webkit2gtk 2.0.1
│   ├── soup3 0.5.0
│   ├── pango 0.18.3
│   ├── gtk 0.18.2
│   ├── gdkx11 0.18.2
│   ├── gdk-pixbuf 0.18.5
│   │   ├── gtk 0.18.2
│   │   └── gdk 0.18.2
│   └── gdk 0.18.2
├── gdkx11 0.18.2
├── gdk-pixbuf 0.18.5
├── gdk 0.18.2
├── cairo-rs 0.18.5
│   ├── webkit2gtk 2.0.1
│   ├── gtk 0.18.2
│   └── gdk 0.18.2
└── atk 0.18.2
    └── gtk 0.18.2

Crate:     rand
Version:   0.7.3
Warning:   unsound
Title:     Rand is unsound with a custom logger using `rand::rng()`
Date:      2026-04-09
ID:        RUSTSEC-2026-0097
URL:       https://rustsec.org/advisories/RUSTSEC-2026-0097
Dependency tree:
rand 0.7.3
└── phf_generator 0.8.0
    └── phf_codegen 0.8.0
        └── selectors 0.24.0
            └── kuchikiki 0.8.8-speedreader
                ├── wry 0.53.5
                │   └── tauri-runtime-wry 2.9.3
                │       └── tauri 2.9.5
                │           ├── tauri-plugin-opener 2.5.2
                │           │   └── domusfeed 2.0.0
                │           └── domusfeed 2.0.0
                └── tauri-utils 2.8.1
                    ├── tauri-runtime-wry 2.9.3
                    ├── tauri-runtime 2.9.2
                    │   ├── tauri-runtime-wry 2.9.3
                    │   └── tauri 2.9.5
                    ├── tauri-plugin 2.5.2
                    │   └── tauri-plugin-opener 2.5.2
                    ├── tauri-macros 2.5.2
                    │   └── tauri 2.9.5
                    ├── tauri-codegen 2.5.2
                    │   └── tauri-macros 2.5.2
                    ├── tauri-build 2.5.3
                    │   ├── tauri 2.9.5
                    │   └── domusfeed 2.0.0
                    └── tauri 2.9.5

Crate:     rand
Version:   0.8.5
Warning:   unsound
Title:     Rand is unsound with a custom logger using `rand::rng()`
Date:      2026-04-09
ID:        RUSTSEC-2026-0097
URL:       https://rustsec.org/advisories/RUSTSEC-2026-0097
Dependency tree:
rand 0.8.5
├── sqlx-postgres 0.8.6
│   ├── sqlx-macros-core 0.8.6
│   │   └── sqlx-macros 0.8.6
│   │       └── sqlx 0.8.6
│   │           └── domusfeed 2.0.0
│   └── sqlx 0.8.6
├── sqlx-mysql 0.8.6
│   ├── sqlx-macros-core 0.8.6
│   └── sqlx 0.8.6
├── phf_generator 0.11.3
│   ├── string_cache_codegen 0.5.4
│   │   └── markup5ever 0.14.1
│   │       └── html5ever 0.29.1
│   │           ├── wry 0.53.5
│   │           │   └── tauri-runtime-wry 2.9.3
│   │           │       └── tauri 2.9.5
│   │           │           ├── tauri-plugin-opener 2.5.2
│   │           │           │   └── domusfeed 2.0.0
│   │           │           └── domusfeed 2.0.0
│   │           ├── tauri-utils 2.8.1
│   │           │   ├── tauri-runtime-wry 2.9.3
│   │           │   ├── tauri-runtime 2.9.2
│   │           │   │   ├── tauri-runtime-wry 2.9.3
│   │           │   │   └── tauri 2.9.5
│   │           │   ├── tauri-plugin 2.5.2
│   │           │   │   └── tauri-plugin-opener 2.5.2
│   │           │   ├── tauri-macros 2.5.2
│   │           │   │   └── tauri 2.9.5
│   │           │   ├── tauri-codegen 2.5.2
│   │           │   │   └── tauri-macros 2.5.2
│   │           │   ├── tauri-build 2.5.3
│   │           │   │   ├── tauri 2.9.5
│   │           │   │   └── domusfeed 2.0.0
│   │           │   └── tauri 2.9.5
│   │           └── kuchikiki 0.8.8-speedreader
│   │               ├── wry 0.53.5
│   │               └── tauri-utils 2.8.1
│   ├── phf_macros 0.11.3
│   │   └── phf 0.11.3
│   │       ├── tauri-utils 2.8.1
│   │       └── markup5ever 0.14.1
│   └── phf_codegen 0.11.3
│       └── markup5ever 0.14.1
├── phf_generator 0.10.0
│   └── phf_macros 0.10.0
│       └── phf 0.10.1
│           └── cssparser 0.29.6
│               ├── selectors 0.24.0
│               │   └── kuchikiki 0.8.8-speedreader
│               └── kuchikiki 0.8.8-speedreader
└── num-bigint-dig 0.8.6
    └── rsa 0.9.10
        └── sqlx-mysql 0.8.6

Crate:     rand
Version:   0.9.2
Warning:   unsound
Title:     Rand is unsound with a custom logger using `rand::rng()`
Date:      2026-04-09
ID:        RUSTSEC-2026-0097
URL:       https://rustsec.org/advisories/RUSTSEC-2026-0097
Dependency tree:
rand 0.9.2
└── quinn-proto 0.11.14
    └── quinn 0.11.9
        └── reqwest 0.13.3
            └── domusfeed 2.0.0

error: 1 vulnerability found!
warning: 21 allowed warnings found
```