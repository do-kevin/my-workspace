# Electron.js (Abandoned)

## Electron js

- Install `fakeroot` and `dpkg` for Electron forge.
- `apt install mono-runtime`
- Restart WSL by `wsl --shutdown` in powershell for rcedit errors.
- `apt install nuget`
  _Ubuntu 20.04 (Microsoft package feed)_

1.

```
wget https://packages.microsoft.com/config/ubuntu/22.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
rm packages-microsoft-prod.deb
```

2.

```
sudo apt-get update && \
  sudo apt-get install -y dotnet-sdk-7.0
```

3.

```
sudo apt-get update && \
  sudo apt-get install -y aspnetcore-runtime-7.0
```

Note: Could not make executable with Electron & Electron Forge. Stopped at missing `System.IO.Compression` error.
