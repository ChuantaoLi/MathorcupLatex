# MathorCup LaTex 模板

基于 Andrew82106 开源的模板 [MathorcupLatexTemplate](https://github.com/Andrew82106/MathorcupLatexTemplate) 修改，编译器选用 XeLaTeX，主要修改：

- 解决了原来模板在 Overleaf 上编译超时的问题：删除 newtxmath, esint, amsfonts, amsthm，保留 amsmath, amssymb；移除 physics, siunitx；删除 zhlipsum, mwe。
- Manuscript.tex ：修复正文文献引用不显示的问题。
- 编译流程修复：已统一为“清理后强制重编译”，用于修复总页码 ?? 、旧缓存不更新等问题。
- 目录显示修复：修复了参考文献在目录中格式不正确的问题。

无论是在 Overleaf 还是本地编译，都需要先将编译器设置为 XeLaTeX，否则会导致编译错误。在本地可以通过以下指令进行编译：

```bash
latexmk -xelatex -synctex=1 -interaction=nonstopmode -file-line-error Manuscript.tex
```

![Manuscript_01](https://lctmemos.oss-cn-beijing.aliyuncs.com/img/Manuscript_01.png)

![Manuscript_02](https://lctmemos.oss-cn-beijing.aliyuncs.com/img/Manuscript_02.png)

![Manuscript_03](https://lctmemos.oss-cn-beijing.aliyuncs.com/img/Manuscript_03.png)
