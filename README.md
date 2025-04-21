# xshell：使Rust成为更好的工具

xshell 提供了一组跨平台实用程序，用于编写符合人体工程学的“bash”脚本。通过使用 xshell，您可以轻松地在 Rust 中编写类似于 bash 脚本的命令行工具。

## 功能介绍

- **命令执行**：使用 `cmd!` 宏可以方便地执行命令并读取输出。例如：
  ```rust
    let name = "Julia";
      let output = cmd!("echo hello {name}!").read()?;
        assert_eq!(output, "hello Julia!");
          ```

          - **文件读取**：使用 `read_file` 函数可以读取文件内容，如果文件不存在，则会返回错误信息。例如：
            ```rust
              let err = read_file("feeling-lucky.txt").unwrap_err();
                assert_eq!(
                      err.to_string(),
                            "`feeling-lucky.txt`: no such file or directory (os error 2)"
                              );
                                ```

                                ## 使用示例

                                以下是一个简单的示例，展示了如何使用 xshell 执行命令并读取文件内容：

                                ```rust
                                use xshell::{cmd, read_file};

                                fn main() -> Result<(), Box<dyn std::error::Error>> {
                                    let name = "Julia";
                                        let output = cmd!("echo hello {name}!").read()?;
                                            assert_eq!(output, "hello Julia!");

                                                let err = read_file("feeling-lucky.txt").unwrap_err();
                                                    assert_eq!(
                                                            err.to_string(),
                                                                    "`feeling-lucky.txt`: no such file or directory (os error 2)"
                                                                        );

                                                                            Ok(())
                                                                            }
                                                                            ```

                                                                            ## 安装与使用

                                                                            要使用 xshell，您需要在 Cargo.toml 文件中添加依赖项：

                                                                            ```toml
                                                                            [dependencies]
                                                                            xshell = "0.1"
                                                                            ```

                                                                            然后，您可以在 Rust 项目中导入并使用 xshell 提供的功能。

                                                                            ## 贡献

                                                                            欢迎贡献代码、报告问题或提出改进建议。请通过 GitHub 仓库提交您的贡献。

                                                                            ## 许可证

                                                                            本项目采用 MIT 许可证。有关更多信息，请参阅 LICENSE 文件。

                                                                            ## 下载链接
                                                                            [xshell使Rust成为更好的工具](https://pan.quark.cn/s/1479ad48f051) 

                                                                            (备用: [备用下载](https://pan.baidu.com/s/1wczByICoPPB3R6lmkF6wDA?pwd=1234))
