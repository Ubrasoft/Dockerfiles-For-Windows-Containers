FROM microsoft/aspnet:4.6.2-windowsservercore-10.0.14393.693

# Install Chocolatey
RUN @powershell -NoProfile -ExecutionPolicy Bypass -Command "$env:ChocolateyUseWindowsCompression='false'; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"

# Install MSBuild
RUN powershell choco install microsoft-build-tools -y

#
RUN powershell choco install dotnet4.6-targetpack -y

# Install Nuget
RUN powershell choco install nuget.commandline --allow-empty-checksums -y

#
RUN powershell nuget install MSBuild.Microsoft.VisualStudio.Web.targets -Version 14.0.0

# Install net framework 4.6.1 Developer Pack
RUN powershell choco install netfx-4.6.1-devpack -y



