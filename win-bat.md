# BAT 脚本开启新 CMD 窗口指南

# 在 `.bat` 脚本中开启新的 cmd 窗口，主要使用 `start` 命令。搭配 `/k` 或 `/c` 参数可以控制窗口执行完命令后是否自动关闭。

## 1. 基础打开方式

* **打开空白窗口**：
  ```bat
  start cmd
  ```
* **执行命令后保持打开**（常用，便于查看结果）：
  ```bat
  start cmd /k "echo Hello"
  ```
* **执行命令后自动关闭**：
  ```bat
  start cmd /c "echo Hello"
  ```

## 2. 进阶使用技巧

* **自定义窗口标题**：
  ```bat
  start "我的新窗口" cmd
  ```
  *(注意：第一个双引号内的文本会被识别为窗口标题)*

* **切换到指定工作目录**：
  ```bat
  start cmd /k "cd /d D:\workspace && dir"
  ```

* **在一个新窗口中执行多条命令**（使用 `&&` 连接）：
  ```bat
  start cmd /k "echo 正在启动服务 && cd /d D:\server && start_server.exe"
  ```
