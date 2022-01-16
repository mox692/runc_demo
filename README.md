ref: https://www.youtube.com/watch?v=xKRcM_Rmwrk

### tool install

skopeoのinstall(ubuntu 18.04)
```
$ echo "deb https://download.opensuse.org/repositories/devel:/kubic:/libcontainers:/stable/xUbuntu_18.04/ /" | $ sudo tee /etc/apt/sources.list.d/devel:kubic:libcontainers:stable.list
$ curl -L "https://download.opensuse.org/repositories/devel:/kubic:/libcontainers:/stable/xUbuntu_18.04/Release.key" | sudo apt-key add -
$ sudo apt-get update
$ sudo apt-get -y upgrade
$ sudo apt-get -y skopeo
```

umociのinstall
```
$ git clone https://github.com/opencontainers/umoci && cd umoci && make build
```

umociを使ったimageのruntime bundle
```
$ sudo umoci unpack --image alpine:latest alpine-bundle
```
