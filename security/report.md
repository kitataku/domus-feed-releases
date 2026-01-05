# セキュリティレポート
## Virus Total
**domusfeed.exe**  
https://www.virustotal.com/gui/file/c8dd25a51b847d6bbb5cc0db6317ed1bfcc325a97abd5306281ddcdcaeb26f43/detection

**launch_server.exe**(Sidecar)  
https://www.virustotal.com/gui/file/16b05b73255d7580ac6fa392f54f00dfc6f48b6edf93581ceda75a3babb21e39/detection

**migrate.exe**(Sidecar)  
https://www.virustotal.com/gui/file/ba3daa147b51dcdf6a60e94a3fe411732ac6220669d4c4b93046bfcf4bcb2290/detection

### Cargo Audit
```
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
    │           ├── tauri-plugin-shell 2.3.3
    │           │   └── domusfeed 0.9.1
    │           ├── tauri-plugin-opener 2.5.2
    │           │   └── domusfeed 0.9.1
    │           ├── tauri-plugin-http 2.5.4
    │           │   └── domusfeed 0.9.1
    │           ├── tauri-plugin-fs 2.4.4
    │           │   └── tauri-plugin-http 2.5.4
    │           └── domusfeed 0.9.1
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
│   │   │           ├── tauri-plugin-shell 2.3.3
│   │   │           │   └── domusfeed 0.9.1
│   │   │           ├── tauri-plugin-opener 2.5.2
│   │   │           │   └── domusfeed 0.9.1
│   │   │           ├── tauri-plugin-http 2.5.4
│   │   │           │   └── domusfeed 0.9.1
│   │   │           ├── tauri-plugin-fs 2.4.4
│   │   │           │   └── tauri-plugin-http 2.5.4
│   │   │           └── domusfeed 0.9.1
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
        │           ├── tauri-plugin-shell 2.3.3
        │           │   └── domusfeed 0.9.1
        │           ├── tauri-plugin-opener 2.5.2
        │           │   └── domusfeed 0.9.1
        │           ├── tauri-plugin-http 2.5.4
        │           │   └── domusfeed 0.9.1
        │           ├── tauri-plugin-fs 2.4.4
        │           │   └── tauri-plugin-http 2.5.4
        │           └── domusfeed 0.9.1
        └── tauri-utils 2.8.1
            ├── tauri-runtime-wry 2.9.3
            ├── tauri-runtime 2.9.2
            │   ├── tauri-runtime-wry 2.9.3
            │   └── tauri 2.9.5
            ├── tauri-plugin-fs 2.4.4
            ├── tauri-plugin 2.5.2
            │   ├── tauri-plugin-shell 2.3.3
            │   ├── tauri-plugin-opener 2.5.2
            │   ├── tauri-plugin-http 2.5.4
            │   └── tauri-plugin-fs 2.4.4
            ├── tauri-macros 2.5.2
            │   └── tauri 2.9.5
            ├── tauri-codegen 2.5.2
            │   └── tauri-macros 2.5.2
            ├── tauri-build 2.5.3
            │   ├── tauri 2.9.5
            │   └── domusfeed 0.9.1
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
│   │           ├── tauri-plugin-shell 2.3.3
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-opener 2.5.2
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-http 2.5.4
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-fs 2.4.4
│   │           │   └── tauri-plugin-http 2.5.4
│   │           └── domusfeed 0.9.1
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
│   │           ├── tauri-plugin-shell 2.3.3
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-opener 2.5.2
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-http 2.5.4
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-fs 2.4.4
│   │           │   └── tauri-plugin-http 2.5.4
│   │           └── domusfeed 0.9.1
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
            ├── tauri-plugin-shell 2.3.3
            │   └── domusfeed 0.9.1
            ├── tauri-plugin-opener 2.5.2
            │   └── domusfeed 0.9.1
            ├── tauri-plugin-http 2.5.4
            │   └── domusfeed 0.9.1
            ├── tauri-plugin-fs 2.4.4
            │   └── tauri-plugin-http 2.5.4
            └── domusfeed 0.9.1

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
            ├── tauri-plugin-shell 2.3.3
            │   └── domusfeed 0.9.1
            ├── tauri-plugin-opener 2.5.2
            │   └── domusfeed 0.9.1
            ├── tauri-plugin-http 2.5.4
            │   └── domusfeed 0.9.1
            ├── tauri-plugin-fs 2.4.4
            │   └── tauri-plugin-http 2.5.4
            └── domusfeed 0.9.1

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
│           ├── tauri-plugin-shell 2.3.3
│           │   └── domusfeed 0.9.1
│           ├── tauri-plugin-opener 2.5.2
│           │   └── domusfeed 0.9.1
│           ├── tauri-plugin-http 2.5.4
│           │   └── domusfeed 0.9.1
│           ├── tauri-plugin-fs 2.4.4
│           │   └── tauri-plugin-http 2.5.4
│           └── domusfeed 0.9.1
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
│           ├── tauri-plugin-shell 2.3.3
│           │   └── domusfeed 0.9.1
│           ├── tauri-plugin-opener 2.5.2
│           │   └── domusfeed 0.9.1
│           ├── tauri-plugin-http 2.5.4
│           │   └── domusfeed 0.9.1
│           ├── tauri-plugin-fs 2.4.4
│           │   └── tauri-plugin-http 2.5.4
│           └── domusfeed 0.9.1
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
│   │           ├── tauri-plugin-shell 2.3.3
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-opener 2.5.2
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-http 2.5.4
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-fs 2.4.4
│   │           │   └── tauri-plugin-http 2.5.4
│   │           └── domusfeed 0.9.1
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
    │           ├── tauri-plugin-shell 2.3.3
    │           │   └── domusfeed 0.9.1
    │           ├── tauri-plugin-opener 2.5.2
    │           │   └── domusfeed 0.9.1
    │           ├── tauri-plugin-http 2.5.4
    │           │   └── domusfeed 0.9.1
    │           ├── tauri-plugin-fs 2.4.4
    │           │   └── tauri-plugin-http 2.5.4
    │           └── domusfeed 0.9.1
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
│       │           ├── tauri-plugin-shell 2.3.3
│       │           │   └── domusfeed 0.9.1
│       │           ├── tauri-plugin-opener 2.5.2
│       │           │   └── domusfeed 0.9.1
│       │           ├── tauri-plugin-http 2.5.4
│       │           │   └── domusfeed 0.9.1
│       │           ├── tauri-plugin-fs 2.4.4
│       │           │   └── tauri-plugin-http 2.5.4
│       │           └── domusfeed 0.9.1
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
        ├── tauri-utils 2.8.1
        │   ├── tauri-runtime-wry 2.9.3
        │   │   └── tauri 2.9.5
        │   │       ├── tauri-plugin-shell 2.3.3
        │   │       │   └── domusfeed 0.9.1
        │   │       ├── tauri-plugin-opener 2.5.2
        │   │       │   └── domusfeed 0.9.1
        │   │       ├── tauri-plugin-http 2.5.4
        │   │       │   └── domusfeed 0.9.1
        │   │       ├── tauri-plugin-fs 2.4.4
        │   │       │   └── tauri-plugin-http 2.5.4
        │   │       └── domusfeed 0.9.1
        │   ├── tauri-runtime 2.9.2
        │   │   ├── tauri-runtime-wry 2.9.3
        │   │   └── tauri 2.9.5
        │   ├── tauri-plugin-fs 2.4.4
        │   ├── tauri-plugin 2.5.2
        │   │   ├── tauri-plugin-shell 2.3.3
        │   │   ├── tauri-plugin-opener 2.5.2
        │   │   ├── tauri-plugin-http 2.5.4
        │   │   └── tauri-plugin-fs 2.4.4
        │   ├── tauri-macros 2.5.2
        │   │   └── tauri 2.9.5
        │   ├── tauri-codegen 2.5.2
        │   │   └── tauri-macros 2.5.2
        │   ├── tauri-build 2.5.3
        │   │   ├── tauri 2.9.5
        │   │   └── domusfeed 0.9.1
        │   └── tauri 2.9.5
        └── tauri-plugin-http 2.5.4

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
│       ├── tauri-utils 2.8.1
│       │   ├── tauri-runtime-wry 2.9.3
│       │   │   └── tauri 2.9.5
│       │   │       ├── tauri-plugin-shell 2.3.3
│       │   │       │   └── domusfeed 0.9.1
│       │   │       ├── tauri-plugin-opener 2.5.2
│       │   │       │   └── domusfeed 0.9.1
│       │   │       ├── tauri-plugin-http 2.5.4
│       │   │       │   └── domusfeed 0.9.1
│       │   │       ├── tauri-plugin-fs 2.4.4
│       │   │       │   └── tauri-plugin-http 2.5.4
│       │   │       └── domusfeed 0.9.1
│       │   ├── tauri-runtime 2.9.2
│       │   │   ├── tauri-runtime-wry 2.9.3
│       │   │   └── tauri 2.9.5
│       │   ├── tauri-plugin-fs 2.4.4
│       │   ├── tauri-plugin 2.5.2
│       │   │   ├── tauri-plugin-shell 2.3.3
│       │   │   ├── tauri-plugin-opener 2.5.2
│       │   │   ├── tauri-plugin-http 2.5.4
│       │   │   └── tauri-plugin-fs 2.4.4
│       │   ├── tauri-macros 2.5.2
│       │   │   └── tauri 2.9.5
│       │   ├── tauri-codegen 2.5.2
│       │   │   └── tauri-macros 2.5.2
│       │   ├── tauri-build 2.5.3
│       │   │   ├── tauri 2.9.5
│       │   │   └── domusfeed 0.9.1
│       │   └── tauri 2.9.5
│       └── tauri-plugin-http 2.5.4
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
            ├── tauri-utils 2.8.1
            │   ├── tauri-runtime-wry 2.9.3
            │   │   └── tauri 2.9.5
            │   │       ├── tauri-plugin-shell 2.3.3
            │   │       │   └── domusfeed 0.9.1
            │   │       ├── tauri-plugin-opener 2.5.2
            │   │       │   └── domusfeed 0.9.1
            │   │       ├── tauri-plugin-http 2.5.4
            │   │       │   └── domusfeed 0.9.1
            │   │       ├── tauri-plugin-fs 2.4.4
            │   │       │   └── tauri-plugin-http 2.5.4
            │   │       └── domusfeed 0.9.1
            │   ├── tauri-runtime 2.9.2
            │   │   ├── tauri-runtime-wry 2.9.3
            │   │   └── tauri 2.9.5
            │   ├── tauri-plugin-fs 2.4.4
            │   ├── tauri-plugin 2.5.2
            │   │   ├── tauri-plugin-shell 2.3.3
            │   │   ├── tauri-plugin-opener 2.5.2
            │   │   ├── tauri-plugin-http 2.5.4
            │   │   └── tauri-plugin-fs 2.4.4
            │   ├── tauri-macros 2.5.2
            │   │   └── tauri 2.9.5
            │   ├── tauri-codegen 2.5.2
            │   │   └── tauri-macros 2.5.2
            │   ├── tauri-build 2.5.3
            │   │   ├── tauri 2.9.5
            │   │   └── domusfeed 0.9.1
            │   └── tauri 2.9.5
            └── tauri-plugin-http 2.5.4

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
    ├── tauri-utils 2.8.1
    │   ├── tauri-runtime-wry 2.9.3
    │   │   └── tauri 2.9.5
    │   │       ├── tauri-plugin-shell 2.3.3
    │   │       │   └── domusfeed 0.9.1
    │   │       ├── tauri-plugin-opener 2.5.2
    │   │       │   └── domusfeed 0.9.1
    │   │       ├── tauri-plugin-http 2.5.4
    │   │       │   └── domusfeed 0.9.1
    │   │       ├── tauri-plugin-fs 2.4.4
    │   │       │   └── tauri-plugin-http 2.5.4
    │   │       └── domusfeed 0.9.1
    │   ├── tauri-runtime 2.9.2
    │   │   ├── tauri-runtime-wry 2.9.3
    │   │   └── tauri 2.9.5
    │   ├── tauri-plugin-fs 2.4.4
    │   ├── tauri-plugin 2.5.2
    │   │   ├── tauri-plugin-shell 2.3.3
    │   │   ├── tauri-plugin-opener 2.5.2
    │   │   ├── tauri-plugin-http 2.5.4
    │   │   └── tauri-plugin-fs 2.4.4
    │   ├── tauri-macros 2.5.2
    │   │   └── tauri 2.9.5
    │   ├── tauri-codegen 2.5.2
    │   │   └── tauri-macros 2.5.2
    │   ├── tauri-build 2.5.3
    │   │   ├── tauri 2.9.5
    │   │   └── domusfeed 0.9.1
    │   └── tauri 2.9.5
    └── tauri-plugin-http 2.5.4

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
        ├── tauri-utils 2.8.1
        │   ├── tauri-runtime-wry 2.9.3
        │   │   └── tauri 2.9.5
        │   │       ├── tauri-plugin-shell 2.3.3
        │   │       │   └── domusfeed 0.9.1
        │   │       ├── tauri-plugin-opener 2.5.2
        │   │       │   └── domusfeed 0.9.1
        │   │       ├── tauri-plugin-http 2.5.4
        │   │       │   └── domusfeed 0.9.1
        │   │       ├── tauri-plugin-fs 2.4.4
        │   │       │   └── tauri-plugin-http 2.5.4
        │   │       └── domusfeed 0.9.1
        │   ├── tauri-runtime 2.9.2
        │   │   ├── tauri-runtime-wry 2.9.3
        │   │   └── tauri 2.9.5
        │   ├── tauri-plugin-fs 2.4.4
        │   ├── tauri-plugin 2.5.2
        │   │   ├── tauri-plugin-shell 2.3.3
        │   │   ├── tauri-plugin-opener 2.5.2
        │   │   ├── tauri-plugin-http 2.5.4
        │   │   └── tauri-plugin-fs 2.4.4
        │   ├── tauri-macros 2.5.2
        │   │   └── tauri 2.9.5
        │   ├── tauri-codegen 2.5.2
        │   │   └── tauri-macros 2.5.2
        │   ├── tauri-build 2.5.3
        │   │   ├── tauri 2.9.5
        │   │   └── domusfeed 0.9.1
        │   └── tauri 2.9.5
        └── tauri-plugin-http 2.5.4

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
│   │           ├── tauri-plugin-shell 2.3.3
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-opener 2.5.2
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-http 2.5.4
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-fs 2.4.4
│   │           │   └── tauri-plugin-http 2.5.4
│   │           └── domusfeed 0.9.1
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

warning: 18 allowed warnings found
found 0 vulnerabilities

D:\desktop\Develops\02_DomusFeed\DomusFeed\app\src-tauri>cargo audit
    Fetching advisory database from `https://github.com/RustSec/advisory-db.git`
      Loaded 894 security advisories (from C:\Users\kitat\.cargo\advisory-db)
    Updating crates.io index
    Scanning Cargo.lock for vulnerabilities (534 crate dependencies)
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
    │           ├── tauri-plugin-shell 2.3.3
    │           │   └── domusfeed 0.9.1
    │           ├── tauri-plugin-opener 2.5.2
    │           │   └── domusfeed 0.9.1
    │           ├── tauri-plugin-http 2.5.4
    │           │   └── domusfeed 0.9.1
    │           ├── tauri-plugin-fs 2.4.4
    │           │   └── tauri-plugin-http 2.5.4
    │           └── domusfeed 0.9.1
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
│   │   │           ├── tauri-plugin-shell 2.3.3
│   │   │           │   └── domusfeed 0.9.1
│   │   │           ├── tauri-plugin-opener 2.5.2
│   │   │           │   └── domusfeed 0.9.1
│   │   │           ├── tauri-plugin-http 2.5.4
│   │   │           │   └── domusfeed 0.9.1
│   │   │           ├── tauri-plugin-fs 2.4.4
│   │   │           │   └── tauri-plugin-http 2.5.4
│   │   │           └── domusfeed 0.9.1
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
        │           ├── tauri-plugin-shell 2.3.3
        │           │   └── domusfeed 0.9.1
        │           ├── tauri-plugin-opener 2.5.2
        │           │   └── domusfeed 0.9.1
        │           ├── tauri-plugin-http 2.5.4
        │           │   └── domusfeed 0.9.1
        │           ├── tauri-plugin-fs 2.4.4
        │           │   └── tauri-plugin-http 2.5.4
        │           └── domusfeed 0.9.1
        └── tauri-utils 2.8.1
            ├── tauri-runtime-wry 2.9.3
            ├── tauri-runtime 2.9.2
            │   ├── tauri-runtime-wry 2.9.3
            │   └── tauri 2.9.5
            ├── tauri-plugin-fs 2.4.4
            ├── tauri-plugin 2.5.2
            │   ├── tauri-plugin-shell 2.3.3
            │   ├── tauri-plugin-opener 2.5.2
            │   ├── tauri-plugin-http 2.5.4
            │   └── tauri-plugin-fs 2.4.4
            ├── tauri-macros 2.5.2
            │   └── tauri 2.9.5
            ├── tauri-codegen 2.5.2
            │   └── tauri-macros 2.5.2
            ├── tauri-build 2.5.3
            │   ├── tauri 2.9.5
            │   └── domusfeed 0.9.1
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
│   │           ├── tauri-plugin-shell 2.3.3
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-opener 2.5.2
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-http 2.5.4
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-fs 2.4.4
│   │           │   └── tauri-plugin-http 2.5.4
│   │           └── domusfeed 0.9.1
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
│   │           ├── tauri-plugin-shell 2.3.3
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-opener 2.5.2
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-http 2.5.4
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-fs 2.4.4
│   │           │   └── tauri-plugin-http 2.5.4
│   │           └── domusfeed 0.9.1
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
            ├── tauri-plugin-shell 2.3.3
            │   └── domusfeed 0.9.1
            ├── tauri-plugin-opener 2.5.2
            │   └── domusfeed 0.9.1
            ├── tauri-plugin-http 2.5.4
            │   └── domusfeed 0.9.1
            ├── tauri-plugin-fs 2.4.4
            │   └── tauri-plugin-http 2.5.4
            └── domusfeed 0.9.1

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
            ├── tauri-plugin-shell 2.3.3
            │   └── domusfeed 0.9.1
            ├── tauri-plugin-opener 2.5.2
            │   └── domusfeed 0.9.1
            ├── tauri-plugin-http 2.5.4
            │   └── domusfeed 0.9.1
            ├── tauri-plugin-fs 2.4.4
            │   └── tauri-plugin-http 2.5.4
            └── domusfeed 0.9.1

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
│           ├── tauri-plugin-shell 2.3.3
│           │   └── domusfeed 0.9.1
│           ├── tauri-plugin-opener 2.5.2
│           │   └── domusfeed 0.9.1
│           ├── tauri-plugin-http 2.5.4
│           │   └── domusfeed 0.9.1
│           ├── tauri-plugin-fs 2.4.4
│           │   └── tauri-plugin-http 2.5.4
│           └── domusfeed 0.9.1
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
│           ├── tauri-plugin-shell 2.3.3
│           │   └── domusfeed 0.9.1
│           ├── tauri-plugin-opener 2.5.2
│           │   └── domusfeed 0.9.1
│           ├── tauri-plugin-http 2.5.4
│           │   └── domusfeed 0.9.1
│           ├── tauri-plugin-fs 2.4.4
│           │   └── tauri-plugin-http 2.5.4
│           └── domusfeed 0.9.1
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
│   │           ├── tauri-plugin-shell 2.3.3
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-opener 2.5.2
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-http 2.5.4
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-fs 2.4.4
│   │           │   └── tauri-plugin-http 2.5.4
│   │           └── domusfeed 0.9.1
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
    │           ├── tauri-plugin-shell 2.3.3
    │           │   └── domusfeed 0.9.1
    │           ├── tauri-plugin-opener 2.5.2
    │           │   └── domusfeed 0.9.1
    │           ├── tauri-plugin-http 2.5.4
    │           │   └── domusfeed 0.9.1
    │           ├── tauri-plugin-fs 2.4.4
    │           │   └── tauri-plugin-http 2.5.4
    │           └── domusfeed 0.9.1
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
│       │           ├── tauri-plugin-shell 2.3.3
│       │           │   └── domusfeed 0.9.1
│       │           ├── tauri-plugin-opener 2.5.2
│       │           │   └── domusfeed 0.9.1
│       │           ├── tauri-plugin-http 2.5.4
│       │           │   └── domusfeed 0.9.1
│       │           ├── tauri-plugin-fs 2.4.4
│       │           │   └── tauri-plugin-http 2.5.4
│       │           └── domusfeed 0.9.1
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
        ├── tauri-utils 2.8.1
        │   ├── tauri-runtime-wry 2.9.3
        │   │   └── tauri 2.9.5
        │   │       ├── tauri-plugin-shell 2.3.3
        │   │       │   └── domusfeed 0.9.1
        │   │       ├── tauri-plugin-opener 2.5.2
        │   │       │   └── domusfeed 0.9.1
        │   │       ├── tauri-plugin-http 2.5.4
        │   │       │   └── domusfeed 0.9.1
        │   │       ├── tauri-plugin-fs 2.4.4
        │   │       │   └── tauri-plugin-http 2.5.4
        │   │       └── domusfeed 0.9.1
        │   ├── tauri-runtime 2.9.2
        │   │   ├── tauri-runtime-wry 2.9.3
        │   │   └── tauri 2.9.5
        │   ├── tauri-plugin-fs 2.4.4
        │   ├── tauri-plugin 2.5.2
        │   │   ├── tauri-plugin-shell 2.3.3
        │   │   ├── tauri-plugin-opener 2.5.2
        │   │   ├── tauri-plugin-http 2.5.4
        │   │   └── tauri-plugin-fs 2.4.4
        │   ├── tauri-macros 2.5.2
        │   │   └── tauri 2.9.5
        │   ├── tauri-codegen 2.5.2
        │   │   └── tauri-macros 2.5.2
        │   ├── tauri-build 2.5.3
        │   │   ├── tauri 2.9.5
        │   │   └── domusfeed 0.9.1
        │   └── tauri 2.9.5
        └── tauri-plugin-http 2.5.4

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
│       ├── tauri-utils 2.8.1
│       │   ├── tauri-runtime-wry 2.9.3
│       │   │   └── tauri 2.9.5
│       │   │       ├── tauri-plugin-shell 2.3.3
│       │   │       │   └── domusfeed 0.9.1
│       │   │       ├── tauri-plugin-opener 2.5.2
│       │   │       │   └── domusfeed 0.9.1
│       │   │       ├── tauri-plugin-http 2.5.4
│       │   │       │   └── domusfeed 0.9.1
│       │   │       ├── tauri-plugin-fs 2.4.4
│       │   │       │   └── tauri-plugin-http 2.5.4
│       │   │       └── domusfeed 0.9.1
│       │   ├── tauri-runtime 2.9.2
│       │   │   ├── tauri-runtime-wry 2.9.3
│       │   │   └── tauri 2.9.5
│       │   ├── tauri-plugin-fs 2.4.4
│       │   ├── tauri-plugin 2.5.2
│       │   │   ├── tauri-plugin-shell 2.3.3
│       │   │   ├── tauri-plugin-opener 2.5.2
│       │   │   ├── tauri-plugin-http 2.5.4
│       │   │   └── tauri-plugin-fs 2.4.4
│       │   ├── tauri-macros 2.5.2
│       │   │   └── tauri 2.9.5
│       │   ├── tauri-codegen 2.5.2
│       │   │   └── tauri-macros 2.5.2
│       │   ├── tauri-build 2.5.3
│       │   │   ├── tauri 2.9.5
│       │   │   └── domusfeed 0.9.1
│       │   └── tauri 2.9.5
│       └── tauri-plugin-http 2.5.4
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
            ├── tauri-utils 2.8.1
            │   ├── tauri-runtime-wry 2.9.3
            │   │   └── tauri 2.9.5
            │   │       ├── tauri-plugin-shell 2.3.3
            │   │       │   └── domusfeed 0.9.1
            │   │       ├── tauri-plugin-opener 2.5.2
            │   │       │   └── domusfeed 0.9.1
            │   │       ├── tauri-plugin-http 2.5.4
            │   │       │   └── domusfeed 0.9.1
            │   │       ├── tauri-plugin-fs 2.4.4
            │   │       │   └── tauri-plugin-http 2.5.4
            │   │       └── domusfeed 0.9.1
            │   ├── tauri-runtime 2.9.2
            │   │   ├── tauri-runtime-wry 2.9.3
            │   │   └── tauri 2.9.5
            │   ├── tauri-plugin-fs 2.4.4
            │   ├── tauri-plugin 2.5.2
            │   │   ├── tauri-plugin-shell 2.3.3
            │   │   ├── tauri-plugin-opener 2.5.2
            │   │   ├── tauri-plugin-http 2.5.4
            │   │   └── tauri-plugin-fs 2.4.4
            │   ├── tauri-macros 2.5.2
            │   │   └── tauri 2.9.5
            │   ├── tauri-codegen 2.5.2
            │   │   └── tauri-macros 2.5.2
            │   ├── tauri-build 2.5.3
            │   │   ├── tauri 2.9.5
            │   │   └── domusfeed 0.9.1
            │   └── tauri 2.9.5
            └── tauri-plugin-http 2.5.4

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
    ├── tauri-utils 2.8.1
    │   ├── tauri-runtime-wry 2.9.3
    │   │   └── tauri 2.9.5
    │   │       ├── tauri-plugin-shell 2.3.3
    │   │       │   └── domusfeed 0.9.1
    │   │       ├── tauri-plugin-opener 2.5.2
    │   │       │   └── domusfeed 0.9.1
    │   │       ├── tauri-plugin-http 2.5.4
    │   │       │   └── domusfeed 0.9.1
    │   │       ├── tauri-plugin-fs 2.4.4
    │   │       │   └── tauri-plugin-http 2.5.4
    │   │       └── domusfeed 0.9.1
    │   ├── tauri-runtime 2.9.2
    │   │   ├── tauri-runtime-wry 2.9.3
    │   │   └── tauri 2.9.5
    │   ├── tauri-plugin-fs 2.4.4
    │   ├── tauri-plugin 2.5.2
    │   │   ├── tauri-plugin-shell 2.3.3
    │   │   ├── tauri-plugin-opener 2.5.2
    │   │   ├── tauri-plugin-http 2.5.4
    │   │   └── tauri-plugin-fs 2.4.4
    │   ├── tauri-macros 2.5.2
    │   │   └── tauri 2.9.5
    │   ├── tauri-codegen 2.5.2
    │   │   └── tauri-macros 2.5.2
    │   ├── tauri-build 2.5.3
    │   │   ├── tauri 2.9.5
    │   │   └── domusfeed 0.9.1
    │   └── tauri 2.9.5
    └── tauri-plugin-http 2.5.4

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
        ├── tauri-utils 2.8.1
        │   ├── tauri-runtime-wry 2.9.3
        │   │   └── tauri 2.9.5
        │   │       ├── tauri-plugin-shell 2.3.3
        │   │       │   └── domusfeed 0.9.1
        │   │       ├── tauri-plugin-opener 2.5.2
        │   │       │   └── domusfeed 0.9.1
        │   │       ├── tauri-plugin-http 2.5.4
        │   │       │   └── domusfeed 0.9.1
        │   │       ├── tauri-plugin-fs 2.4.4
        │   │       │   └── tauri-plugin-http 2.5.4
        │   │       └── domusfeed 0.9.1
        │   ├── tauri-runtime 2.9.2
        │   │   ├── tauri-runtime-wry 2.9.3
        │   │   └── tauri 2.9.5
        │   ├── tauri-plugin-fs 2.4.4
        │   ├── tauri-plugin 2.5.2
        │   │   ├── tauri-plugin-shell 2.3.3
        │   │   ├── tauri-plugin-opener 2.5.2
        │   │   ├── tauri-plugin-http 2.5.4
        │   │   └── tauri-plugin-fs 2.4.4
        │   ├── tauri-macros 2.5.2
        │   │   └── tauri 2.9.5
        │   ├── tauri-codegen 2.5.2
        │   │   └── tauri-macros 2.5.2
        │   ├── tauri-build 2.5.3
        │   │   ├── tauri 2.9.5
        │   │   └── domusfeed 0.9.1
        │   └── tauri 2.9.5
        └── tauri-plugin-http 2.5.4

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
│   │           ├── tauri-plugin-shell 2.3.3
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-opener 2.5.2
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-http 2.5.4
│   │           │   └── domusfeed 0.9.1
│   │           ├── tauri-plugin-fs 2.4.4
│   │           │   └── tauri-plugin-http 2.5.4
│   │           └── domusfeed 0.9.1
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

warning: 18 allowed warnings found
```