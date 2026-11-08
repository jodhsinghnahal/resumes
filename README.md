Compile all latex:

```
latexmk -g -pdf -interaction=nonstopmode *.tex
```

Check page counts:

```
for f in *.pdf; do echo -n "$f: "; pdfinfo "$f" | awk '/^Pages:/ {print $2}'; done
```
