ssh into your vm instance, dont use cloudshell they are different
Install code-server - vscode on browser 
```
curl -fsSL https://code-server.dev/install.sh | sh
```

Enable systemctl to start code-server as system process
```
sudo systemctl enable --now code-server@narayanan_kmu
sudo systemctl start code-server@narayanan_kmu
```

Use ssh tunnel to port 8080 (default code-server port) from local machine wherever you got gcloud CLI installed. quickbytes being your VM instance name. keyphr - k8sbit
```
gcloud compute ssh quickbytes --ssh-flag="-L 8080:localhost:8080"
```

Now you can open your local browser and use localhost:8080 to use vscode in browser and edit files under gcloud vm instance directly from browser vscode :thumbsup: .
Added bonus you can just use terminal in VS clode to run all remote commands too.
