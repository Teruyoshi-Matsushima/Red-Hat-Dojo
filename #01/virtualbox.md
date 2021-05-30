# VirtualBox編

VirtualBoxを使ってMac, Windowsに Red Hat Enterprise Linux8.3 の仮想マシンを作成します。</br>
インストール後、sudo設定・ネットワーク設定・サブスクリプション登録までを実施し、 Red Hat Enterprise Linux8.3 マシンとして利用できる環境を構築します。</br>
前提：VirtualBoxインストール済み、Red Hat Enterprise Linux8.3 インストール用ISOダウンロード済み。</br>

## 仮想マシンのプロファイル作成

Red Hat Enterprise Linux8.3 の推奨スペック
<kbd><img src=./images/virtualbox/002.png /></kbd>
</br>

お使いの環境にインストールされている「VirtualBox」を起動し、「新規」をクリック</br>
<kbd><img src=./images/virtualbox/139.png /></kbd>
</br>


<!--
</br>
<kbd><img src=./images/virtualbox/003.png /></kbd>
</br>
-->

Red Hat Enterprise Linux8.3 の推奨スペックに従い、メモリーを1.5GB以上</br>
<kbd><img src=./images/virtualbox/140.png /></kbd>
</br>

Red Hat Enterprise Linux8.3 の推奨スペックに従い、仮想ハードディスサイズを20GB以上</br>
また、この仮想マシンのデータを保存する場所を指定</br>
<kbd><img src=./images/virtualbox/141.png /></kbd>
</br>

仮想マシンの詳細設定を実施するため、「設定」をクリック</br>
<kbd><img src=./images/virtualbox/142.png /></kbd>
</br>

Red Hat Enterprise Linux8.3 インストール用ISOを仮想光学ドライブに設定</br>
<kbd><img src=./images/virtualbox/006_1.png /></kbd>
</br>

ネットワーク設定</br>
NAT</br>
<kbd><img src=./images/virtualbox/007_1.png /></kbd>
</br>

ホストオンリーアダプター</br>
<kbd><img src=./images/virtualbox/007_2.png /></kbd>
</br>


## Red Hat Enterprise Linux8.3 インストール開始
これからVirtualBoxの中で作業していきますが、VirtualBoxから抜けたい場合は左*command*キーを押せばOK

</br>
<kbd><img src=./images/virtualbox/008_0.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/008.png /></kbd>
</br>


「Install Red Hat Enterprise Linux 8.3」を選択するため、*ENTER*キーをクリック</br>
<kbd><img src=./images/virtualbox/009.png /></kbd>
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
ここで Red Hat Enterprise Linux の初期設定をしていく</br>
<kbd><img src=./images/virtualbox/012_6.png /></kbd>
</br>


#### ①インストール先ディスクを選択</br>
インストール先の対象デバイスをクリック
<kbd><img src=./images/virtualbox/104.png /></kbd>
</br>

#### ②時刻と日付設定</br>
地域：アジア、都市：東京 をクリック
<kbd><img src=./images/virtualbox/113.png /></kbd>
</br>

#### ③ネットワークとホスト名を設定</br>
デフォルト状態でNATとホストオンリーアダプターのインターフェースはネットワークに接続されていません。</br>
ここの設定で **enp0s3** と **enp0s8** のインターフェースをネットワークへ接続できるようにしておく。</br>
＊青枠で囲まれたところにボタンが半分隠れています。</br>
ここで、ネットワーク接続のボタンをONにしておくと起動時にDHCPが有効であれば自動的にネットワークへ接続できる。</br>
また青枠で示したように、ここでホスト名も決定しておく。サブスクリプション登録時にマシンを見分けやすくなる。</br>

##### enp0s3
<kbd><img src=./images/virtualbox/175.png /></kbd>
</br>

##### enp0s8
<kbd><img src=./images/virtualbox/176.png /></kbd>
</br>



##### NATとホストオンリーアダプターデバイスを識別する方法
VirtualBoxのネットワーク設定を確認し、NATに設定したネットワークアダプタのMACアドレスとRed Hat Enterprise Linux側のハードウェアアドレスより、
どちらの設定がNATに使用するネットワークアダプタか判別する。
<kbd><img src=./images/virtualbox/145.png /></kbd>
</br>


#### ④rootのパスワード作成</br>
<kbd><img src=./images/virtualbox/014.png /></kbd>
</br>

#### ⑤ユーザーの作成</br>
「このユーザーを管理者にする」にチェックを入れ、管理者権限を持つユーザを作成</br>
管理者として作成したユーザはwheel groupに入り、sudo コマンドを利用できるようになる</br>
<kbd><img src=./images/virtualbox/106.png /></kbd>
</br>


最後に「インストールの開始(R)」をクリック</br>
＊私の環境では、１０分ほどで完了しました。</br>
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


#### 初期セットアップ</br>
<kbd><img src=./images/virtualbox/151.png /></kbd>
</br>


#### ①ライセンス契約への同意</br>
<kbd><img src=./images/virtualbox/153.png /></kbd>
</br>


#### ②システム</br>
ここでサブスクリプション登録</br>
<kbd><img src=./images/virtualbox/154.png /></kbd>
</br>

Red Hat Enterprise Linux Developer Program に登録したログイン名とパスワードを入力し、［登録］をクリック
</br>
<kbd><img src=./images/virtualbox/156.png /></kbd>
</br>

</br>
<kbd><img src=./images/virtualbox/162.png /></kbd>
</br>

</br>
最後に「設定の完了」をクリック
</br>
<kbd><img src=./images/virtualbox/161.png /></kbd>
</br>

<!--
**ユーザーの作成**</br>
一般ユーザーとして**testuser**を作成</br>
<kbd><img src=./images/virtualbox/025.png /></kbd>
</br>


「設定の完了(F)」をクリック</br>
<kbd><img src=./images/virtualbox/026.png /></kbd>
</br>
-->

## 一般権限ユーザーでログイン

先の手順で「設定の完了」をクリック後、作成した一般ユーザーでログイン</br>
<kbd><img src=./images/virtualbox/027.png /></kbd>
</br>


<!--
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
-->

Welcome!画面でこのＯＳで利用する言語を指定</br>
<kbd><img src=./images/virtualbox/036.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/037.png /></kbd>
</br>
</br>

位置情報サービスに関してオン/オフを決定(どちらでも良い)</br>
<kbd><img src=./images/virtualbox/038_1.png /></kbd>
</br>


「オンラインアカウントへの接続」については sandbox 環境ですので敢えて設定はしないので「スキップ」</br>
＊連携したいアカウントがあればいづれかを選択しログイン＊</br>
<kbd><img src=./images/virtualbox/040.png /></kbd>
</br>


使用準備完了！「Red Hat Enterprise Linuxを使い始める(S)」をクリック</br>
<kbd><img src=./images/virtualbox/041.png /></kbd>
</br>


</br>
<kbd><img src=./images/virtualbox/042.png /></kbd>
</br>


「初めて使う方へ」画面では、右上の[×]をクリック
</br>
<kbd><img src=./images/virtualbox/163.png /></kbd>
</br>

<!--
## ホストオンリーアダプター設定

先の設定で、NATネットワークは「enp0s3」と判明したので、ホストオンリーアダプターは「enp0s8」と分かるが確認</br>
</br>
<kbd><img src=./images/virtualbox/164.png /></kbd>
</br>


ホストオンリーアダプターを有効化</br>
</br>
<kbd><img src=./images/virtualbox/170.png /></kbd>
</br>
-->

<!--
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



ホストオンリーアダプターの仮想NIC割当範囲を確認</br>
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
-->

## ホストマシンからゲストマシンへのSSH接続

Red Hat Enterprise Linux のネットワークアドレスを確認するため、「**ip a**」と入力
</br>
<kbd><img src=./images/virtualbox/169.png /></kbd>
</br>


Google社が無償で提供している Public DNSサーバー(8.8.8.8)に対してPingを打ち、インターネット接続を確認
</br>
<kbd><img src=./images/virtualbox/074.png /></kbd>
</br>

<!--
ホストマシンのIPアドレスを確認するため、**ホストマシンのターミナル**を開き「**ifconfig**」と入力</br>
この場合、ホストマシンのIPアドレスが「**192.168.3.4**」と判明する</br>
</br>
<kbd><img src=./images/virtualbox/075.png /></kbd>
</br>


Red Hat Enterprise Linux のターミナルからホストマシンに向けて「**ping 192.168.3.6**」を打つ。
</br>
<kbd><img src=./images/virtualbox/076.png /></kbd>
</br>
-->

ホストマシンのターミナルを使い、Red Hat Enterprise Linux に SSH 経由でログイン</br>
コマンド： **``` ssh testuser@172.31.95.94 ```** </br>
初回はこのアドレスに対して本当にSSH接続をするのか聞いてくるので **yes** と打つ
接続に成功するとプロンプトが ユーザー名@マシン名 となる(この場合 **testuser@tmrhel83** )
</br>
<kbd><img src=./images/virtualbox/077.png /></kbd>
</br>


## サブスクリプション登録
まず手始めに利用可能なリポジトリを確認。</br>
root権限が必要なので、**sudo**を使用</br>
<kbd><img src=./images/virtualbox/080.png /></kbd>
</br>

subscription-managerコマンドで以下を登録</br>
システムのロール：**role**</br>
文法：```sudo subscription-manager role --set="Red Hat Enterprise Linux Server"```</br>
サービスレベル：**service-level**</br>
文法：```sudo subscription-manager service-level --set="Self-Support"```</br>
用途：**usage**</br>
文法：```sudo subscription-manager usage --set="Development/Test"```</br>
システムのロールとサービスレベルを設定し、サブスクリプションをアタッチ</br>
文法：```sudo subscription-manager attach```</br>
<kbd><img src=./images/virtualbox/081.png /></kbd>
</br>

サブスクリプションのステータス確認</br>
<kbd><img src=./images/virtualbox/082.png /></kbd>
</br>


パッケージをアップデート</br>
<kbd><img src=./images/virtualbox/084_5.png /></kbd>
</br>

## Red Hat Customer Portalで登録状況確認

1. Red Hat Customer Portalにログインする。</br>
https://access.redhat.com/</br>

2. ページ上の[SUBSCRIPITONS]をクリックする。</br>
<kbd><img src=./images/virtualbox/089.png /></kbd>
</br>

設定したマシン名が登録されていることを確認</br>
<kbd><img src=./images/virtualbox/085.png /></kbd>
</br>

また、登録情報の詳細を確認</br>
<kbd><img src=./images/virtualbox/086.png /></kbd>
</br>
