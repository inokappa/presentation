Mac に markdow2impress をインストールした
--

前提
--

 * Mac OS X 10.7
 * homebrew 導入済み

cpanm をインストール
--

    brew install cpanm

perl の lib パスを設定
--

.bashrc を修正する。

     vi ~/.bashrc

以下を追加する。

    export PERL_CPANM_OPT="--local-lib=~/perl5"
    export PATH=$HOME/perl5/bin:$PATH;
    export PERL5LIB=$HOME/perl5/lib/perl5:$PERL5LIB;

`source .bashrc` にて設定を読みこませる。

必要なモジュールをインストール
--

    cpanm install Data/Section/Simple.pm 
    cpanm install Text/Markdown.pm
    cpanm install Text/Xslate.pm
    cpanm install Path/Class.pm

markdown2impress を git clone する
--

     git clone https://github.com/yoshiki/markdown2impress.git

Markdown ファイルを変換する
--

    ~/bin/markdown2impress.pl hoge.md