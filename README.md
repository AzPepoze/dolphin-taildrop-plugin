# Taildrop Plugin - Dolphin File Explorer (KIO Support)

This bash script is designed to facilitate file transfers over the [Tailscale](https://tailscale.com/) network on Linux using **Dolphin** (KDE File Manager). It uses modern KIO service menu paths for broad compatibility across different desktop environments (Plasma, Hyprland, GNOME, etc.) where Dolphin is used. It leverages Tailscale's features to interactively choose a device from the network and securely transfer files to that chosen device via the Taildrop service.

## Prerequisites

- [Tailscale](https://tailscale.com/download/linux).
- **Dolphin**.
- `kdialog` installed (usually part of `kdb/kde-cli-tools` or `plasma-desktop`, required for UI popups).
- `zip` installed (for directory transfers).

## Usage

`curl -fsSL https://raw.githubusercontent.com/AzPepoze/dolphin-taildrop-plugin/refs/heads/main/install.sh | bash`

## Features

- **Modern KIO Support:** Uses standard `kio` service menu paths (`~/.local/share/kio/servicemenus/`) for broader compatibility with newer Dolphin versions.
- **Dynamic Device List:** The script dynamically fetches the Tailscale network status to provide an up-to-date list of available devices.
- **Interactive Device Selection:** Users can choose a device interactively from the list for secure file transfers.
- **Real-time Notifications:** The script provides real-time notifications on the success or failure of file transfers.
- **Cleaner UX:** Stripped full paths from notifications for a cleaner look.

## Original Project

Based on the work from [Dolphin-Taildrop-Plugin](https://github.com/Stalloevan/Dolphin-Taildrop-Plugin) by [@Stalloevan](https://github.com/Stalloevan).
