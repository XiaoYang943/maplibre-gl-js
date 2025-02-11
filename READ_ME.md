## 开发环境搭建
1. 若本地没有node-gyp环境，则安装
   1. 先切换到node-v14.20.0等低版本
   2. 若本地有python环境，最好先卸载掉，且环境变量也删掉
   3. `npm install --global --production windows-build-tools`
      - 安装时在python环境卡住时，[参考解决](https://www.cnblogs.com/lidy5436/p/15182801.html)
2. 切换到node-v20.11.0(大于20版本)
3. `npm install -g node-gyp`
4. `npm install`

### 报错记录
```
npm ERR! code 1
npm ERR! path Z:\source\maplibre-gl-js\node_modules\canvas
npm ERR! command failed
npm ERR! command C:\Windows\system32\cmd.exe /d /s /c prebuild-install -r napi || node-gyp rebuild
npm ERR! Warning: Missing input files:
npm ERR! C:\GTK\bin\zlib1.dll
npm ERR! C:\GTK\bin\libintl-8.dll
npm ERR! C:\GTK\bin\libgthread-2.0-0.dll
npm ERR! C:\GTK\bin\libpango-1.0-0.dll
npm ERR! C:\GTK\bin\libpangocairo-1.0-0.dll
npm ERR! C:\GTK\bin\libgobject-2.0-0.dll
npm ERR! C:\GTK\bin\libexpat-1.dll
npm ERR! C:\GTK\bin\libpng14-14.dll
npm ERR! C:\GTK\bin\libgmodule-2.0-0.dll
npm ERR! C:\GTK\bin\libpangoft2-1.0-0.dll
npm ERR! C:\GTK\bin\libpangowin32-1.0-0.dll
npm ERR! C:\GTK\bin\libcairo-2.dll
npm ERR! C:\GTK\bin\libfontconfig-1.dll
npm ERR! C:\GTK\bin\libfreetype-6.dll
npm ERR! C:\GTK\bin\libglib-2.0-0.dll
npm ERR!
npm ERR!   Backend.cc
npm ERR! Z:\source\maplibre-gl-js\node_modules\canvas\src\backend\Backend.h(3,10): error C1083: 无法打开包括文件: “cairo.h”: No such file or directory [Z:\source\maplibre-gl-js\node_modules\canvas\build\canvas.vcxproj]
npm ERR!   (编译源文件“../src/backend/Backend.cc”)
npm ERR! prebuild-install warn install Request timed out
npm ERR! gyp info it worked if it ends with ok
npm ERR! gyp info using node-gyp@10.0.1
npm ERR! gyp info using node@20.11.0 | win32 | x64
npm ERR! gyp info find Python using Python version 3.12.7 found at "C:\ProgramData\anaconda3\python.exe"
npm ERR! gyp info find VS using VS2022 (17.12.35707.178) found at:
npm ERR! gyp info find VS "C:\Program Files (x86)\Microsoft Visual Studio\2022\BuildTools"
npm ERR! gyp info find VS run with --verbose for detailed information
npm ERR! gyp info spawn C:\ProgramData\anaconda3\python.exe
npm ERR! gyp info spawn args [
npm ERR! gyp info spawn args 'S:\\nvm\\v20.11.0\\node_modules\\npm\\node_modules\\node-gyp\\gyp\\gyp_main.py',
npm ERR! gyp info spawn args 'binding.gyp',
npm ERR! gyp info spawn args '-f',
npm ERR! gyp info spawn args 'msvs',
npm ERR! gyp info spawn args '-I',
npm ERR! gyp info spawn args 'Z:\\source\\maplibre-gl-js\\node_modules\\canvas\\build\\config.gypi',
npm ERR! gyp info spawn args '-I',
npm ERR! gyp info spawn args 'S:\\nvm\\v20.11.0\\node_modules\\npm\\node_modules\\node-gyp\\addon.gypi',
npm ERR! gyp info spawn args '-I',
npm ERR! gyp info spawn args 'C:\\Users\\admin\\AppData\\Local\\node-gyp\\Cache\\20.11.0\\include\\node\\common.gypi',
npm ERR! gyp info spawn args '-Dlibrary=shared_library',
npm ERR! gyp info spawn args '-Dvisibility=default',
npm ERR! gyp info spawn args '-Dnode_root_dir=C:\\Users\\admin\\AppData\\Local\\node-gyp\\Cache\\20.11.0',
npm ERR! gyp info spawn args '-Dnode_gyp_dir=S:\\nvm\\v20.11.0\\node_modules\\npm\\node_modules\\node-gyp',
npm ERR! gyp info spawn args '-Dnode_lib_file=C:\\\\Users\\\\admin\\\\AppData\\\\Local\\\\node-gyp\\\\Cache\\\\20.11.0\\\\<(target_arch)\\\\node.lib',
npm ERR! gyp info spawn args '-Dmodule_root_dir=Z:\\source\\maplibre-gl-js\\node_modules\\canvas',
npm ERR! gyp info spawn args '-Dnode_engine=v8',
npm ERR! gyp info spawn args '--depth=.',
npm ERR! gyp info spawn args '--no-parallel',
npm ERR! gyp info spawn args '--generator-output',
npm ERR! gyp info spawn args 'Z:\\source\\maplibre-gl-js\\node_modules\\canvas\\build',
npm ERR! gyp info spawn args '-Goutput_dir=.'
npm ERR! gyp info spawn args ]
npm ERR! gyp info spawn C:\Program Files (x86)\Microsoft Visual Studio\2022\BuildTools\MSBuild\Current\Bin\MSBuild.exe
npm ERR! gyp info spawn args [
npm ERR! gyp info spawn args 'build\\binding.sln',
npm ERR! gyp info spawn args '/clp:Verbosity=minimal',
npm ERR! gyp info spawn args '/nologo',
npm ERR! gyp info spawn args '/p:Configuration=Release;Platform=x64'
npm ERR! gyp info spawn args ]
npm ERR! gyp ERR! build error
npm ERR! gyp ERR! stack Error: `C:\Program Files (x86)\Microsoft Visual Studio\2022\BuildTools\MSBuild\Current\Bin\MSBuild.exe` failed with exit code: 1
npm ERR! gyp ERR! stack at ChildProcess.<anonymous> (S:\nvm\v20.11.0\node_modules\npm\node_modules\node-gyp\lib\build.js:209:23)
npm ERR! gyp ERR! stack at ChildProcess.emit (node:events:518:28)
npm ERR! gyp ERR! stack at ChildProcess._handle.onexit (node:internal/child_process:294:12)
npm ERR! gyp ERR! System Windows_NT 10.0.22631
npm ERR! gyp ERR! command "C:\\Program Files\\nodejs\\node.exe" "S:\\nvm\\v20.11.0\\node_modules\\npm\\node_modules\\node-gyp\\bin\\node-gyp.js" "rebuild"
npm ERR! gyp ERR! cwd Z:\source\maplibre-gl-js\node_modules\canvas
npm ERR! gyp ERR! node -v v20.11.0
npm ERR! gyp ERR! node-gyp -v v10.0.1
npm ERR! gyp ERR! not ok
```
#### 解决方法
1. package.json中先删除`"canvas": "^3.0.1",`依赖，先安装其他依赖
2. 安装canvas依赖
   1. [参考](https://github.com/Automattic/node-canvas/wiki/Installation:-Windows)
   2. [下载 gtk+-bundle_2.22.1-20101229_win64.zip](https://download.gnome.org/binaries/win64/gtk+/2.22/),解压缩到C:GTK
   3. `npm install canvas@3.0.1 -D`
