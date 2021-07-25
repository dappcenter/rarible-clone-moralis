# how to setup frpc
This is the frpc setting.

In fact, `frpc.ini` in the directory `frp_0.37.0_darwin_arm64` is loaded as a configuration file.
## Install frpc on your machine
Go to the [distribution page](https://github.com/fatedier/frp/releases) on github.

Then, choose the appropriate version for your OS.
I'm on a Mac, so select `frp_x.xx.x_darwin_amd64.tar.gz`.
In fact, I installed this:
[frp_0.37.0_darwin_amd64.tar.gz](https://github.com/fatedier/frp/releases/download/v0.37.0/frp_0.37.0_darwin_amd64.tar.gz)

## Modify the `frpc.ini` to fit your Server Instance in Moralis

```
[common]
  server_addr = astudillyj2i.usemoralis.com
  server_port = 7000
  token = kdJeEQlRKb
[ganache]
  type = http
  local_port = 7545
  custom_domains = astudillyj2i.usemoralis.com
```

## Run `./frpc -c frpc.ini` on your frpc directory

In my case, there is the frpc directory at `/Users/mbp/NFT/frp_0.37.0_darwin_arm64`. 
On the directory, run `./frpc -c frpc.ini`.
Then go to the Moralis Server page and refresh the screen, you will see `STATUS: CONNECTED`.

## Restart your Moralis Server

Click `Update and Restart`.
