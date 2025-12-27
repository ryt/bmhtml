# bmhtml - HTML Bookmark Bar Generator

A tool that creates a portable, optimized html bookmarks bar from your bookmark exports.

#### Install

After downloading, you can call the script directly at `./bmhtml.py`.

You can also create an alias for faster access. If you're using bash, add the following to your aliases:

```console
alias bmhtml='{install}/bmhtml/bmhtml.py'
```

> *Note: Depending on your system, aliases may be found in `~/.bashrc`, `~/.bash_aliases` or `~/.bash_profile`. For other shells, use the corresponding config file: e.g. `~/.zshrc`.*

In the examples below, the command `bmhtml` is used to refer to `bmhtml.py`.

#### Usage

There are two types of bookmarks html files that are used with bmhtml:

1. Browser bookmarks html files (i.e. **Netscape bookmarks files**) that are exported from Chrome, Firefox, Opera, etc.
2. **bmhtml** files which are generated portable html files that mimic a browser bookmark via JavaScript and CSS functionality.

Both conversion instructions are shown below.

##### 1. Convert browser exported bookmarks html file to bmhtml file.

There are three options the can be used in the `bmhtml` command in this process: 1. **specific output path**, 2. **no output path**, 3. **replace**.

**Option 1:** If an output path is given, the converted file will use the output path.

> bmhtml  {input}  {output}

```console
bmhtml bookmarks.html bookmarks-portable.html
```
...

```
> Writing to file "bookmarks-portable.html" successful.
```

**Option 2:** If no output path is given, the converted portable file will use a `-bm.html` suffix.

> bmhtml {input}

```console
bmhtml bookmarks.html
```
...

```
> Writing to file "bookmarks-bm.html" successful.
```

**Option 3:** If the replace option is used (i.e. `replace` or `r`) as the ouput path, the existing file is converted and replaced with the generated file.

> bmhtml {input} r  
> bmhtml {input} replace

```console
bmhtml bookmarks.html r
bmhtml bookmarks.html replace
```
...

```console
> Replacing file "bookmarks.html" successful.
```

##### 2. Convert bmhtml file to browser based (i.e. Netscape) bookmarks file.

The instructions above can also be used to convert bmhtml files to browser bookmarks files (to import to Chrome, Firefox, Opera, etc).

**Option 1:** Convert and generate to output path: `chrome-import.html`.

```console
bmhtml bookmarks-bm.html chrome-import.html
```
...

```
> Writing to file "chrome-import.html" successful.
```

**Option 2:** No output path, convert & generate using default suffix. When no output path is given, the suffix `-browser.html` is used for the generated file.

```console
bmhtml bookmarks-bm.html
bmhtml bookmarks.html
```
...

```
> Writing to file "bookmarks-browser.html" successful.
```
> *If the input path has a `-bm` suffix, it'll be replaced in the ouput path as well.*

**Option 3:** Convert & replace existing file.

```console
bmhtml bookmarks.html r
bmhtml bookmarks-bm.html replace
bmhtml firefox-favorites.html r
```
...

```
> Replacing file "bookmarks.html" successful.
> Replacing file "bookmarks-bm.html" successful.
> Replacing file "firefox-favorites.html" successful.
```


##### Show the help manual.

```console
bmhtml
bmhtml man|help
```



###### 

<sub><sup>Copyright (C) 2024 Ray Mentose.</sup></sub>

