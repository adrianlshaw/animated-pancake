# XKCD on Remarkable 

This program fetches a random XKCD comic and puts it on your Remarkable's suspend screen.

## Building
```sh
env GOOS=linux GOARCH=arm GOARM=7 go build -o cover.arm
```
## Install
```sh
scp cover.arm remarkable-local:/home/root/
scp cover.service remarkable-local:/etc/systemd/system/
```
```sh
ssh remarkable-local "systemctl daemon-reload; systemctl enable cover; systemctl restart cover; echo done;"
```
