# Literate programming example using noweb

Full article: TODO

Install noweb with brew (macOS):

```bash
brew install noweb
```

To generate the files:

```bash
notangle -Rgo.mod hello.nw > go.mod
mkdir -p mypackage
notangle -R'mypackage/mypackage.go' hello.nw > mypackage/mypackage.go
notangle -Rmain.go hello.nw > main.go
noweave -html hello.nw > hello.html
```

To run the program:

```bash
go run main.go
```

To view docs as HTML (on macOS):

```bash
open hello.html
```
