# IECapt
**This is an unofficial cloned &amp; tweaked version of IECapt. Source copied from http://iecapt.sourceforge.net/. The original author of IECapt is Björn Höhrmann (bjoern@hoehrmann.de). The documentation was also copied, in case the original site goes down.**

IECapt is a small command-line utility to capture Internet Explorer's rendering of a web page into a BMP, JPEG or PNG image file.

## Samples
Here are some samples of IECapt generated renderings:

 - [Snapshot](sample-images/www.zeldman.com.png) of http://www.zeldman.com
 - [Snapshot](sample-images/msdn.microsoft.com.png) of http://msdn.microsoft.com
 - [Snapshot](sample-images/complexspiral.png) of http://www.meyerweb.com/.../demo.html
 - [Snapshot](sample-images/spiegel.de.png) of http://www.spiegel.de

## Status
"Works for me" :-) The current version is not very verbose, it does not catch or report errors, it has some general limitations and there are some known bugs to be addressed in future versions.

## Requirements
IECapt depends on GDI+. GDI+ is included in Windows XP/2003/Vista/2008. If there is no gdiplus.dll on your system, you can download it from Microsoft and put it into the same directory where IECapt.exe resides.

## Usage
Open a command prompt and ask for help:

```
C:\> IECapt --help
 -----------------------------------------------------------------------------
 Usage: IECapt --url=http://www.example.org/ --out=localfile.png
 -----------------------------------------------------------------------------
  --help                      Print this help page and exit
  --url=<url>                 The URL to capture (http:...|file:...|...)
  --out=<path>                The target file (.png|bmp|jpeg|emf|...)
  --min-width=<int>           Minimal width for the image (default: 800)
  --min-height=<int>          Minimal height for the image (default 800)
  --max-wait=<ms>             Don't wait more than (default: 90000, inf: 0)
  --delay=<ms>                Wait after loading (e.g. for Flash; default: 0)
  --silent                    Whether to surpress some dialogs
 -----------------------------------------------------------------------------
 http://iecapt.sf.net - (c) 2003-2008 Bjoern Hoehrmann - <bjoern@hoehrmann.de>
```

## Tweaks

  - Fixed browser width/height fallback to `--min-width` not working in some circumstances
  - Added a `--min-height` argument
