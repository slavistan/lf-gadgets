# File Dialogs using **lf**

TODO: demo.gif

## Usage

Excerpt from `lf-filedialog --help`:

```
Press return to choose the currently selected file or use the command
'new <FILENAME>' to print a new filename.

lf-filedialog [-t TYPE] [-s STARTDIR] [-o OUTFILE] [-p PROMPT]
		  [-x [TERMARGS]...]

	-t TYPE   Specify what type of object(s) to return. May
		be any combination of the letters f (files),
		d (directories). DEFAULT: fd

	-s STARTDIR   Set the dialog's default working directory.
		DEFAULT: Working directory of the executing shell

	-o OUTFILE   Write output to OUTFILE instead of stdout.
		Can be invoked multiple times. DEFAULT: None

	-p PROMPT   Configure the dialog prompt. DEFAULT: 'Select files(s):'

	-x TERMARGS   Display dialog in a new terminal window using
		the $TERMINAL envvar. Optional TERMARGS may be used to
		pass parameters to the terminal. MUST be the last option
		if present. DEFAULT: None
```

Please take note of the known limitations of interfacing TUIs with shell
scripts: As TUIs (such as `lf`) communicate with the terminal via stdout/stdin
to draw their layouts it is impossible to use return values in the usual manner
(by capturing a commands stdout, e.g. `x=$(date)`). `x=$(lf)` will do nothing
for the same reason `x=$(htop)` will not display its TUI.

Thus, when using `lf-filedialog` inside shell scripts you may use the `-x`
option which will display the dialog inside a new terminal and allows to
capture the script's stdout:

```
myfile="$(lf-filedialog -p "Select a file:" -t f -x)"
echo "$myfile"
```

Alternatively, to display the dialog in the same terminal use the `-o` option
to write the selection to a file:

```
lf-filedialog -p "Select a file:" -t f -o /tmp/selection
myfile="$(cat /tmp/selection)"
echo "$myfile"
```


## Installation

Requires `zsh`.

```
# copy scripts into $PATH
sudo cp lf-filedialog /usr/local/bin
sudo chmod 755 /usr/local/bin/lf-filedialog

# copy config file
mkdir -p "${XDG_CONFIG_HOME:-$HOME/.config}/lf-filedialog"
cp lfrc-filedialog "${XDG_CONFIG_HOME:-$HOME/.config}/lf-filedialog"
```

To uninstall simply delete the files.
