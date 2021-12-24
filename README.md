## phplink - a tool to link against a specific PHP version

`phplink` is a `cli` tool to link against a specific PHP version.

### What does that mean?

The purpose of `phplink` is easily allowing switching from one PHP version to another one.

For instance, say we have locally installed PHP versions `7.4`, `8.0` and `8.1` and
our current PHP `cli` is linked/pointed to version `7.4` and we want to easily switch to version `8.1`.
By using `phplink`, one could simply do `sudo phplink 8.1` and everything should work just fine.

[![asciicast](https://asciinema.org/a/5Hw4LRgXX9eCnWT9xMqw01f7x.svg)](https://asciinema.org/a/5Hw4LRgXX9eCnWT9xMqw01f7x)

### Why?

Because who needs Docker anyway?

## Requirements

- GNU bash, version 5+

## Instalation

Below is the easiest way to install this tool:

```bash
git clone https://github.com/chapeupreto/phplink
cd phplink
sudo mv -v phplink /usr/local/bin
chmod +x /usr/local/bin/phplink
```

After those steps, `phplink` is supposed to be available globally on your system. You can check if everything is OK with:

```bash
phplink --help
```

## Usage

`phplink` can be used to link against a specific PHP version by just doing

```bash
sudo phplink <php-version>
```

As an example, assuming PHP `8.0` is already installed, one could do the following in order to link against it:

```bash
sudo phplink 8.0
```

After doing that, the output of `php -v` should display something regarding PHP version 8.0.

One can use the `-l` (`--list`) flag in order to see all available PHP versions:

```bash
phplink -l
```

There is also the `-h` (`--help`) flag that shows a little help about how to use this tool.

## Notes

This tool was tested on `Ubuntu 20.04.2 LTS` where all PHP versions were installed through `apt`.
