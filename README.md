# ConsoleLogonHook-Vista-Style-2

Silght warning, Bitmaps and images were replaced with Reshacker.

Fork of ConsoleLogonHook

>[!WARNING]
>This version uses console logon hook 1.0.7.
>
>Use AuthUX currently, much better.
>
> I'll not put updates into this either.

>[!WARNING]
>This might ruin most login screens.

Console logon hook, but it's Vista style.
Also, if you use %100 or %125 DPI Scaling, the edition goes back to Windows Seven

Import installhooks.reg as trustedinstaller.

1. Move ConsoleLogonHook and ConsoleLogonUI to system32
2. Import installhooks.reg as trustedinstaller.
3. Press CTRL-ALT-DEL and it should work, no reboots required.

Credits goto wiktorwiktor12

Also, for users who don't want to import installhooks.reg

Type the commands at the bottom of the README.md in a trusted installer CMD window.

```cmd
reg add HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsRuntime\ActivatableClassId\Windows.Internal.UI.Logon.Controller.ConsoleBlockedShutdownResolver /v DllPath /t REG_SZ /d %systemroot%\System32\ConsoleLogonHook.dll /f

reg add HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsRuntime\ActivatableClassId\Windows.Internal.UI.Logon.Controller.ConsoleLockScreen /v DllPath /t REG_SZ /d %systemroot%\System32\ConsoleLogonHook.dll /f

reg add HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsRuntime\ActivatableClassId\Windows.Internal.UI.Logon.Controller.ConsoleLogonUX /v DllPath /t REG_SZ /d %systemroot%\System32\ConsoleLogonHook.dll /f

reg add HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsRuntime\ActivatableClassId\Windows.Internal.Shell.PlatformExtensions.ConsoleCredUX /v DllPath /t REG_SZ /d %systemroot%\System32\ConsoleLogonHook.dll /f
```
Then rename windows.ui.logon.dll to something like windows.ui.logon.bak so logonui doesn't overlap.
