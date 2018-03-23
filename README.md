# Stupid git pre-commit hook for OCaml code

## Usage

- Compile file `ocpChecker.ml`, eg with

```
ocamlopt -o ocp-checker ocpChecker.ml 
```

- Copy `ocp-checker` and `pre-commit` to directory `.git/hooks/` of your
  local cloned git project

- You are done ! The hook with inspect your files before every commit:

 * trailing whitespaces are automatically removed. Modified files
  should be added before you try to commit again

 * a warning will be issued for files with lines larger that 80
   characters. You should fix them before trying to commit again