# MathorCup LaTex 模板

基于 Andrew82106 开源的模板 [MathorcupLatexTemplate](https://github.com/Andrew82106/MathorcupLatexTemplate) 修改，编译器选用 XeLaTeX，主要修改：

- 解决了原来模板在 Overleaf 上编译超时的问题：删除 newtxmath, esint, amsfonts, amsthm，保留 amsmath, amssymb；移除 physics, siunitx；删除 zhlipsum, mwe。
- Manuscript.tex ：修复正文文献引用不显示的问题。
- 编译流程修复：已统一为“清理后强制重编译”，用于修复总页码 ?? 、旧缓存不更新等问题。
- 目录显示修复：修复了参考文献在目录中格式不正确的问题。

如果 Ctrl+S 无法编译，可以先清除缓存再编译。

清除缓存的运行指令为：

```bash
latexmk -C Manuscript.tex
```

编译的指令为：

```bash
latexmk -gg -pdf Manuscript.tex
```

![Manuscript_01](https://lctmemos.oss-cn-beijing.aliyuncs.com/img/Manuscript_01.png)

![Manuscript_02](https://lctmemos.oss-cn-beijing.aliyuncs.com/img/Manuscript_02.png)

![Manuscript_03](https://lctmemos.oss-cn-beijing.aliyuncs.com/img/Manuscript_03.png)
