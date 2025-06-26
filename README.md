
关于vscode配置、使用的所有，包括R、MATLAB、远程服务器等


## MATLAB

### jupyter编辑MATLAB代码
- 参考：[Run MATLAB in Jupyter Notebooks Using VS Code](https://github.com/user-attachments/assets/97ad3214-0db6-4261-9524-688e2769e38e)
1. 安装 jupyter-matlab-proxy，命令行终端输入：
```
python -m pip install jupyter-matlab-proxy
install-matlab-kernelspec![image](https://github.com/user-attachments/assets/b8357d77-8d2b-497d-a28d-5a6975f3aa4d)
```

2. 打开Powershell（管理员形式），安装MATLAB Package Manager
```
Invoke-WebRequest -Uri https://www.mathworks.com/mpm/win64/mpm -OutFile mpm.exe
```

3. vscode中新建 `.ipynb` 文件 -> 选择 `Jupyter Kernel` -> 选择 `Matlab Kernel`

4. 运行可能遇到的问题

```
Error: Cannot start MATLAB as no licensing information was found. 
Resolution: Set the environment variable MLM_LICENSE_FILE to provide a network license manager, 
or set MWI_USE_EXISTING_LICENSE to True if the installed MATLAB is already licensed. 
See https://github.com/mathworks/matlab-proxy/blob/main/Advanced-Usage.md for more information.
To use Online licensing, start a MATLAB Kernel in a Jupyter notebook and login using the web interface 
shown upon execution of any code.
```
解决方案：

1. 打开环境变量
2. 点击 新建 系统变量 （*****!!!!不是添加路径!!!!!*****）
3. 系统变量添加 MWI_USE_EXISTING_LICENSE，值设置为 True，然后重启电脑

