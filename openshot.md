# OpenShot

↑ **Parent:** [Video editing software](video-editing-software.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/OpenShot)

[Ubuntu](ubuntu.md) 20.10 crash...:
```
  exceptions:ERROR Unhandled Exception
Traceback (most recent call last):
  File "/usr/bin/openshot-qt", line 11, in <module>
    load_entry_point('openshot-qt==2.5.1', 'gui_scripts', 'openshot-qt')()
  File "/usr/lib/python3/dist-packages/openshot_qt/launch.py", line 97, in main
    app = OpenShotApp(argv)
  File "/usr/lib/python3/dist-packages/openshot_qt/classes/app.py", line 218, in __init__
    from windows.main_window import MainWindow
  File "/usr/lib/python3/dist-packages/openshot_qt/windows/main_window.py", line 45, in <module>
    from windows.views.timeline_webview import TimelineWebView
  File "/usr/lib/python3/dist-packages/openshot_qt/windows/views/timeline_webview.py", line 42, in <module>
    from PyQt5.QtWebKitWidgets import QWebView
ImportError: /usr/lib/x86_64-linux-gnu/libQt5Quick.so.5: undefined symbol: _ZN4QRhi10newSamplerEN11QRhiSampler6FilterES1_S1_NS0_11AddressModeES2_, version Qt_5_PRIVATE_API
```

## ↑ Ancestors (8)

1. [Video editing software](video-editing-software.md)
2. [Video file format](video-file-format.md)
3. [File format](file-format.md)
4. [Computer](computer-split.md)
5. [Information technology](information-technology.md)
6. [Area of technology](area-of-technology.md)
7. [Technology](technology-split.md)
8. [Ciro Santilli's Homepage](split.md)
