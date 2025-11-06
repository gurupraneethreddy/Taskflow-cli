# Quick start

Open power shell
# install deps
npm install

# initialize storage
node taskflow.js init

# add a task (PowerShell)
Set-Content -Path .\task.json -Value '{"command":"echo Hello from TaskFlow","max_retries":2}' -Encoding utf8
Get-Content -Raw .\task.json | node taskflow.js add -

# run the worker (foreground)
node taskflow.js worker
