# useful-tips
Reminders to self about various workflows

# Python Setup
## Windows
<ol>
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
          <li><code>python: command not found</code><br><code>curl: (23) Failed writing body (1354 != 1371)</code>
          </li>
          <li>
        </ul>
    </ol>
</ol>

## 
