# _book 
The _book repository is just an HTML build of [Rubyfu repository](https://github.com/rubyfu/RubyFu) to server [Rubyfu gem](https://github.com/rubyfu/RubyfuGem) core contents.

# How it works

- Fork then locally clone the **Rubyfu book** repository

```
git clone https://github.com/[YOURUSER]/RubyFu.git
```

- Generate/Build an HTML
Using [gitbook-cli](https://github.com/GitbookIO/gitbook-cli) application

```
cd Rubyfu
gitbook install
gitbook build 
```
This will generate a folder named `_book` contains HTML version of the book


- Zip then sha512sum the zipped file

```
tar -czf _book.tar.gz _book
sha512sum _book.tar.gz
```

- Fork then locally clone the **_book** repository

```
cd ..
git clone https://github.com/[YOURUSER]/_book.git
```


- Paste the generated HTML book (`_book`) folder in `_book` directory, then push it

```
cp -a Rubyfu/_book _book/
```

- Update **hash.txt** in the forked _book repository from sha512sum outputs, then push it


- Crate a new pull request (PR) to https://github.com/rubyfu/_book/

To report any issue, please refere to [issues](https://github.com/rubyfu/RubyfuGem/issues)
Done!





