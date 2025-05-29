# MiniOS APT Repository
[![MiniOS](images/minios.png)](https://minios.dev)

[MiniOS APT Repository on GitHub](https://github.com/minios-linux/ftp)

## Installation
For the buster, bookworm, trixie, sid, execute the following commands:

```bash
curl http:/ftp.minios.dev/debian/minios-linux.asc | sudo gpg --dearmor > /etc/apt/trusted.gpg.d/minios-linux.gpg

# Determine the distribution
distro=$(lsb_release -cs)

# Add the source depending on the distribution
echo "deb http:/ftp.minios.dev/debian $distro main contrib non-free" | sudo tee /etc/apt/sources.list.d/minios-linux.list
echo "deb http:/ftp.minios.dev/debian generic main contrib non-free" | sudo tee -a /etc/apt/sources.list.d/minios-linux.list
```
