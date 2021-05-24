# VirtualBox編

VirtualBoxを使ってMac, Windowsに Red Hat Enterprise Linux8.3 の仮想マシンを作成します。</br>
インストール後、sudo設定・ネットワーク設定・サブスクリプション登録までを実施し、 Red Hat Enterprise Linux8.3 マシンとして利用できる環境を構築します。</br>
前提：VirtualBoxインストール済み、Red Hat Enterprise Linux8.3 インストール用ISOダウンロード済み。</br>

## 仮想マシンのプロファイル作成

Red Hat Enterprise Linux8.3 の推奨スペック
<kbd><img src=./images/virtualbox/002.png /></kbd>
</br>

お使いの環境にインストールされている「VirtualBox」を起動</br>
<kbd><img src=./images/virtualbox/001.png /></kbd>
</br>


<!--
</br>
<kbd><img src=./images/virtualbox/003.png /></kbd>
</br>
-->

Red Hat Enterprise Linux8.3 の推奨スペックに従い、メモリーを1.5GB以上</br>
<kbd><img src=./images/virtualbox/101.png /></kbd>
</br>

Red Hat Enterprise Linux8.3 の推奨スペックに従い、仮想ハードディスサイズを20GB以上</br>
また、この仮想マシンのデータを保存する場所を指定</br>
<kbd><img src=./images/virtualbox/102.png /></kbd>
</br>

Red Hat Enterprise Linux8.3 インストール用ISOを仮想光学ドライブに設定</br>
<kbd><img src=./images/virtualbox/006.png /></kbd>
</br>

ネットワーク設定</br>
<kbd><img src=./images/virtualbox/007.png /></kbd>
</br>


## Red Hat Enterprise Linux8.3 インストール開始
*はじめに、ここからVirtualBox*の中で作業していきますが、VirtualBoxから抜けたい場合は左*command*キーを押せばOK

</br>
<kbd><img src=./images/virtualbox/008.png /></kbd>
</br>


「Install Red Hat Enterprise Linux 8.3」を選択</br>
<kbd><img src=./images/virtualbox/103.png /> <img src=./images/virtualbox/009.png /></kbd>
</br>

<!--
</br>
<kbd><img src=./images/virtualbox/010.png /></kbd>
</br>
-->

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


</br>
<kbd><img src=./images/virtualbox/022.png /></kbd>
</br>


**システム**</br>
サブスクリプション登録なのだけど、ネットワークに接続されていない状態では失敗</br>
<kbd><img src=./images/virtualbox/023.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/024.png /></kbd>
</br>


**ユーザーの作成**</br>
一般ユーザーとして**testuser**を作成</br>
<kbd><img src=./images/virtualbox/025.png /></kbd>
</br>


「設定の完了(F)」をクリック</br>
<kbd><img src=./images/virtualbox/026.png /></kbd>
</br>

## sudo権限設定

rootでログインするため、「アカウントが見つかりませんか？」をクリック</br>
<kbd><img src=./images/virtualbox/027.png /></kbd>
</br>


ユーザー名:root とし「次へ」</br>
<kbd><img src=./images/virtualbox/028.png /></kbd>
</br>


root のパスワードを入力し「サインイン」</br>
<kbd><img src=./images/virtualbox/029.png /></kbd>
</br>


ターミナルを起動するため、左上の[アクティビティ]－[端末]をクリック</br>
<kbd><img src=./images/virtualbox/030.png /></kbd>
</br>


sudo設定のためターミナルにvisudoと入力</br>
<kbd><img src=./images/virtualbox/031.png /></kbd>
</br>


:101と打って101行目に移動</br>
ちなみに行番号表示は:set number</br>
<kbd><img src=./images/virtualbox/032.png /></kbd>
</br>


キーボードのiを押して編集モードへ移行。101行目にtestuser ALL=(ALL) ALLと入力</br>
キーボードの[ESC]を押して編集モードを終了し、さらにviを保存＆終了するために:wqを入力</br>
<kbd><img src=./images/virtualbox/033.png /></kbd>
</br>

## 一般ユーザーでログイン

インストールの途中で作成した一般ユーザー**testuser**でログイン</br>
<kbd><img src=./images/virtualbox/034.png /></kbd>
</br>


Welcome!画面でこのＯＳで利用する言語を指定</br>
<kbd><img src=./images/virtualbox/036.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/037.png /></kbd>
</br>


位置情報サービスに関してオン/オフを決定</br>
<kbd><img src=./images/virtualbox/038.png /></kbd>
</br>


「オンラインアカウントへの接続」ですが、まだネットワークへの接続もできていないので「スキップ」</br>
<kbd><img src=./images/virtualbox/039.png /></kbd>
</br>


使用準備完了！「Red Hat Enterprise Linuxを使い始める(S)」をクリック</br>
<kbd><img src=./images/virtualbox/040.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/041.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/042.png /></kbd>
</br>

## ネットワーク設定

ターミナルを起動するため、左上の[アクティビティ]－[端末]をクリック</br>
<kbd><img src=./images/virtualbox/052.png /></kbd>
</br>


ネットワークへの接続状況を確認するためip aとターミナルへ入力</br>
赤枠で示すように「eth0」ネットワークへは接続されていないようです。</br>
<kbd><img src=./images/virtualbox/053.png /></kbd>
</br>

仮想マシンのプロファイル作成時にネットワーク設定の中でNATとホストオンリーアダプターを設定したので再度内容を確認</br>
それぞれのデバイス名を明らかにしましょう</br>
まず、アダプター１のNAT設定から</br>
真ん中くらいにある「高度」をクリックし詳細を表示してください</br>
そのMACアドレスに注目し、その下４桁くらいをメモしておいてください</br>
NATについては、アドレス変換しているだけなので仮想NICは不要のようです</br>
<kbd><img src=./images/virtualbox/054.png /></kbd>
</br>


次に、アダプター2のホストオンリーアダプター設定</br>
真ん中くらいにある「高度」をクリックし、そのMACアドレスの下４桁くらいをメモしておいてください</br>
ホストオンリーアダプターは仮想NICを**vboxnet0**使ってIPアドレスを付与しています</br>
<kbd><img src=./images/virtualbox/055.png /></kbd>
</br>


再度、Red Hat Enterprise Linux のネットワーク設定</br>
<kbd><img src=./images/virtualbox/056.png /></kbd>
</br>
これより、NATのデバイス名は**enp0s3**、ホストオンリーアダプターのデバイス名は**enp0s8**であることが判明

</br>
<kbd><img src=./images/virtualbox/046.png /></kbd>
</br>


ホストオンリーアダプターは仮想NICを使用しているので、その設定を確認</br>
まずは、「DHCPサーバー」側から確認し、サーバーアドレスやネットマスク、割り当てるIPアドレスレンジを確認</br>
<kbd><img src=./images/virtualbox/044.png /></kbd>
</br>


次に「アダプター」</br>
「アダプターを手動で設定」しか選択できないので、先程確認したDHCPサーバーのアドレスやネットマスクからこのアダプターのIPアドレスを決定</br>
<kbd><img src=./images/virtualbox/045.png /></kbd>
</br>


「アダプターを自動で設定」した場合は、以下のようになり設定できません</br>
<kbd><img src=./images/virtualbox/060.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/061.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/062_0.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/062.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/063.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/064.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/065.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/066.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/067.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/068.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/069.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/070.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/071.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/072.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/073.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/074.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/075.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/076.png /></kbd>
</br>

## ホストマシンからゲストマシンへのSSH接続

</br>
<kbd><img src=./images/virtualbox/077.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/078.png /></kbd>
</br>


## サブスクリプション登録
まず手始めに利用可能なリポジトリを確認。</br>
root権限が必要なので、先に設定しておいた**sudo**を使用</br>
<kbd><img src=./images/hyper-v/057.png /></kbd>
</br>

subscription-managerコマンドでユーザー登録</br>
文法：```subscription-manager register --username <ユーザー名> --password <パスワード>```</br>
ユーザー名とパスワードはRed Hat Customer Portalのものを使用</br>
<kbd><img src=./images/hyper-v/058.png /></kbd>
</br>

システムのロールとサービスレベルを設定し、サブスクリプションをアタッチ</br>
<kbd><img src=./images/hyper-v/059.png /></kbd>
</br>

サブスクリプションのステータス確認</br>
<kbd><img src=./images/hyper-v/060.png /></kbd>
</br>

再度、リポジトリを確認</br>
<kbd><img src=./images/hyper-v/062.png /></kbd>
</br>

アップデートパッケージを確認</br>
<kbd><img src=./images/hyper-v/063.png /></kbd>
</br>

## Red Hat Customer Portalで登録状況確認
<kbd><img src=./images/hyper-v/064.png /></kbd>
</br>

これじゃぁ、どれを登録したのか分からないですね。でも、5/8に登録したこれをクリック</br>

サブスクリプション登録時にUUIDを入手しているので比較</br>
<kbd><img src=./images/hyper-v/065.png /></kbd>
</br>
同じですね。</br>



参考(Special thanks!)
@yamada-hakase サン</br>
[Red Hat Developer Programに登録して最大16台までRHELを使おう](https://qiita.com/yamada-hakase/items/dc39d29fda693238d113)

