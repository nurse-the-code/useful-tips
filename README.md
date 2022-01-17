# Intro
This is a list of useful tips for my own personal use. Some of this may or may not be useful to others. If you find it useful, you are free to use this repo in any way permitted by the repo's license. Please note that this repo will be a perpetual work in progress.

# Table of Contents
1. [Initial Python Setup](#initial-python-setup)
2. [Windows Quick Commands](#windows-quick-commands)
3. [Browser Preferences](#browser-preferences)
4. [Git Quick References](#git-quick-references)

# Initial Python Setup
## Windows
<ol>
  <li>Install Git Bash
  <li>Install <a href="https://github.com/pyenv-win/pyenv-win">pyenv-win</a> (windows version of pyenv). Here is what worked for me:
    <ol>
      <li>Use git to clone pyenv-win to home folder: <code>git clone https://github.com/pyenv-win/pyenv-win.git $HOME/.pyenv</code>
      <li>You will have to update Path (Control Panel>System>Advanced System Settings>Environment Variables) with the following variables:
        <ul>
          <li><code>c:\users\USERNAME\.pyenv\pyenv-win\bin</code>
          <li><code>c:\users\USERNAME\.pyenv\pyenv-win\shims</code>
        </ul>
      <li>List versions of Python currently availible to pyenv-win: <code>pyenv install -–list</code> (there is some delay getting newer versions)
      <li>From that list, install your desired Python version (<code>pyenv install 3.9.6</code>)
      <li>To update the shims, run <code>pyenv hash</code> anytime another version of Python is installed
    </ol>
  <li>Install <a href"">Poetry</a>. Here is what worked for me:
    <ol>
      <li>Run <code>curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | pyenv exec python</code>
      <li>You may get one of the two following errors. If you get these, disable the Python.exe and Python3.exe aliases. You can find them by typing "manage app execution aliases into the Windows Search box.
        <ul>
          <li><samp>bash: python: command not found</samp><br><samp>curl: (23) Failed writing body (1354 != 1371)</samp>
          <li><samp>/c/Users/username/AppData/Local/Microsoft/WindowsApps/ Permission Denied</samp>
        </ul>
    </ol>
</ol>

# Windows Quick Commands
* Open task switcher (manages multiple desktops): WIN-TAB
* Change tasks (aka change desktop): 4 finger swipe on laptop
* Open window switcher: ALT-TAB
* Change windows: 3 finger swipe on laptop
* Paste text in terminal: SHIFT-INSERT

## Browser Preferences
### Browser Choice
* Use Chrome for Google apps
* Use Brave for other stuff
* Firefox container feature is also useful
* Vivaldi has useful features that display content from up to 4 different websites side-by-side

# Git Quick References
* Clone a repo from the web: `$ git clone https://github.com/nurse-the-code/useful-tips.git`
* Add all changes in the working tree to the staging area: `$ git add -A` (the `-A` option is case-sensitive)
* Commit work with quick message: `$ git commit -m "describe your commit here`
* Pull a remote to get the most recent updates: `$ git pull <remote-name> <branch-name>` (e.g. `git pull origin main`). Always pull before pushing a repo when working for others.
* Push changes to server: `$ git pull <remote-name> <branch-name>` (e.g. `git pull origin main`). The remote in this example could refer to a remote you forked, or it could refer to the original remote (especially if you originally made the repo).
* Adding the working directory (not necessarily the working tree) to the repo: `$ git add .`. Note: if this is the root directory of the git project, then this command adds everything to the repo (much like `$ git add -A`).
* Directories added to the staging area are always added recursively.
