很多时候，你拿到了一套题，想要在本地测试一下自己能得多少分，这时候就需要评测软件了。

## Cena

Cena 是由刘其帅和李子星使用 Pascal 语言编写的开源评测工具，是流传最广泛的本地评测工具。Cena 最初开源于 Google Code 平台，由于不明原因 Google 删除了 Cena 项目，目前可以在 [Web Archive](https://web.archive.org/web/20131023112258/http://code.google.com/p/cena/) 上找到 Cena 的官网。

Cena 的源代码可以在[这里](https://github.com/billchenchina/cena)找到。

Cena 对权限的限制不是很明确，测试的时候可以读测点 AC QAQ

## Lemon

Lemon 是 zhipeng-jia 写的开源的评测工具，地址在：[zhipeng-jia/project-lemon](https://github.com/zhipeng-jia/project-lemon)。

Ir1d 提供了一份 linux 下编译好的版本在 [Project_lemon](https://github.com/FreestyleOJ/Project_lemon/tree/Built)。

Menci 提供了一份更新的版本在 [Menci/Lemon](https://github.com/Menci/Lemon/)

如果你使用 macOS， 可以自行下载源代码并使用 Qt 来编译一份 Lemon。具体请看 Menci 的 gitHub，和下文中的编译命令还是稍有区别。

**注意** 使用 macLemon 可能会出现内存测试不准确的情况， 这是由于 mac 下没有一些 Linux 的监测工具，而 Lemon-Linux 也没有对于 macOS 的使用优化。

### 自行编译

```bash
sudo apt update
sudo apt install qt5-default build-essential git -y
git clone --depth=1 http://github.com/menci/lemon.git
cd lemon
 可以修改 make 文件来调整 make job 的线程数
sed -i 's/make $/make -j 1 $/g' make
./make
cp Lemon ~
cd ..
```

### 数据格式

首先打开 lemon 选择新建试题，而后打开新建试题的文件夹

题目和数据应该如以下格式所示

```text
├── data
│   ├── gendata.py
│   ├── product
│   │   ├── product100.in
│   │   ├── product100.out
│   │   ├── product10.in
│   │   ├── product10.out
│   │   ├── product11.in
...
```

当所有试题添加完成后，回到 lemon 选择自动添加试题

此时你的题目和数据点应该都显示在 lemon 当中了

## Arbiter

Arbiter 为北京航空航天大学为 NOI Linux 开发的评测工具，现已用于各大 NOI 系列程序设计竞赛的评测。

## CCR-Plus

一款开源的界面好看的评测工具 gitHub 地址 ：[sxyzccr/CCR-Plus](https://github.com/sxyzccr/CCR-Plus)
