# mxedeployqt

A little tool to substitute the missing windeployqt in mxe.
It grabs all the qt dependencies your program may need, in order to deploy it.

## Usage

1) grab the mxedeployqt file from this repo and ensure you have python installed on your machine
1) build your project and place all your binaries into a "target dir"
2) run mxedeployqt

### Example usage:

```
mxedeployqt --qtplugins="canbus;iconengines;imageformats;platforminputcontexts;platforms;sqldrivers;styles" --skiplibs="qsqlmysql.dll;qsqlodbc.dll;qsqlpsql.dll;qsqltds.dll" --additionallibs="libwinpthread-1.dll;icudt56.dll;icuin56.dll;icuuc56.dll" --mxepath=~/mxe/usr --qmlrootpath=$PWD/src target/
```

### Available options:

```
usage: mxedeployqt [-h] [--mxepath MXEPATH] [--mxetarget MXETARGET]
                   [--qtplugins QTPLUGINS] [--qmlmodules QMLMODULES]
                   [--skiplibs SKIPLIBS] [--additionallibs ADDITIONALLIBS]
                   [--qmlrootpath QMLROOTPATH]
                   target

positional arguments:
  target

optional arguments:
  -h, --help            show this help message and exit
  --mxepath MXEPATH     path to mxe installation. (Default: /opt/mxe)
  --mxetarget MXETARGET
                        mxe target to use (Default: i686-w64-mingw32.shared)
  --qtplugins QTPLUGINS
                        ; separated list of qt plugins to copy (Default: all
                        Qt plugins)
  --qmlmodules QMLMODULES
                        ; separated list of qml modules to copy. (Default
                        autodetected, if qmlrootpath is supplied and
                        qmlimportscanner is available
  --skiplibs SKIPLIBS   ; separated list of libraries to skip. (Default: None)
  --additionallibs ADDITIONALLIBS
                        ; separated list of libraries to copy. (Default: None)
  --qmlrootpath QMLROOTPATH
                        Path in the source directory to scan qml files for,
                        for using modules
```


## Contributing
1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## Thanks to
1) https://github.com/digitalist/pydeployqt
2) https://github.com/Martchus/

## License
MIT License

Copyright (c) 2018 Dinesh Manajipet

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
