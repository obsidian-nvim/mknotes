# mknotes

`mknotes` is a bash script for creating Lorem Ipsum Obsidian Markdown notes.

## Installation

```
curl -L -o mknotes https://raw.githubusercontent.com/obsidian-nvim/mknotes/main/mknotes
chmod +x mknotes
```

## Usage

```
NAME
    mknotes - create Lorem Ipsum Obsidian Markdown notes

SYNOPSIS
    mknotes [OPTION..] NOTE_COUNT

OPTIONS:
    -n, --dry-run                                         Print note contents to console instead of writing files
    -h, --help                                            Show this help message
    -f, --file-name FILE_NAME                             Note file name
    -d, --dir-name DIR_NAME                               Notes file directory
    -p, --paragraphs [MAX_PARAGRAPHS[,MIN_PARAGRAPHS]]    Number of paragraphs per note
    -w, --words [MAX_WORDS[,MIN_WORDS]]                   Number of words per paragraph
    -s, --seed SEED                                       Set the random seed for reproducible notes
    -m, --frontmatter                                     Include Obsidian frontmatter metadata header

DESCRIPTION
    Create NOTE_COUNT Obsidian Markdown note files in the current directory or specified directory.

    - Note sizes range randomly from MIN_PARAGRAPHS (0..MAX_PARAGRAPHS, default 0) to MAX_PARAGRAPHS (1..999, default 5).
      Examples: -p 10 (0 to 10 paragraphs per note), -p 20,10 (10 to 20 paragraphs per note).
    - Paragraph sizes range randomly from MIN_WORDS (0..MAX_WORDS, default 25) to MAX_WORDS (1..999, default 150).
      Examples: -w 10 (0 to 10 words per paragraph), -w 20,10 (10 to 20 words per paragraph).
    - Paragraph text is Lorem Ipsum text.
    - FILE_NAME is the note file name prefix (default note).
    - DIR_NAME is the notes file directory (default current directory).
    - SEED is an integer to initialize the random number generator for reproducible output.
    - Note files are named like FILE_NAME-N.md where N is 1,2,..
    - If NOTE_COUNT is 1 then the file name is FILE_NAME.md

```
