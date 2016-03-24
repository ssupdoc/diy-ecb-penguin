# Do-It-Yourself ECB Penguin

Create your own version of the famous ECB encrypted version of Tux, the Linux
mascot. This can be used to illustrate issues and weaknesses of using the
electronic codebook (ECB) mode of operation when encrypting data. For
comparison, images can also be encrypted using cipher block chaining (CBC).

Example image taken from
[Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Tux.png):

![tux](https://raw.githubusercontent.com/pakesson/diy-ecb-penguin/master/Tux.png)

ECB:

![tux_ecb](https://raw.githubusercontent.com/pakesson/diy-ecb-penguin/master/Tux_ecb.png)

CBC:

![tux_cbc](https://raw.githubusercontent.com/pakesson/diy-ecb-penguin/master/Tux_cbc.png)

# Requirements

Ubuntu packages:
  * python3-crypto
  * python3-pil

# Usage

```bash
  $ ./encrypt_image.py -h
    usage: encrypt_image.py [-h] (-cbc | -ecb) input_file output_file

    Encrypt images with AES ECB/CBC

    positional arguments:
      input_file   Input file
      output_file  Output file

    optional arguments:
      -h, --help   show this help message and exit
      -cbc, --cbc
      -ecb, --ecb
```

# Examples
Encrypt Tux in ECB mode:

```bash
  $ ./encrypt_image.py --ecb Tux.png Tux_ecb.png
```

Encrypt Tux in CBC mode:

```bash
  $ ./encrypt_image.py --cbc Tux.png Tux_cbc.png
```

