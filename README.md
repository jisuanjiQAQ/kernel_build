# MikaKernel 构建器

使用方法：

1. 叉（fork）这个仓库。

2. 编辑 `config.env` 文件：

   | 参数 | 说明 |
   | :---------------------: | ------------------------------------------------- |
   | ANYKERNEL_SOURCE | 您的 Anykernel3 仓库 |
   | ANYKERNEL_SOURCE_BRANCH | 您的 Anykernel3 分支 |
   | KERNEL_SOURCE | 您的内核源码仓库 |
   | KERNEL_SOURCE_BRANCH | 您的内核源码分支 |
   | KERNEL_CONFIG | 您的设备配置 |
   | BUILD_ARGS | 您的内核编译参数，用空格分隔 |

3. 在 "Action->构建 MikaKernel" 中点击 "运行工作流（Run workflow）"

警告：对于 5.4 之前的内核，您应该为内核回溯 LLVM 相关的更改，或者直接将 build-kernel.yml 中定义的工具链降级到 android12-dev 分支，并移除 config.env 中的 "LLVM=1 LLVM_IAS=1" 标志。
