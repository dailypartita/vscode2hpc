## How to use vscode to connect to BGI's HPC supercomputing cluster

- Object Oriented:
Users whose HPC cannot connect to the Internet normally

- Why use vscode instead of putty, mobaxterm and other terminals:
1. vscode can visualize a variety of special files directly on the cluster, such as PDF, xlsx, csv, markdown...
2. vscode can debug python and R code directly on the cluster
3. vscode can replace VIM with the writing method of conventional IDE, and can also automatically complete
......

- vscode local configuration:
1. Download and install vscode
2. Install remote-SSH, Simplified Chinese expansion package

- vscode cluster configuration:
1. Download the corresponding version of vscode-server locally: Since the login node of the cluster cannot be connected to the Internet, you need to download vscode-server manually. Connection: https://update.code.visualstudio.com/commit:${commit_id}/server-linux-x64/stable
2. Upload vscode-server to the cluster, decompress it, rename it, create the .vscode-swever/bin directory in the commonly used software directory, put the renamed directory in the bin directory, and create .vscode- in the home directory Soft link to the server directory
3. Open the remote resource manager of vscode, configure the login node, user name, enter the password and verification code to connect to the cluster
4. Download common extension packages: vscode-pdf, R extension, python extension, office extension, markdown extension
5. Turn off the vscode automatic update function to prevent the need to re-upload vscode-server due to the vscode version update