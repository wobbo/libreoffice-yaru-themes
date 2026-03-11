# libreoffice-yaru-themes

LibreOffice Yaru icon themes for **Raspberry Pi OS arm64 GNOME** and **Debian Trixie**.

Debian Trixie does not provide a LibreOffice Yaru icon theme by default on this setup.
This project provides a complete set of **Yaru-based LibreOffice icon themes** matching the GNOME Yaru desktop.

---

## Included icon theme variants

The following LibreOffice icon themes are included:

* Yaru
* Yaru Bark
* Yaru Blue
* Yaru Mate
* Yaru Olive
* Yaru Prussian Green
* Yaru Purple
* Yaru Red

Each theme is provided as a standard LibreOffice icon archive.

---

## Files

The repository contains:

* Individual theme archives (`images_yaru_*.zip`)
* A combined archive containing all themes

Example:

```
libreoffice_yaru-themes_2025-09-23.zip
```

---

## Target system

Tested on:

* Raspberry Pi OS arm64
* Debian Trixie
* GNOME desktop
* LibreOffice GTK3 interface

---

## Installation

Download the combined archive and extract the icon themes into the LibreOffice configuration directory.

```
sudo unzip libreoffice_yaru-themes_2025-09-23.zip -d /usr/lib/libreoffice/share/config/
```

Create dark variants of the themes (LibreOffice expects separate icon archives):

```
cd /usr/lib/libreoffice/share/config/

for f in images_yaru*.zip; do
    [[ "$f" == *_dark.zip ]] && continue
    cp "$f" "${f%.zip}_dark.zip"
done
```

Fix permissions:

```
sudo chmod -R a+rX /usr/lib/libreoffice/share/config/images_yaru*
```

---

## Enable the icon theme

Start LibreOffice and select the icon theme:

```
Tools → Options → View → Icon Theme
```

Choose one of the **Yaru** variants.

---

## Screenshot

Add a screenshot here if desired.

Example location:

```
screenshots/libreoffice-yaru.png
```

---

## Why this project exists

LibreOffice packages in **Debian Trixie / Raspberry Pi OS** do not include a Yaru icon theme, even though the GNOME desktop uses Yaru by default.

This project provides matching icon themes so LibreOffice visually integrates with the Yaru desktop environment.

---

## Author

Ernst Lanser

Forum thread:
- [LibreOffice Yaru Theme for Raspberry Pi OS Trixie (Debian 13)](https://forums.raspberrypi.com/viewtopic.php?t=393058#p2344404)
- [GUIDE: Install GNOME on Raspberry Pi OS Lite](https://forums.raspberrypi.com/viewtopic.php?t=373028#p2233233)
---

## License

MIT License
