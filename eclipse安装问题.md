# eclipse
## jdk15没有jre
 1. 以管理员身份运行cmd
 2. 进入jdk文件目录
 3. 运行命令 'bin\jlink.exe --module-path jmods --add-modules java.desktop --output jre'