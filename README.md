# Hardhat-demo

## 安装hardhat

参考链接：[3. 创建新的 Hardhat 项目 | Hardhat | 为专业人士开发的以太坊开发环境 by Nomic Labs (learnblockchain.cn)](https://learnblockchain.cn/docs/hardhat/tutorial/creating-a-new-hardhat-project.html)

> 操作系统：macOS 14.4.1
>
> git version 2.39.3
>
> nvm 0.39.7

### 安装nvm命令：

```sh
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.35.2/install.sh | bash
nvm install 18
nvm use 18
nvm alias default 18
npm install npm --global # Upgrade npm to the latest version
```

### 安装hardhat命令：

们将使用npm 命令行安装**hardhat**。 NPM是一个Node.js软件包管理器和一个JavaScript代码库。

打开一个新终端并运行以下命令：

```shell
mkdir hardhat-tutorial 
cd hardhat-tutorial 
npm init
npm install --save-dev hardhat 
npm install --global hardhat
//在项目中安装 Hardhat，这是一个用于智能合约开发的以太坊开发环境。--save-dev 选项表示 Hardhat 是一个开发时依赖，只在开发过程中使用。
//使用 --global 选项，npm 会将 Hardhat 安装到你的系统中一个全局的位置，这样你可以在任何地方的命令行中直接访问和使用 Hardhat 命令。

```

TIP

安装**Hardhat**将安装一些以太坊JavaScript依赖项，因此请耐心等待。

在安装**Hardhat**的目录下运行：

```shell
npx hardhat
```

使用键盘选择"创建一个新的hardhat.config.js（`Create an empty hardhat.config.js`）" ，然后回车。

在运行**Hardhat**时，它将从当前工作目录开始搜索最接近的`hardhat.config.js`文件。 这个文件通常位于项目的根目录下，一个空的`hardhat.config.js`足以使**Hardhat**正常工作。

### 安装插件

**Hardhat** 不限制选择哪种工具，但是它确实内置了一些插件，所有这些也都可以覆盖。 大多数时候，使用给定工具的方法是将其集成到**Hardhat**中作为插件。

在本教程中，我们将使用插件`@nomicfoundation/hardhat-toolbox`。 通过他们与以太坊进行交互并测试合约。 稍后将解释它们的用法。 要安装它们，请在项目目录中运行：

```shell
npm install --save-dev @nomicfoundation/hardhat-toolbox
```

将高亮行`require("@nomicfoundation/hardhat-toolbox");` 添加到你的`hardhat.config.js`中，如下所示：

```js
require("@nomicfoundation/hardhat-toolbox");

/** @type import('hardhat/config').HardhatUserConfig */
module.exports = {
  solidity: "0.8.24",
};
```

## 编译合约

```shell
npx hardhat compile
```

注意：合约必须放在项目目录下的`contracts`目录才能顺利编译

## 测试

```sh
npx hardhat test
```

注意：必须在项目目录下的`test`中 写了对应的测试js脚本 才能顺利执行





