# debug-tips

Here are my tips one debugging C++, especially on GDB.

## the `-femit-class-debug-always` gcc option for handling `incomplete type` issue when debugging
See those discussions: [GDB can not show the type info of wxCommandEvent](https://forums.codeblocks.org/index.php?topic=17953.0) and [Re: [solved] Creating a gdb Pretty-Printer for wxIPV4address](https://forums.wxwidgets.org/viewtopic.php?p=211795#p211795)
When this option is added to the GCC compile option, and you link to the *release* version of a wxWidgets library, you will see the full content of a class such as `wxAuiNotebookEvent`, if this option is not used, you got gdb report `incomplet type` if you would like to see the content of the `event` variable.

![image](https://github.com/asmwarrior/debug-tips/assets/561818/ea6cdbe5-b646-4de0-96f2-b7941638096e)
