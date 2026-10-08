FEREZ Remote Desktop — Logo update

1. Close the source editor if open.
2. Extract ALL ZIP contents into your existing project folder:
   C:\projects\FEREZ_Remote_Desktop_Source_Preview
3. Accept replacement of the included files. Do not delete your project.
4. In CMD in that project folder:
   git add .gitignore flutter/lib/common.dart flutter/assets/logo.png flutter/assets/icon.png flutter/windows/runner/resources/app_icon.ico res/icon.ico res/icon.png res/tray-icon.ico
   git commit -m "Apply FEREZ robot logo"
   git push
5. GitHub -> Actions -> FEREZ Windows Preview -> Run workflow -> main.
6. After success, download the new FEREZ preview artifact and use the new EXE.

Uses the image supplied by the user on 2026-10-08. The home image preserves
its full composition. Windows icons fit both faces with padding, without
cropping. The source code branding image area is increased from 60 to 120 px.
.gitignore explicitly includes the branding PNGs to avoid missing assets.
Upstream attribution and authentication behaviour are unchanged.

Validated asset formats, ICO sizes and git diff formatting locally.
Windows compilation and runtime appearance require the next build/test.
Based on repository commit ca07c2f.
