# fields -- display the header line of a TSV/CSV and number the columns

Last updated: Oct. 30, 2018

## Purpose

If you enjoy slicing and dicing structured data on the command line, using
tools such as `awk` and `cut`, perhaps you've run into the small-but-real
difficulty of figuring out which column number corresponds to the field you
want. This is a simple tool to help.

## Installation

Download and locate somewhere in your $PATH. Other than `bash` it uses only
standard POSIX tools (specifically `grep`, `tr`, and `nl`).

## Usage

Just call `fields` and provide the name of the CSV/TSV file (with a header
on the first line containing column names) on the command line.  Specify a
delimiter if you want, or it will try to guess. Output consists of a
numbered list of the fields it detects. These numbers can then be used to
specify fields for `awk` or `cut` (etc).

To specify a delimiter:

- `-p` specifies pipe-delimited (the "|" character)
- `-t` specifies TAB-delimited
- `-c` specifies comma-delimited (note, no attempt is made to handle complicated CSV files with commas inside quoted fields)
- `-s` specifies space-delimited

Invoking `fields` without any command line options should produce a help
message.

## Caveats

Developed on a Debian Linux system. Suggestions to enhance portability to
other Unix-like systems would be welcomed.
