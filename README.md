# TgStatisticsReferenceChat

统计Tg导出的聊天文件, 并到出到指定文件夹内

这个项目是一个C#控制台应用程序，用于从HTML导出文件中提取和分析聊天记录。目标是识别并列出被其他消息引用或回复的消息。并导出到指定的文件夹下

### 环境

net 6, 请确保你安装了软件所需环境

## 功能

- **HTML解析**：程序读取包含导出聊天记录的HTML文件。
- **消息提取**：提取所有消息及其唯一ID和内容。
- **引用检测**：识别被其他消息引用或回复的消息。
- **输出**：打印出所有被引用的消息，显示其内容和被引用的ID。

## 使用方法

1. **运行程序**：执行控制台应用程序来分析聊天记录并输出相关的消息。

2. **输入你的tg群文件夹地址**：确保你的导出聊天记录的HTML文件（例如`C:\Users\ThinkPad\Downloads\Telegram Desktop\ChatExport_2024-09-01`）。

3. **输出示例**：检查你输入的文件夹里的remark.txt文件 。

> 需要注意的是如果你生成过`remark.txt`文件, 下次生成时, 会将 `remark.txt` 文件进行删除, 如果之前生成的文件对你很重要, 请转移到其他地方

### 示例

例如，程序将提取并识别以下互动：

```csharp
// 被引用的消息
消息ID: message81364
内容: 你叫什么名字

// 回复消息
消息ID: message81372
内容: 张三
回复了: message81364
