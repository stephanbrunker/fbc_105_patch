WinAPI Library/Header Patch for FreeBasic 1.05
==============================================

Using the patch: Replace the inc\win\*.bi and lib\win{32|64}\*.dll.a files with the patched ones for your FB architecture (win32 or win64)

## Import Libraries

### patched definition files (source for compiling the import libraries):
* def\comctl32.def: added LoadIconMetric
* def\user32.def: added CalculatePopupWindowPosition

### Compiled new import libraries with from the windows libraries with these definition files:
* Lib\libcomctl32.dll.a
* Lib\libuser32.dll.a

Because of the restriction for binaries on github, these binaries are compressed in the *lib{32|64}.zip* file.

## Headers

* inc\win\commctrl.bi: changed _WIN32_WINNT value for LoadIconMetric
* inc\win\shellapi.bi: changed ShellNotifyIcon
* inc\win\winbase.bi: changed _WIN32_WINNT value for GetQueuedCompletionStatusEx, CancelIoEx, CancelSynchronousIo
* inc\win\winerror.bi: added ERROR_HANDLES_CLOSED, ERROR_OPERATION_ABORTED
* inc\win\winnt.bi: changed brackets for SID Authorities so that they'll work with _SID_IDENTIFIER_AUTHORITY
