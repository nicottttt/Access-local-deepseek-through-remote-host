# 在云服务器上部署本地deepseek，通过chatbox公网访问
## 查看GPU配置
```
nvidia-smi
```
图片
要根据自己GPU的配置选择deepseek镜像的版本

可以看到本机配置为4090显卡，24G左右显存，最适配的deepseek镜像为32b

## 安装ollama
图片
根据官网https://ollama.com/download/linux 提示选择自己的操作系统下载，我这里是linux，直接复制官方命令下载
```
curl -fsSL https://ollama.com/install.sh | sh
```
下载完成后会自动识别nvidia驱动，如果没有检测到GPU驱动则会显示CPU-only模式

## 拉取并运行deepseek模型
根据ollama官方model的命令直接拉取
```
ollama pull deepseek-r1:32b
```
也可以直接拉取加运行
```
ollama run deepseek-r1:32b
```
运行成功后输入任意内容开始对话，有返回结果便表示成功部署了deepseek模型

## 绑定本地deepseek服务到本机ip的端口上


## 使用nginx将公网端口映射到本机ip端口上

## 使用不同网段的主机curl命令尝试连接deepseek

## 使用chatbox拉去部署在云服务器的deepseek api
