Challenge:
```
Find the flag in this picture.
```
they gave me the picture

<img src="pico_img.png" />

As the challenge name is ```So Meta``` I looked into the meta data of the image. I used ```exiftool``` this time and here is the output

```
ExifTool Version Number         : 12.08
File Name                       : pico_img.png
Directory                       : .
File Size                       : 106 kB
File Modification Date/Time     : 2020:10:26 14:38:23-04:00
File Access Date/Time           : 2021:01:05 23:49:08-05:00
File Inode Change Date/Time     : 2021:01:05 23:49:08-05:00
File Permissions                : rw-r--r--
File Type                       : PNG
File Type Extension             : png
MIME Type                       : image/png
Image Width                     : 600
Image Height                    : 600
Bit Depth                       : 8
Color Type                      : RGB
Compression                     : Deflate/Inflate
Filter                          : Adaptive
Interlace                       : Noninterlaced
Software                        : Adobe ImageReady
XMP Toolkit                     : Adobe XMP Core 5.3-c011 66.145661, 2012/02/06-14:56:27
Creator Tool                    : Adobe Photoshop CS6 (Windows)
Instance ID                     : xmp.iid:A5566E73B2B811E8BC7F9A4303DF1F9B
Document ID                     : xmp.did:A5566E74B2B811E8BC7F9A4303DF1F9B
Derived From Instance ID        : xmp.iid:A5566E71B2B811E8BC7F9A4303DF1F9B
Derived From Document ID        : xmp.did:A5566E72B2B811E8BC7F9A4303DF1F9B
Warning                         : [minor] Text chunk(s) found after PNG IDAT (may be ignored by some readers)
Artist                          : picoCTF{s0_m3ta_fec06741}
Image Size                      : 600x600
Megapixels                      : 0.360
```

In the Artist Column we have our flag

flag:```picoCTF{s0_m3ta_fec06741}```
