# winserver v0.1

这是一个用于创建Win32服务的包，这个包基于GPLv2发布。
This is a package for create win32 service, it under GPLv2.

安装：
install:

	go get github.com/liuaifu/winservice

示例：
example:

	package main
	
	import (
		"time"
		"winservice"
	)
	
	func main() {
		/**
		* 这个GoService1替换为你创建的服务名，创建服务的命令如下：
		* 注意：等号后的空格必不可少
		* sc.exe create GoService1 binPath= x:\...\test.exe
		* sc start GoService1
		*/
		winservice.Start("GoService1")
		for{
			//在这里做一些事情
			//do something here
			//...
			time.Sleep(20*1e9)
		}
		winservice.Stop()
		return
	}

liuaifu
laf163@gmail.com
2011-3-4
