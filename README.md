# Spleen

Spleen is a monospaced bitmap font available in 5 sizes:

- 5x8
- 8x16
- 12x24
- 16x32
- 32x64

Each size is provided in the Glyph Bitmap Distribution Format (BDF), and
release tarballs contain the fonts in the following formats: `PCF`, `PSF`
(for the Linux console), and `.dfont` for Macintosh users.

All font sizes contain all ISO/IEC 8859-1 characters, except for the 5x8
version which only contains printable ASCII characters due to character
size constraints.

The font name is a reference to Baudelaire.

## Screenshots

The following screenshots show Spleen 16x32 displaying code and prose.

![Spleen - Hello][1]

![Spleen - L'etranger][2]

ASCII characters for all sizes:

Spleen 5x8:

![Spleen - ASCII characters - 5x8][3]

Spleen 8x16:

![Spleen - ASCII characters - 8x16][4]

Spleen 12x24:

![Spleen - ASCII characters - 12x24][5]

Spleen 16x32:
![Spleen - ASCII characters - 16x32][6]

Spleen 32x64:
![Spleen - ASCII characters - 32x64][7]

## XLFD font names

```
-misc-spleen-medium-r-normal--8-80-72-72-c-50-iso10646-1
-misc-spleen-medium-r-normal--16-160-72-72-c-80-iso10646-1
-misc-spleen-medium-r-normal--24-240-72-72-c-120-iso10646-1
-misc-spleen-medium-r-normal--32-320-72-72-c-160-iso10646-1
-misc-spleen-medium-r-normal--64-640-72-72-c-320-iso10646-1
```

## Packages

Packages are available for the following operating systems:

- [OpenBSD][8]
- [NetBSD][9]
- [FreeBSD][10]
- [Arch Linux][11]
- [Void Linux][12]

## Manual installation

### *BSD and Linux

Clone the repository, convert the files to the Portable Compiled Format
(PCF) using **bdftopcf** and run **mkfontdir** in the directory.

### Mac OS X / macOS

macOS users should use the provided `.dfont` file containing all sizes.

## Usage

### *BSD and Linux

Update the font path to include **Spleen**:

	xset +fp /usr/local/share/fonts/spleen/

Update **.Xdefaults** and add one of the following directives:

	xterm*faceName: spleen:pixelsize=8:antialias=false
	xterm*faceName: spleen:pixelsize=16:antialias=false
	xterm*faceName: spleen:pixelsize=24:antialias=false
	xterm*faceName: spleen:pixelsize=32:antialias=false
	xterm*faceName: spleen:pixelsize=64:antialias=false

Launch **xterm**.

### Linux console

Release tarballs provide PSF files for each size, `setfont` can be used
to load and set the desired font.

### FreeBSD console

The FreeBSD package contains .fnt files which can be loaded using
vidcontrol(1).

For example, to load Spleen 16x32:

	vidcontrol -f /usr/local/share/fonts/spleen/spleen-16x32.fnt

### Mac OS X / macOS

Configure the terminal application to use Spleen, and make sure anti-aliasing
is disabled.

Use the following sizes:

- Spleen 5x8: 8 Pt
- Spleen 8x16: 16 Pt
- Spleen 12x24: 24 Pt
- Spleen 16x32: 32 Pt
- Spleen 32x64: 64 Pt

## License

Spleen is released under the BSD 2-Clause license. See `LICENSE` file for
details.

## Author

Spleen is developed by Frederic Cambus.

- Site: https://www.cambus.net

## Resources

GitHub: https://github.com/fcambus/spleen

[1]: https://www.cambus.net/content/2018/09/spleen-hello.png
[2]: https://www.cambus.net/content/2018/09/spleen-etranger.png
[3]: https://www.cambus.net/files/spleen/spleen-5x8.png
[4]: https://www.cambus.net/files/spleen/spleen-8x16.png
[5]: https://www.cambus.net/files/spleen/spleen-12x24.png
[6]: https://www.cambus.net/files/spleen/spleen-16x32.png
[7]: https://www.cambus.net/files/spleen/spleen-32x64.png
[8]: https://cvsweb.openbsd.org/cgi-bin/cvsweb/ports/fonts/spleen/
[9]: http://pkgsrc.se/fonts/spleen
[10]: https://www.freshports.org/x11-fonts/spleen/
[11]: https://aur.archlinux.org/packages/bdf-spleen/
[12]: https://github.com/void-linux/void-packages/tree/master/srcpkgs/font-spleen
