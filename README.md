# win10_chaGPT_NEXT_WEB 本地部署教程

前置环境搭建
安装NodeJS
下载地址：https://nodejs.org/en
一路next安装完毕
运行命令 npm -v
查看版本，弹出版本号就证明安装成功了

安装yarn包管理
安装命令 npm install --global yarn
运行命令 yarn -v
查看版本，弹出版本号就证明安装成功了

安装git
请访问Git的官方网站：https://git-scm.com/download/win
下载安装

1. 下载zip压缩包
2. 解压压缩包到自定义文件夹
3. 在ChatGPT-Next-Web-main根目录下按住shift+鼠标右键————在此处打开poweshell窗口
4. 运行命令 yarn install 

 ![win10部署01](https://github.com/mxiaonian/win10_chaGPT_NEXT_WEB/assets/41322284/ae64d378-312a-46d0-bb5a-e724b7607775)


   下载依赖包
   等待进度跑完
6. 运行命令 git init 
   初始化git
   ![win10部署02](https://github.com/mxiaonian/win10_chaGPT_NEXT_WEB/assets/41322284/121e11a5-750e-4cb5-b08f-e2ec9bbc6fdc)
   ![win10部署03](https://github.com/mxiaonian/win10_chaGPT_NEXT_WEB/assets/41322284/fc7f708b-24ac-4766-abd9-b5edbc50669b)

7. 运行命令 yarn add sharp
   添加sharp
   ![win10部署04](https://github.com/mxiaonian/win10_chaGPT_NEXT_WEB/assets/41322284/861ba420-2a61-482b-9478-522394322732)

9. 运行命令 yarn build
    开始构建程序
   ![win10部署05](https://github.com/mxiaonian/win10_chaGPT_NEXT_WEB/assets/41322284/95b041e3-5f04-484a-abd8-aa509115435b)

    出现以下内容表示
    $ cross-env BUILD_MODE=standalone next build
    [Next] build mode standalone
    [Next] build with chunk:  true
    - warn You have enabled experimental feature (forceSwcTransforms) in next.config.mjs.
    - warn Experimental features are not covered by semver, and may cause unexpected or broken application behavior. Use at your own risk.
    这是一个关于Next.js构建过程的输出信息。
    首先，cross-env是一个跨平台设置环境变量的工具，它允许你在不同的操作系统上设置环境变量。在这个命令中，BUILD_MODE=standalone是设置了一个名为BUILD_MODE的环境变量，并将其值设置为standalone。
    接下来，next build是Next.js的命令，用于构建应用程序。在这个命令中，Next.js将使用standalone模式进行构建。
    输出信息中的[Next] build mode standalone表示Next.js正在以独立模式进行构建。[Next] build with chunk: true表示构建过程中启用了代码分割（chunk）功能，这将使得构建后的应用程序可以按需加载代码，提高性能。
    最后，输出信息中的warn部分是关于一些警告信息。它提醒你在next.config.mjs配置文件中启用了一个实验性功能forceSwcTransforms，并告诉你实验性功能可能导致意外或破坏性的应用程序行为。它建议你自行承担风险。如果你不确定是否需要启用该功能，可以考虑在配置文件中禁用它或查阅相关文档以了解更多信息。

    等待构建成功

11. 添加各类环境变量
    （1）在此电脑图标处右击
    
    （2）点击属性
    
    （3）点击高级系统设置
    ![win10部署06](https://github.com/mxiaonian/win10_chaGPT_NEXT_WEB/assets/41322284/e035a0bd-a8ca-4d77-a2ad-1f18ad9a2656)

    （4）点击环境变量
    ![win10部署07](https://github.com/mxiaonian/win10_chaGPT_NEXT_WEB/assets/41322284/3cf5e7b3-b833-4381-82c1-2d798548c896)

    （5）点击新建环境变量
         新建BASE_URL (你的openai API代理地址，可在github上找各个大佬开源的，也可用这个项目作者自己搭建的)
         新建CODE （你的访问密码）
         新建OPENAI_API_KEY (你的key，一般为sk-XXX)
    ![win10部署08](https://github.com/mxiaonian/win10_chaGPT_NEXT_WEB/assets/41322284/06da7a7a-1a7e-410e-a7a2-187501d86c7c)

     (6) 点击确定

8. 在ChatGPT-Next-Web-main根目录下运行命令 yarn start
    ![win10部署09](https://github.com/mxiaonian/win10_chaGPT_NEXT_WEB/assets/41322284/09e833b9-6262-426e-acbd-207360df0b88)

   开启服务
   浏览器进入http://localhost:3000 即可看到你搭建的自己的chatGPT了。
