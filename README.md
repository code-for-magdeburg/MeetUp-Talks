# Meeting repo OKFMD


This repo contains the presentations and meeting minutes of the [OKFMD](https://github.com/code-for-magdeburg/) MeetUps.
It was startet at 2019-07-04.


## dependencies
- texlive
- pandoc

## how to create a presentation as.md?
To create a new presentation please rename the template-presentation.md to %date-presentation.md

```
$ mv presentation.md $(date +%Y-%m-%d)-presentation.md
```
## create the presentation.pdf

In order to create the presentation.pdf you need to use pandoc for convert the markdown to a pdf-file
```
$ pandoc %date-presentation.md --pdf-engine xelatex -t beamer -o $(date +%Y-%m-%d)-presentation.pdf
```

## Hints/Known Problems

If your using macOS with MacTex (texlive for macOS) you need to export your $PATH of texlive

```
$ export PATH=/Library/TeX/texbin:$PATH
```
> *hint:* put this $PATH to you shell config like .bash_profile or .zshrc.
