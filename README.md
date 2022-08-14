# VSCode Settings

My VSCode settings

## Usage

### Installation

#### Download and Apply Settings

1. Clone this repository.
   - `git clone <repository-url> <vscode-settings-path>`
1. Put a link to the files `keybindings.json` and `settings.json` in the
   directory for VSCode's user settings.
   - The path for this directory under different OS:
     - Linux: `$HOME/.config/Code/User/`
     - Windows: `%APPDATA%\Code\User\`
     - MacOS: `$HOME/Library/Application Support/Code/User/`
   - For example in Linux, execute the commands below.
     - `ln -s <vscode-settings-path>/keybindings.json $HOME/.config/Code/User/`
     - `ln -s <vscode-settings-path>/settings.json $HOME/.config/Code/User/`
   - See [Settings file locations][].
1. Install all extensions listed in the file `installed_extensions.txt`.
   - For example in Linux, execute the command below.
     - `cat <vscode-settings-path>/installed_extensions.txt | xargs -L 1 code --install-extension`

#### Additional Setup

##### Install Monospaced Fonts

Monospaced fonts are used in the settings.

1. Install the required monospaced font if it is not installed.
   - Linux: `sudo apt install fonts-ipafont`

### Update

- `keybindings.json`, `settings.json`
  - If a link to these files are put in the VSCode user settings directory,
    changes made through editting these configuration files through VSCode
    will be reflected in the local reporitory.
  - Just commit and push changes that are made.
- `installed_extensions.txt`
  - It is necessary to explicitly update the file
    `<vscode-settings-path>/installed_extensions.txt`.
  - This can be done by executing the following command.
    - `code --list-extensions`

[Settings file locations]: <https://code.visualstudio.com/docs/getstarted/settings#_settings-file-locations>
