<!-- vim: set spell: -->

> Note: This repository is patched for addrindex patches.

monacoin-debian
===============



Japanese
--------

Ubuntuをお使いの方は、下記の手順を踏むことで簡単にお使いのシステムにMonacoinを導入できます。

### 簡単な使い方

端末から以下のコマンドを入力することでPPAリポジトリを有効化してください。

```bash
$ sudo add-apt-repository ppa:visvirial/monacoin
$ sudo apt-get update
```

次に、Monacoinパッケージをインストールします。

* サーバ版の場合
```bash
$ sudo apt-get install monacoind
```
* デスクトップ版の場合
```bash
$ sudo apt-get install monacoin-qt
```

あとは通常の使い方と同様です。

なお、Ubuntuデスクトップ版をお使いの方は、UnityのDashからも起動することができます。

### 詳細

Debianパッケージのビルド方法などの詳細については、下記の英語の説明をお読みください。



English
-------

Monacoin Debian/Ubuntu (or any other debian-derivative distributions) integration files.

This repository provides files needed to debianize monacoin.

This repository is useful only for developers who want to debianize monacoin.
If you want to install monacoin on your computer,
just add the PPA repository (see below).

Installing the PPA repository
-----------------------------

Ubuntu's PPA (personal package archive) is provided [here](https://launchpad.net/~visvirial/+archive/monacoin).
You can add this repository by the following commands.

    $ sudo add-apt-repository ppa:visvirial/monacoin
    $ sudo apt-get update

Then, you can install monacoin-qt [desktop app] and monacoind [server app] using apt-get:

    $ sudo apt-get install monacoin-qt
    $ sudo apt-get install monacoind

Building the debian package
---------------------------

We show the brief instruction for building the monacoin Debian/Ubuntu package.
For details, please refer the manuals of your distribution.

### Download the monacoin's source code.

You can download the monacoin's source code from the following links.

 * Official releases: https://github.com/monacoinproject/monacoin/releases
 * keystore00's releases: https://github.com/keystore00/monacoin/releases

You can clone the development version from repositories alternatively.

    $ git clone https://github.com/monacoinproject/monacoin.git

Or

    $ git clone https://github.com/keystore00/monacoin.git

### Copying debian/\*

Copy the debian directory of this repository into the monacoin source code root directory.

    $ cp -R monacoin-debian/debian monacoin/

### Building the package

Run the following command.

    $ cd monacoin && debuild

You can optionally prepare source tar ball.

Filing a bug
------------

If you find any bugs, or any improvement suggestions, let me know via

 * E-mail: &lt;visvirial[MONA]gmail.com&gt; [replace [MONA] as @]
 * Twitter: [@visvirial](https://twitter.com/visvirial)





