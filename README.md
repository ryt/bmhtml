# bmhtml - HTML Bookmark Bar Generator

A tool that creates a portable, optimized html bookmarks bar from your bookmark exports.

#### Install

After downloading, you can call the script directly at `./bmhtml.py`.

You can also create an alias for faster access. If you're using bash, add the following to your aliases:

```console
alias bmhtml='{install}/bmhtml/bmhtml.py'
```

> Note: Depending on your system, aliases may be found in `~/.bashrc`, `~/.bash_aliases` or `~/.bash_profile`. For other shells, use the corresponding config file: e.g. `~/.zshrc`.

#### Usage

There are two types of bookmarks html files that are used with bmhtml:

1. Browser bookmarks html files (i.e. **Netscape bookmarks files**) that are exported from Chrome, Firefox, Opera, etc.
2. **bmhtml** files which are html files that mimic a browser bookmark via JavaScript and CSS functionality.

##### Run on browser exported bookmarks html file. Output name is optional.

If no output name is given, the existing bookmarks html file is converted to a bmhtml file.

> bmhtml.py {input}  

```console
bmhtml.py bookmark_file.html
```

> bmhtml.py {input} {output}

```console
bmhtml.py bookmark_file.html bmhtml_file.html
```

The new `bmhtml_file.html` or custom named file will be created in the same directory as your input file. If output name is specified and the path is different, it will be created in the output path.



##### Show the help manual.

```console
bmhtml.py
bmhtml.py  man|help
```



###### 

<sub><sup>Copyright (C) 2024 Ray Mentose.</sup></sub>

