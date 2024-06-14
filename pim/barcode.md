---
title: Barcode/QRcode software
---

# Barcode  and QRcode References
-   Wikipedia: {{< wp "Barcode" >}} look at this article to find cross references to
    each of numerous barcode symbologies.
-   Wikipedia: {{< wp "Barcode reader" >}}, {{< wp "QRcode" >}},
    {{< wp "Rectangular_Micro_QR_Code"   >}},
        {{< wp "Extended_Channel_Interpretation"  >}} (ECI).
-   {{< wp "GS1" >}}  is a not-for-profit, international organization developing and
    maintaining its own standards for barcodes and the corresponding issue company
    prefixes.
-   [ISO/IEC 18004 - QR Code 2005 bar code symbology specification
    ](https://cdn.standards.iteh.ai/samples/43655/42dc967b5d3b4f50905eccdb3f55d96e/ISO-IEC-18004-2006.pdf)
    *This is the old version of the standard, as usual with iso, the standards are not
    public you have to pay for them!*
-   [QR Code Tutorial - Thonky.com](https://www.thonky.com/qr-code-tutorial/).
-   [QRcode.com｜DENSO WAVE](https://www.qrcode.com/en/) is the creator of QRcodes and
    the main source of information regarding QRcodes.
-   [Tech-IT barcode reference
    ](https://www.tec-it.com/download/PDF/Barcode_Reference_EN.pdf) (pdf)
    describe a huge list of linear barcodes, and QR codes.
-   [Barcode Guide
    ](https://barcodeguide.seagullscientific.com/Content/gettingStarted.htm)
-   Data encoding is described in [rMQR encoding - Wikipedia
    ](https://en.wikipedia.org/wiki/Rectangular_Micro_QR_Code#Encoding).
-   [Creating a QR Code step by step
    ](https://www.nayuki.io/page/creating-a-qr-code-step-by-step)
    This JavaScript demo application visualizes in detailed steps, how a text string is
    encoded into a QR Code barcode symbol.
-   [Reading QR codes without a computer!](https://qr.blinry.org/)
-   [Optimal text segmentation for QR Codes
    ](https://www.nayuki.io/page/optimal-text-segmentation-for-qr-codes).
-   [The Ultimate QR Code Size Guide for Optimal Scanning
    ](https://qrcodedynamic.com/blog/qr-code-size/)

## different types of QRcodes:
-   [Model 1 and 2](https://www.qrcode.com/en/codes/model12.html),
-   [Micro QR Code](https://www.qrcode.com/en/codes/microqr.html) that can encode up to 35
    numerals,
-   [rMQR Code](https://www.qrcode.com/en/codes/rmqr.html) of rectangular shape that can
    store up to 361 numerals,

    -   {{< wp "Rectangular_Micro_QR_Code"  "Wikipedia: Rectangular_Micro_QR_Code" >}}.
    -   [ISO/IEC 23941  - Rectangular Micro QR Code (rMQR) bar code symbology
        specification](https://cdn.standards.iteh.ai/samples/77404/e103bf2d1f0d4162b34ca493efdaf9c4/ISO-IEC-23941-2022.pdf)

-   [SQRC](https://www.denso-wave.com/en/system/qr/product/sqrc.html) which contains both
    public data and private data, the private data is accessible only with a private
    scanning device,
-   [Frame QR](https://www.denso-wave.com/en/system/qr/product/frame.html) which add a frame
    with an image.

    The two last codes type are proprietaries.

## QR Code capacity
[Information capacity and versions of QR Code | QRcode.com](https://www.qrcode.com/en/about/version.html) list  capacities of QR Codes
depending of version, error-correcting code, and type of information.

From the previous document we get

For the larger `v40`, `177x177` bits bitmap

| ECC | loss | Data bits | Numeric | Alphanum. | Binary |
|-----|------|-----------|---------|-----------|--------|
| L   | 7%   | 23,648    | 7,089   | 4,296     | 2,953  |
| M   | 15%  | 18,672    | 5,596   | 3,391     | 2,331  |
| Q   | 25%  | 13,328    | 3,993   | 2,420     | 1,663  |
| H   | 30%  | 10,208    | 3,057   | 1,852     | 1,273  |

If we want smaller image, the capacity of course drop down proportionally to the square
of the size of the image square, to achieve the third of
capacity of `v40` we get the `v22` `105x105` bitmap

| ECC | loss | Data bits | Numeric | Alphanum. | Binary |
|-----|------|-----------|---------|-----------|--------|
| L   | 7%   | 8,048     | 2,409   | 1,460     | 1,003  |
| M   | 15%  | 6,256     | 1,872   | 1,134     | 779    |
| Q   | 25%  | 4,544     | 1,358   | 823       | 565    |
| H   | 30%  | 3,536     | 1,056   | 640       | 439    |

The full table of capacity for each version is available in
[qrcode.com - information capacity and versions
](https://www.qrcode.com/en/about/version.html).

The Rectangular Micro QR code has a lesser capacity than model2 QR code, but a bigger
capacity than Micro QR Code.

It may be not appropriate to transmit big data chunk like a detailed vcard *the example
at the end of the page is 397 chars long too big to fit in the larger rMQR*, but for
most use like id string, url, sms, mailto, it can be convenient.

For the larger v32 R17x139 we get:

| ECC | loss | Data bits | Numeric | Alphanum. | Binary |
|-----|------|-----------|---------|-----------|--------|
| M   | 15%  | 1216      | 361     | 219       | 150    |
| H   | 30%  | 608       | 178     | 108       | 174    |

If we want a thinner rectangle v10 R9x139 we have

| ECC | loss | Data bits | Numeric | Alphanum. | Binary |
|-----|------|-----------|---------|-----------|--------|
| M   | 15%  | 504       | 147     | 89        | 68     |
| H   | 30%  | 264       | 75      | 46        | 31     |

With the narrowest square v5 R7x139
| ECC | loss | Data bits | Numeric | Alphanum. | Binary |
|-----|------|-----------|---------|-----------|--------|
| M   | 15%  | 352       | 102     | 62        | 42     |
| H   | 30%  | 192       | 54      | 33        | 22     |

This is only some example with the longer rectangle of 139 modules for a complete table
look at the [qrcode.com rMQR page](https://www.qrcode.com/en/codes/rmqr.html).

Note that to hold an the same payload than R17x139 we have to use a QR code of 49x49,
for R9x139 the equivalent is 33x33, and for R7x139 a QR code of 29x29.

The density of information is similar, but we can use a narrow zone.

# Barcode Software
[QR Code generator library compared to competitors
](https://www.nayuki.io/page/qr-code-generator-library#compared-to-competitors)
give an overview and analysis of code quality of QRcode libraries.

-   [libdmtx](https://github.com/dmtx/libdmtx) (BSD License)
    is open source software for reading and writing Data Matrix
    barcodes on Linux, Unix, OS X, Windows, and mobile devices.
    _dmtxread_ and _dmtxwrite_, provide the official command line
    interface for libdmtx.<br />
    _libdtmx_ and _libdtmx-utils_ are available as Debian/Ubuntu
    packages.
-   [python-qrcode](https://github.com/lincolnloop/python-qrcode) (BSD License)
     a pure Python QR Code generator module. It uses the Python Imaging Library (PIL) to
     allow for the generation of QR Codes. It provides a command line tool to generate
     QR codes and either write these QR codes to a file or do the output as ascii art at
     the console.

     *python3-qrcode* is in Debian.
-   [Qrazybox](https://github.com/merricx/qrazybox/) (MIT license)
     is a web-based application (a toolkit), that used to analyzing and recovering
     damaged QR Code.
-   [QR Code generator library](https://www.nayuki.io/page/qr-code-generator-library)
    (MIT License)
    The library is designed first in Java and then ported to TypeScript, Python, Rust,
    C++, and C.

    User can provide desired setting:
        -   specify minimum and maximum version numbers allowed, then library will
            automatically choose smallest version in the range that fits the data.
        -   specify mask pattern manually, or let the library choose the optimal one;
        -   specify absolute error correction level, or the library use the high est that
            does not increase the version number
        -   create a list of data segments manually and add
            {{< wp "Extended_Channel_Interpretation" "ECI segments" >}}.

    -   [GitHub - nayuki/QR-Code-generator](https://github.com/nayuki/QR-Code-generator)
-   [libqrencode](https://fukuchi.org/works/qrencode/index.html.en) (LGPL-2.1 license)
    is a library for encoding data in a QR Code type 2 symbol and MicroQR, *not yet rMQR
        in 2024*. It has bindings to many programming languages. The library and the
    *qrencode* client are packaged in Debian.
    -   [libqrencode - GitHub](https://github.com/fukuchi/libqrencode)
-   [qrcodescan.in](https://github.com/gokulkrishh/qrcodescan.in) (MIT license)
    QR Code Scanner node
    [progressive web application](https://en.wikipedia.org/wiki/Progressive_web_app).
    -   [qrcodescan online instance](https://qrcodescan.in/)
-
-   [ZBar bar code reader](https://github.com/mchehab/zbar) (LGPL):
    is a software suite for reading bar codes from various sources, such as video
    streams, image files and raw intensity sensors. It supports many popular symbologies
    (types of bar codes) including EAN-13/UPC-A, UPC-E, EAN-8, Code 128, Code 39,
    Interleaved 2 of 5 and QR Code. Presently *in 2024* it can not read micro QR nor rMQR.

    Debian/Ubuntu contains packages _libzbar0_and package to interface QT and GTK,
    python3 bindings,_zbar-tool_ a basic applications for decoding captured bar code
    images and using a video4linux device (e.g. webcam) as a bar code scanner. There are
    also GUI frontends for GTK+-3 and QT5 *zbarcam-qt* and *zbarcam-gtk*
-   <a name="zint"></a>[Zint](https://zint.org.uk/) (GPL and BSD)
    consists of a Qt based GUI, a CLI command line executable and a library.  it is able
    to encode data in over 50 barcode symbologies (types of barcode) one dimensional as
    well as two dimensional, and render them in png, tif, gif, bmp, eps, svg.

   *zint* support many type of QR codes, including Micro QR codes, and rMQR.

    *zint* and *zint-qt* are packaged in Debian.
    -   [Zint  Manual](https://zint.org.uk/manual)
        -   [Zint CLI documentation](https://zint.org.uk/manual/chapter/4)
        -   [zint-qt documantation](https://zint.org.uk/manual/chapter/3)
    -   [GitHub - zint](https://github.com/zint/zint).
-   [ZXing](https://github.com/zxing/zxing) (Apache-2.0 license)
    ("Zebra Crossing") barcode scanning library for Java, Android, is no longer
    developed, but has many offspring, few of them are still alive.
-   <a name="zxing-cpp"></a>[zxing-cpp](https://github.com/zxing-cpp/zxing-cpp)
    (Apache-2.0 license)
    multi-format linear/matrix barcode image processing library implemented in C++.
    It supports many symbologies including QR Codes, MicroQR codes, and rMQR codes.

    Debian provides the library *libzing3* and the client *zing-cpp-tool*.
    Presently *ZxingWriter* cannot write rMQR, but *ZxingReader* can read them.

## rMQR software
-   <a name="qrqrpar"></a>[qrqrpar](https://github.com/Nakanishi123/qrqrpar)
    (BSD-3-Clause license)
    QR code generator supporting rMQR written in rust
-   [rmqrcode-python](https://github.com/OUDON/rmqrcode-python) (MIT License)
    rectangular Micro QR Code (rMQR) Generator in Python
-   {{< iref "#zint" "zint" >}} can also generate rMQR codes.
-   {{< iref "#zxing-cpp" "ZxingWriter" >}} can reat rMQR codes.

## misc barcode software
*few software being presently developed, that I have not tested*
-   [bardecoder](https://github.com/piderman314/bardecoder)
-   [CoBang](https://github.com/piderman314/bardecoder)
-   [qrrs](https://github.com/Lenivaya/qrrs)
-   [qrscan](https://github.com/sayanarijit/qrscan)
-   [QReader](https://github.com/Eric-Canas/QReader)
    a python library to read difficult and tricky QR codes.

# Barcode/QRcode online services
-   [QR Code Generator - Thonky.com](https://www.thonky.com/qrcode/) let you choose the
    error correction level, the mask pattern, and the version *i.e. the size*.
-   [QR code generator library live demo
    ](https://www.nayuki.io/page/qr-code-generator-library#live-demo-javascript)
    allows also to choose EEC, mask pattern, version, border modules, pixel by modules.
    The QR code can be generated as bitmap or SVG.
-   [Qr and rMQR Generator](https://qrqrpardemo.nakanishi.dev/) powered by
    {{< iref "#qrqrpar" "qrqrpar" >}} generate rMQR, micro QR, type 2 QR with a choice
    of color, privileging area, height or width, with round or square shape, choosing
    the margin and pixmap size.
-   [Aspose online code reader and scanner](https://products.aspose.app/barcode/)
    can [generate](https://products.aspose.app/barcode/generate) all type of barcodes,
    QR codes, micro QR codes, rMQR ... in bitmap and svg; the available parameters are
    minimal, you can choose the the size of the image but not the version or module
    number.

    The application can also [recognize](https://products.aspose.app/barcode/recognize)
    any bardode or QRcode, microQR, rMQR image; or
    [scan](https://products.aspose.app/barcode/scanqr) it with your camera.

    An android application *Aspose.BarCode Scan & Create* is also available, but do not
    recognize or scan rMQR codes.

    All the code is [hosted on GitHub](https://github.com/aspose-barcode-cloud/) and
    available under a MIT License.
-   [Oudon Online rMQR Generator](https://rmqr.oudon.xyz/) powered by rmqrcode-python.
    You can choose ECC and maximize size or height.
-   [Tec-It Online BarcodeGenerator](http://barcode.tec-it.com/)
    allows to create among a huge choice of barcode symbologies, or QR codes and
    microQR codes, *no rMQR*. You can not select the version or other parameter of QR
    codes.
-   [QR Code Generator](https://www.qr-code-generator.com/) generate QR code for
    URL, vCard, Text, E-mail, SMS, Wifi, Twitter, Facebook, PDF, MP3, App Stores,
    Images. There is no possibility of tailoring the QR Code version, modules, mask. You
    can only add a frame. No support for other QR Code than classic Type 2.
-   [QRCode Monkey](https://www.qrcode-monkey.com/) a large choice of helpers to
    generate the embedded text. For the QR code a large choice of cosmetics, but no
    choice of version, modules, margin, nor alternative QRCode type. Downloads in bitmap
    or SVG.
-   [QRStuff QR Code Generator](https://www.qrstuff.com/) yet an other online QR code
    generator, seems containing more advertisements.

# Mobile Barcode readers
There are many barcode readers on android and ios, the support for different symbologies
is an important criteria, an other mandatory feature is that the barcode reader don't
launch blindly an application, but let you approve the barcode text before opening the
app.
Other wise you cannot avoid that it launch an expensive phone call or sms or use any of
your app to do an unexpected operation.

For reading rMQR there are only few application the best support seems to be the Denso
Wave application [QRQR](https://www.denso-wave.com/en/system/qr/product/reader.html),
which is available on Android and IOS.


# How to redact a QR code
url:
   ```text
   https://www.example.com
    ```
sms:
    ```text
    SMSTO:+33456789712:some text
    ```

wifi:
    ```text
    WIFI:S:access-point-123;T:WPA;P:somepasswd;;
    ```

email:
    ```text
   mailto:donald.duck@yahoo.com?subject=fly or swim&body=some text
   ```
location:
    ```text
    https://maps.google.com/local?q=48.397244,-4.504738
    ```
vcard:
    ```text
    BEGIN:VCARD
    VERSION:3.0
    FN;CHARSET=UTF-8:M John Doe
    N;CHARSET=UTF-8:Doe;John;;M;
    TEL;TYPE=HOME,VOICE:0043-7252-72720
    TEL;TYPE=WORK,VOICE:0043-5284-84840
    EMAIL:email@example.com
    ORG;CHARSET=UTF-8:Gouvernement
    TITLE;CHARSET=UTF-8:Dictator
    BDAY:20000101
    ADR;CHARSET=UTF-8:24 Champs Élysées\, 75008 Paris\, France
    URL:https://www.example.com
    END:VCARD
    ```

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
