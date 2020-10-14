GT-MOS
============================

More to come!

Makefile
--------

I've added two object files, generated from the psf and sfn fonts. It's a good example of how to
include and reference a binary file in C. I've used the following command to find out the label:

```sh
$ aarch64-elf-readelf -s font_psf.o
        ... output removed for clearity ...
     2: 0000000000000820     0 NOTYPE  GLOBAL DEFAULT    1 _binary_font_psf_end
     3: 0000000000000000     0 NOTYPE  GLOBAL DEFAULT    1 _binary_font_psf_start
     4: 0000000000000820     0 NOTYPE  GLOBAL DEFAULT  ABS _binary_font_psf_size
```

Main
----

Very simple. We set the resolution and display the string. First with PSF, and then with SSFN.
