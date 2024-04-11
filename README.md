（
安装方法在https://segmentfault.com/q/1010000043256864/a-1020000043256866

Colaboratory：如何在本地机器上安装和使用？

新手上路，请多包涵

Google Colab 非常好用，但我希望我可以完全在本地和离线运行 Colab 笔记本，就像从本地提供的 Jupyter 笔记本一样？

我该怎么做呢？有没有我可以安装的 Colab 软件包？

编辑：之前对该问题的一些回答似乎提供了访问 Google 托管的 Colab 的方法。但这不是我要找的。

我的问题是我如何 pip install colab 这样我就可以在 pip install jupyter 之后像 jupyter 一样在本地运行它。 Colab 包似乎不存在，所以如果我想要它，我该怎么做才能从源代码安装它？

原文由 Saravanabalagi Ramachandran 发布，翻译遵循 CC BY-SA 4.0 许可协议

从这个 Github 链接 看来，Google Colab 可能不是（或保持）开源。

无论我寻找什么，回购协议都 在这里：

 git clone https://github.com/googlecolab/colabtools.git
 
cd colabtools

python setup.py install

然后检查你是否安装了它:)

 pip list | grep colab
 
google-colab                       0.0.1a1

或者，如果你想要一个轮子（将放在 dist 文件夹中），你应该做

python setup.py bdist_wheel
）

# Google Colaboratory

[Colaboratory](https://colab.research.google.com) is a research project created
to help disseminate machine learning education and research. It’s a Jupyter
notebook environment that requires no setup to use. For more information, see
our [FAQ](https://research.google.com/colaboratory/faq.html).

This repository contains the code for the Python libraries available in the
Colab.

## Intended Use

This repo is intended to share code and other resources with the Colab community
and to solicit feedback on the Colab product via
[github issues](https://github.com/googlecolab/colabtools/issues).

**The code published here is not intended for private reuse.**

## Contacting Us

For support or help using Colab, please submit questions tagged with
`google-colaboratory` on
[StackOverflow](https://stackoverflow.com/questions/tagged/google-colaboratory).

For any product issues, you can either
[submit an issue](https://github.com/googlecolab/colabtools/issues) or "Help" ->
"Send Feedback" in Colab.

## Contributing

If you have a problem, or see something that could be improved, please file an
issue. However, we don't have the bandwidth to support review of external
contributions, and we don't want user PRs to languish, so we aren't accepting
any external contributions right now.
