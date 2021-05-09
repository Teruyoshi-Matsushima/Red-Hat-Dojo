# VirtualBox編

VirtualBoxを使ってMac, Windowsに Red Hat Enterprise Linux8.3 の仮想マシンを作成します。</br>
インストール後、sudo設定・ネットワーク設定・サブスクリプション登録までを実施し、 Red Hat Enterprise Linux8.3 マシンとして利用できる環境を構築します。</br>
前提：VirtualBoxインストール済み、Red Hat Enterprise Linux8.3 インストール用ISOダウンロード済み。</br>

## 仮想マシンのプロファイル作成

お使いの環境にインストールされている「VirtualBox」を起動</br>
<kbd><img src=./images/virtualbox/001.png /></kbd>
</br>

Red Hat Enterprise Linux8.3 の推奨スペック
<kbd><img src=./images/virtualbox/002.png /></kbd>
</br>


<!--
</br>
<kbd><img src=./images/virtualbox/003.png /></kbd>
</br>
-->

Red Hat Enterprise Linux8.3 の推奨スペックに従い、メモリーを1.5GB以上</br>
<kbd><img src=./images/virtualbox/004.png /></kbd>
</br>

Red Hat Enterprise Linux8.3 の推奨スペックに従い、仮想ハードディスサイズを20GB以上</br>
また、この仮想マシンのデータを保存する場所を指定</br>
<kbd><img src=./images/virtualbox/005.png /></kbd>
</br>

Red Hat Enterprise Linux8.3 インストール用ISOを仮想光学ドライブに設定</br>
<kbd><img src=./images/virtualbox/006.png /></kbd>
</br>

ネットワーク設定</br>
<kbd><img src=./images/virtualbox/007.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/008.png /></kbd>
</br>

## Red Hat Enterprise Linux8.3 インストール開始

「Install Red Hat Enterprise Linux 8.3」を選択</br>
<kbd><img src=./images/virtualbox/009.png /></kbd>
</br>

</br>
<kbd><img src=./images/virtualbox/010.png /></kbd>
</br>


このRed Hat Enterprise Linuxで使用する言語を選択</br>
<kbd><img src=./images/virtualbox/011.png /></kbd>
</br>


</br>**インストール概要**</br>
ここでrootのパスワード作成とインストール先デバイスを指定</br>
<kbd><img src=./images/virtualbox/012.png /></kbd>
</br>


まずrootのパスワード作成</br>
<kbd><img src=./images/virtualbox/013.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/014.png /></kbd>
</br>


つぎにインストール先のデバイスを選択するため、赤枠で囲まれたエリアをクリック</br>
<kbd><img src=./images/virtualbox/015.png /></kbd>
</br>


最後に「インストールの開始(R)」をクリック</br>
<kbd><img src=./images/virtualbox/016.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/017.png /></kbd>
</br>


インストール終了後、「システム再起動(R)」をクリック</br>
<kbd><img src=./images/virtualbox/018.png /></kbd>
</br>

## Red Hat Enterprise Linux8.3 起動！

[Red Hat Enterprise Linux (・・・)]にカーソルを当て**enter**</br>
<kbd><img src=./images/virtualbox/019.png /></kbd>
</br>


**初期セットアップ**</br>
<kbd><img src=./images/virtualbox/020.png /></kbd>
</br>


**ライセンス契約への同意**</br>
<kbd><img src=./images/virtualbox/021.png /></kbd>
</br>


**システム**</br>
サブスクリプション登録なのだけど、ネットワークに接続されていない状態では失敗</br>
<kbd><img src=./images/virtualbox/022.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/023.png /></kbd>
</br>


**ユーザーの作成**</br>

<kbd><img src=./images/virtualbox/024.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/025.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/026.png /></kbd>
</br>

## sudo権限設定

</br>
<kbd><img src=./images/virtualbox/027.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/028.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/029.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/030.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/031.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/032.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/033.png /></kbd>
</br>

## 一般ユーザーでログイン

</br>
<kbd><img src=./images/virtualbox/034.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/035.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/036.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/037.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/038.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/039.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/040.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/041.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/042.png /></kbd>
</br>

## ネットワーク設定

</br>
<kbd><img src=./images/virtualbox/043.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/044.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/045.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/046.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/047.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/048.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/049.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/050.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/051.png /></kbd>
</br>



参考(Special thanks!)
@yamada-hakase サン</br>
[Red Hat Developer Programに登録して最大16台までRHELを使おう](https://qiita.com/yamada-hakase/items/dc39d29fda693238d113)

