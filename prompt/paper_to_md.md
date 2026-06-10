 使用 **markitdown MCP** 将 xxx.pdf, 这篇PDF 文档解析并转换为 Markdown 格式，具体要求如下：

  1. **使用 markitdown MCP 进行解析**，不要使用 Python 脚本。
  2. **调用方式**：工具的uri参数需使用 `file:/` + **绝对路径**，例如：
     uri: "file:/D:/ai_coding/nested_learning/paper.pdf"
  3. **绝对不要**使用 read 工具直接读取 PDF，会导致解析错误。
  4. **内容完整性**：输出的 Markdown 内容必须严格对应原 PDF：
     - 不得添加原 PDF 中不存在的内容
     - 不得遗漏或删除原 PDF 中已存在的内容
  5. **图片处理**：PDF 中的图片需单独导出并保存在 `【PDF文件名_images】` 文件夹，并在 Markdown 中以相对路径方式引用。
  6. **公式转换**：PDF 中出现的所有公式，必须使用 **LaTeX 格式**写入 Markdown 文档。
  7. **后续处理**：转换完成后，对内容进行学术级别的中文翻译，保持专业术语的准确性。

  转换后的markdown文件（包括图片）保存在 papar/xxx 文件夹下
