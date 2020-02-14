# latexindent.pl (LaTeX code formatter)

## Installa requirements
The `latexindent` perl script is already included in e.g. MacTex.
However, it does need some requirements that need to be installed.

Install perl (on osx)
```bash
brew install perl cpanminus
```

Install `perl` requirements
```bash
perl - App::cpanminus
cpanm YAML::Tiny
cpanm File::HomeDir
cpanm Unicode::GCString
cpanm Log::Log4perl
cpanm Log::Dispatch::File
```

## Configuration files

```
.indentconfig.yaml
latexindentSettings.yaml
```

## Run `latexindent`
The default output should silenve (`-s`) the script and tell it to modify
linebreaks (`-m`) in order to wrap text:
```bash
latexindent -s -m main.tex -o main2.tex
```
