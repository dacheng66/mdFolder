#### Liunx部署go项目之交叉编译

1.直接在需要编译的main.go 文件夹下，打开cmd，运行如下命令：

```shell
SET CGO_ENABLED=0

SET GOOS=linux

SET GOARCH=amd64

go build main.go
```

2.得到一个main文件，将main二进制文件上传到服务器，在linux中运行一个二进制的文件的命令:一个点接斜杠

```shell
./main
```

3.修改main二进制文件权限chmod -R 777 main ，直接运行之