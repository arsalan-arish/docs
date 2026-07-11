![img](/assets/pathlib.png)

PurePath is only for logical functionality it cannot actually touch the filesystem  
Path class can touch the filesystem, and
auto detects the operating system and resolves into WindowsPath or PosixPath.
The "/" operator is overloaded to append.
 
Note: Posix paths are case sensitive while windows path are not

**Wildcards for pattern search**
- \* --> all
- *.py --> ending with .py
- test* --> starting with test
- test?.py --> files starting with test and ending with .py
- test?py* -> files starting with test, then any pattern, then contain 'py', then any pattern
- /wildcard --> searches only in this directory
- */wildcard--> searches only in the sub directories
- **/wildcard --> searches recursively in both current and sub directories

**Static methods of Path**
- .home()
- .cwd()
- .resolve()
- Methods of a Path object
- .is_dir()
- .is_file()
- .exists()
- .is_absolute()
- .resolve()
- .as_uri() # returns like a uri to be able to open in a browser
- .match('*.py') # match with a pattern and return True or False
- .relative_to('C://Users') # returns a path object relative to the given path
- .with_name() # returns a new path with name of last element changed
- .with_suffix()
- .with_stem()
- .rename(name) # Actually renames the target

*As a directory:*
- .iter_dir()
- .glob(' *.py ') for normal search inside a dir, but .glob(' **/*.py ') for recursive search inside the dir
- .mkdir(exist_ok=True, parents=True)
- .rmdir()

*As a file:*
- .touch(exist_ok=True)
- .unlink(missing_ok=True)
- .write_text()
- .write_bytes()
- .read_text()
- .read_bytes()
- .open(mode) # Then access the python built in functions like .write()

**Properties of a Path object**
- p.name
- p.stem
- p.suffix # or p.suffixes if it has more than one like .tar.gz and you want separately
- p.parent == p.parents[0]
- p.parents[num]
- p.parts # returns a tuple of path components separated
- p.drive # returns a str of the drive letter if any
- p.root # returns a str of the local or global root if any
- p.anchor = p.drive/p.root depending to the OS
