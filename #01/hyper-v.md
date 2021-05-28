# Hyper-V編

Windows 7/8/10 に搭載されているHyper-Vを使って Red Hat Enterprise Linux8.3 の仮想マシンを作成します。
インストール後、sudo設定・ネットワーク設定・サブスクリプション登録までを実施し、 Red Hat Enterprise Linux8.3 マシンとして利用できる環境を構築します。</br>
前提：VirtualBoxインストール済み、Red Hat Enterprise Linux8.3 インストール用ISOダウンロード済み。</br>

## 仮想マシンのプロファイル作成

Red Hat Enterprise Linux8.3 の推奨スペック
<kbd><img src=./images/virtualbox/002.png /></kbd>
</br>

[スタート]-[Windows管理ツール]-[Hyper-V マネージャー]をクリックし、Hyper-Vマネージャーを起動</br>
<kbd><img src=./images/hyper-v/000.png /></kbd>
</br>

<!--
<kbd><img src=./images/hyper-v/001.png /></kbd>
-->

### Hyper-Vマネージャー
まず[仮想スイッチマネージャー]をクリックし、既定のネットワーク(Default Switch)があることを確認</br>
<kbd><img src=./images/hyper-v/004.png /></kbd>
</br>

次に[操作(A)]-[神域(J)]-[仮想マシン]をクリック</br>
<kbd><img src=./images/hyper-v/002.png /></kbd>
</br>

<!--
<kbd><img src=./images/hyper-v/003.png /></kbd>
-->

#### 開始する前に
[次に]をクリック</br>
<kbd><img src=./images/hyper-v/005.png /></kbd>
</br>

#### 名前と場所の指定
ここで適切な仮想マシン名をつけて下さい。</br>
また、この仮想マシンのデータを別の場所に格納したい場合は、チェックを付けて格納場所を選択する。</br>
<kbd><img src=./images/hyper-v/106.png /></kbd>
</br>

#### 世代の指定
世代の違いはUEFIのセキュアブートへの対応しているか否か。</br>
Red Hat Enterprise Linux8.3はUEFIセキュアブートに対応しているので、第二世代でもインストール可。</br>
ただし、Hyper-Vのデフォルト設定を以下のように変更すること。</br>
「ハードウェア」→「セキュリティ」→「セキュアブート」</br>
<kbd><img src=./images/hyper-v/007.png /></kbd>
</br>
[CentOSをHyper-V上に入れるときのポイント（第一世代 vs 第二世代)](https://qiita.com/___monta___/items/7c180e56282e3f1c87d0)
</br>

#### メモリの割り当て
<kbd><img src=./images/hyper-v/008.png /></kbd>
</br>

#### ネットワークの構成
<kbd><img src=./images/hyper-v/009.png /></kbd>
</br>

#### 仮想ハードディスクの接続
<kbd><img src=./images/hyper-v/110.png /></kbd>
</br>

#### インストールオプション
<kbd><img src=./images/hyper-v/011.png /></kbd>
</br>

#### 仮想マシンの新規作成ウィザードの完了
<kbd><img src=./images/hyper-v/012.png /></kbd>
</br>

#### 
<kbd><img src=./images/hyper-v/013.png /></kbd>
</br>

## Red Hat Enterprise Linux8.3 インストール開始
<kbd><img src=./images/hyper-v/014.png /></kbd>
</br>

</br>
<kbd><img src=./images/hyper-v/115_1.png /></kbd>
</br>

</br>
<kbd><img src=./images/hyper-v/115_3.png /></kbd>
</br>


#### 言語の選択
<kbd><img src=./images/hyper-v/017.png /></kbd>
</br>

#### インストール概要
ここで Red Hat Enterprise Linux の初期設定をしていく
</br>
<kbd><img src=./images/hyper-v/118_0.png /></kbd>
</br>

①インストール先ディスクを選択</br>
インストール先の対象デバイスをクリック
</br>
<kbd><img src=./images/hyper-v/118_1.png /></kbd>
</br>

②時刻と日付設定</br>
地域：アジア、都市：東京をクリック
</br>
<kbd><img src=./images/hyper-v/118_2.png /></kbd>
</br>

③ネットワークとホスト名を設定</br>
Hyper-Vで使う Default Switch は NAT と ホストオンリー の機能を持っている</br>
この段階でネットワークに接続しておく
</br>
<kbd><img src=./images/hyper-v/118_3.png /></kbd>
</br>
</br>
<kbd><img src=./images/hyper-v/118_5.png /></kbd>
</br>
ネットワーク接続のボタンをONにしておき、DHCPが有効であれば自動的にネットワークへ接続できる。
また、この画面でホスト名も決定。サブスクリプション登録時にマシンを見分けやすくなる。

④rootパスワード作成
</br>
<kbd><img src=./images/hyper-v/018_1.png /></kbd>
</br>

⑤ユーザーの作成
ここで管理者ユーザを作る。管理者として作成したユーザはwheel groupに入り、sudo コマンドを利用できるようになる。
</br>
<kbd><img src=./images/hyper-v/118_6.png /></kbd>
</br>


最後に「インストールの開始(R)」をクリック</br>
<kbd><img src=./images/hyper-v/018_3.png /></kbd>
</br>


<kbd><img src=./images/hyper-v/018_4.png /></kbd>
</br>

インストール終了後、「システム再起動(R)」をクリック</br>
<kbd><img src=./images/hyper-v/019.png /></kbd>
</br>

 ## Red Hat Enterprise Linux8.3 起動！
[Red Hat Enterprise Linux (・・・)]にカーソルを当て**enter**</br> 
<kbd><img src=./images/hyper-v/020_0.png /></kbd>
 
初期セットアップ
</br>
<kbd><img src=./images/hyper-v/121.png /></kbd>
</br>

①ライセンス契約への同意
</br>
<kbd><img src=./images/hyper-v/121_1.png /></kbd>
</br>

②システム</br>
ここでサブスクリプション登録
</br>
<kbd><img src=./images/hyper-v/121_2.png /></kbd>
</br>

</br>
<kbd><img src=./images/hyper-v/121_3.png /></kbd>
</br>

</br>
<kbd><img src=./images/hyper-v/121_4.png /></kbd>
</br>

</br>
<kbd><img src=./images/hyper-v/121_5.png /></kbd>
</br>

</br>
<kbd><img src=./images/hyper-v/121_6.png /></kbd>
</br>

</br>
<kbd><img src=./images/hyper-v/121_7.png /></kbd>
</br>

</br>
<kbd><img src=./images/hyper-v/121_8.png /></kbd>
</br>


## 一般ユーザーでログイン
インストールの途中で作成した一般ユーザー```testuser```でログイン</br>
<kbd><img src=./images/hyper-v/035.png /></kbd>
</br>

パスワードを入力</br>
<kbd><img src=./images/hyper-v/036.png /></kbd>
</br>

<kbd><img src=./images/hyper-v/037.png /></kbd>


Welcome!画面でこのＯＳで利用する言語を指定</br>
<kbd><img src=./images/hyper-v/038.png /></kbd>
</br>


<kbd><img src=./images/hyper-v/039.png /></kbd>
</br>

位置情報サービスに関してオン/オフを決定</br>
<kbd><img src=./images/hyper-v/040.png /></kbd>
</br>

<kbd><img src=./images/hyper-v/041.png /></kbd>
</br>

「オンラインアカウントへの接続」ですが、まだネットワークへの接続もできていないので「スキップ」</br>
<kbd><img src=./images/hyper-v/042.png /></kbd>
</br>

使用準備完了！「Red Hat Enterprise Linuxを使い始める(S)」をクリック</br>
<kbd><img src=./images/hyper-v/043.png /></kbd>
</br>

「初めて使う方へ」画面ですが右上の[×]をクリック</br>
<kbd><img src=./images/hyper-v/044.png /></kbd>
</br>

<!--
<kbd><img src=./images/hyper-v/045.png /></kbd>
</br>
-->

## ネットワーク設定
ターミナルを起動するため、左上の[アクティビティ]－[端末]をクリック</br>
<kbd><img src=./images/hyper-v/030.png /></kbd>
</br>

画面右上のネットワークをクリックし、接続状況を確認</br>



## ホストマシンからゲストマシンへのSSH接続

ネットワークへの接続状況を確認するため```ip a```とターミナルへ入力</br>
Red Hat Enterprise Linux の IP アドレスを確認
</br>
<kbd><img src=./images/hyper-v/146.png /></kbd>
</br>

ホストマシンでpowershellを開き、Red Hat Enterprise Linux に向けて**ping**を打つ
</br>
<kbd><img src=./images/hyper-v/154.png /></kbd>
</br>

Google社が無償で提供している Public DNSサーバー(8.8.8.8)に対してPingを打ち、インターネット接続を確認
</br>
<kbd><img src=./images/hyper-v/049_11.png /></kbd>
</br>

ホストマシンのターミナルを使い、Red Hat Enterprise Linux に SSH 経由でログインする。
</br>
<kbd><img src=./images/hyper-v/154_1.png /></kbd>
</br>


## PowerShell 文字化け対策
初期設定のままの PowerShell ではサブスクリプション登録時のメッセージが文字化けするので、その対策</br>
文字化けの原因は、初期状態のPowerShellの文字コードは**US-ASCII**。一方、Linux側は**UTF-8**であるためです。</br>
そのため、PowerShellを**UTF-8**対応し、表示フォントも対応させます。</br>
PowerShellのプロパティを開く</br>
<kbd><img src=./images/hyper-v/055_1.png /></kbd>
</br>

[ショートカット]-[リンク先]のパスに以下を追記し、起動時に```chcp```コマンドで**UTF-8(65001)**対応</br>
``` -NoExit -Command "chcp 65001"```</br>
<kbd><img src=./images/hyper-v/055_2.png /></kbd>
</br>

またフォントも、文字化けしないフォントへと変更</br>
**BIZ UDゴシック**はOK。ConsolasはNG。(その他のフォントは未調査。。。m(_ _)m )</br>
<kbd><img src=./images/hyper-v/056.png /></kbd>
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

まず手始めに利用可能なリポジトリを確認。
root権限が必要なので、sudoを使用
</br>
<kbd><img src=./images/hyper-v/157.png /></kbd>
</br>

subscription-managerコマンドで以下を登録</br>
システムのロール：role</br>
文法：sudo subscription-manager role --set="Red Hat Enterprise Linux Server"</br>
サービスレベル：service-level</br>
文法：sudo subscription-manager service-level --set="Self-Support"</br>
用途：usage</br>
文法：sudo subscription-manager usage --set="Development/Test"</br>
システムのロールとサービスレベルを設定し、サブスクリプションをアタッチ</br>
文法：sudo subscription-manager attach</br>
</br>
<kbd><img src=./images/hyper-v/158.png /></kbd>
</br>

サブスクリプションのステータス確認
</br>
<kbd><img src=./images/hyper-v/159.png /></kbd>
</br>

パッケージをアップデート
</br>
<kbd><img src=./images/hyper-v/160.png /></kbd>
</br>

</br>
<kbd><img src=./images/hyper-v/161.png /></kbd>
</br>


## Red Hat Customer Portalで登録状況確認

1. Red Hat Customer Portalにログインする。</br>
https://access.redhat.com/</br>


2. ページ上の[SUBSCRIPITONS]をクリックする。</br>
</br>
<kbd><img src=./images/hyper-v/164.png /></kbd>
</br>


</br>
<kbd><img src=./images/hyper-v/166.png /></kbd>
</br>

</br>
<kbd><img src=./images/hyper-v/168.png /></kbd>
</br>

また、登録情報の詳細を確認
</br>
<kbd><img src=./images/hyper-v/169.png /></kbd>
</br>


## Red Hat Enterprise Linux 終了方法



参考(Special thanks!)
@___monta___ サン</br>
[CentOSをHyper-V上に入れるときのポイント（第一世代 vs 第二世代)](https://qiita.com/___monta___/items/7c180e56282e3f1c87d0)

@yamada-hakase サン</br>
[Red Hat Developer Programに登録して最大16台までRHELを使おう](https://qiita.com/yamada-hakase/items/dc39d29fda693238d113)

@s4i サン</br>
[PowerShell起動時、文字コードをUTF-8に変える方法](https://qiita.com/s4i/items/75c19c9feb10b54c1ce9)
