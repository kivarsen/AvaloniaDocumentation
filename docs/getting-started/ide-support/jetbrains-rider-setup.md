# JetBrains Rider Setup



1. Download and install the .NET SDK of your choice [Download .NET \(Linux, macOS, and Windows\) \(microsoft.com\)](https://dotnet.microsoft.com/download)

   This is the runtime, development kit \(compiler, etc\) that is used to build Avalonia applications.

2. Install Avalonia Templates

   Run the command `dotnet new -i Avalonia.Templates` from the command prompt on your machine.

   The output will look similar to this.

   ```bash
   $ dotnet new -i Avalonia.Templates
     Determining projects to restore...
     Restored /Users/danwalmsley/.templateengine/dotnetcli/v5.0.200/scratch/restore.csproj (in 706 ms).

   Templates                                     Short Name            Language    Tags
   .....

   Avalonia Resource Dictionary                  avalonia.resource                 ui/xaml/avalonia/avaloniaui
   Avalonia Styles                               avalonia.styles                   ui/xaml/avalonia/avaloniaui

   Examples:
       dotnet new mvc --auth Individual
       dotnet new mstest
       dotnet new --help
       dotnet new avalonia.mvvm --help
   $
   ```

3. Download and install [Rider: The Cross-Platform .NET IDE from JetBrains](https://www.jetbrains.com/rider/)

   Rider will give you the very best development experience available for Avalonia. It is available for Windows, Linux, and macOS.

   Rider supports XAML out of the box. However, if you want to use the XAML previewer, you need the Avalonia plugin.

4. Install the Avalonia Plugin

   Once Rider loads you will see the Welcome Screen. Click the `Configure` dropdown and select `Plugins`.

![rider-welcome](<../../../.gitbook/assets/jetbrains-rider-setup-1-rider-welcome.png>)

A new Preferences Screen will open up. Click the `Settings` icon as shown and select `Manage Plugin Repositories...`

![configure-plugin-repos](<../../../.gitbook/assets/jetbrains-rider-setup-2-configure-plugin-repos.png>)

Click the `+` icon and enter the URL `https://plugins.jetbrains.com/plugins/dev/14839` then click `OK`:

![enter-plugin-repo](<../../../.gitbook/assets/jetbrains-rider-setup-3-enter-plugin-repo.png>)

Now click on the `Marketplace` tab and search for `Avalonia`. Select `AvaloniaRider` and click `Install`; once that's done, click the `Restart IDE` button that appears.

![plugin-install](<../../../.gitbook/assets/jetbrains-rider-setup-4-plugin-install.png>)

Now Rider should be ready to develop Avalonia applications.

