# Installation
If you don't have Go installed, download it from <a href="https://go.dev/dl/">here</a> or install it from your package manager. Next:
```
go install github.com/Picocrypt/CLI/picocrypt@latest
```
You should now be able to run `picocrypt` in your terminal. If not, run `export PATH=$PATH:$(go env GOPATH)/bin` and try again.

Alternatively, you can use the prebuilt binaries in Releases.
# Usage
```
C:\Users\Evan>picocrypt
Usage: picocrypt <item1> [<item2> ...]
Items: can be files, folders, or globs
Flags:
  -f    (decryption) attempt to fix corruption
  -k    (decryption) keep output even if corrupted
  -p    (encryption) use paranoid mode
  -r    (encryption) encode with Reed-Solomon
```
## Examples
To encrypt a single file:
```
picocrypt secret.pdf
```
To encrypt all files in the current working directory:
```
picocrypt *
```
To encrypt all PNGs and JPGs with paranoid mode and Reed-Solomon:
```
picocrypt -p -r *.png *.jpg
```
To decrypt a volume:
```
picocrypt volume.pcv
```

## Issues
Report any issues to the main Picocrypt/Picocrypt repository and prefix the title with 'CLI:'.
