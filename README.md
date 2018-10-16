# Edit Kubernetes secrets

Usage:

    $ KUBE_EDITOR=/path/to/kube-secret-editor.py kubectl edit secret my-secret

The script will:
- decode the secret values coming from k8s
- call $EDITOR
- encode the values back

## Setup a kubectl plugin

Edit `kubectl-edit_secret` file and set \_DIR\_ to a directory, where you put the python script.

Copy the file to `/usr/local/bin`:

    # cp kubectl-edit_secret /usr/local/bin

Now you can run

    $ kubectl edit-secret my-secret
