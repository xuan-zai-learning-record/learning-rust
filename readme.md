前提：

- 本书的使用版本为 `v1.67.1` 。
- 官方文档：[https://doc.rust-lang.org/stable/book/](https://doc.rust-lang.org/stable/book/)

### 开始

##### 安装 Rust

- 在 `Linux` 或 `macOS` 上安装
  ```shell
    $ curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
  ```
  > 注：
  > 该命令下载一个脚本并启动 rustup 工具的安装，该工具将安装最新的 Rust 稳定版本。  
  > 系统可能会提示您输入密码。如果安装成功，将显示以下行：  
  > `Rust is installed now. Great!`
  > 完成上面的步骤，您还需要一个链接器，这是 `Rust` 用来将其编译输出连接到一个文件中的程序。很可能你已经有一个了。如果你得到链接器错误，你应该安装一个 `C 编译器`，它通常包括一个链接器。`C 编译器` 也很有用，因为一些常见的 `Rust` 包依赖于 `C` 代码，需要 `C 编译器`。
  ```shell
    $ xcode-select --install
  ```
  `Linux` 用户通常应该安装 `GCC` 或 `Clang`，根据其发行版的文档。例如，如果你使用 `Ubuntu`，你可以安装 `build-essential` 包。
- 在 `windows` 上安装 `rustup`
  - 根据 https://www.rust-lang.org/tools/install 的指引进行下载。
  - 在安装过程中的某个时候，您会收到一条消息，说明您还需要 `Visual Studio 2013` 或更高版本的 `MSVC` 构建工具。

##### 检查是否完成安装

- 在命令行中输入：`$ rustc --version`
- 当命令行中输出：`rustc x.y.z (abcabcabc yyyy-mm-dd)`，则代表安装成功。
- 如果命令行没有输出这个，则我们需要检查 Rust 是否在 `%PATH%` 系统变量中：
  - cmd：`> echo %PATH%`
  - PowerShell：`> echo $env:Path`
  - Linux 或者 macOs 中：`$ echo $PATH`

##### 更新和卸载：

- 在 `shell` 中运行更新脚本：

```shell
$ rustup update
```

- 在 `shell` 中运行卸载脚本：

```shell
$ rustup self uninstall
```

> 本地文件：
>
> - `Rust` 的安装还包括文档的本地副本，以便您可以脱机阅读。运行 `rustup doc` 在浏览器中打开本地文档。
> - 任何时候，当标准库提供了一个类型或函数，而你不确定它是做什么的或如何使用它时，请使用应用程序编程接口（API）文档来找出答案！
