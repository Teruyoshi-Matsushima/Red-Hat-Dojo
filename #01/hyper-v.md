# Hyper-V編

Windows 7/8/10 に搭載されているHyper-Vを使って Red Hat Enterprise Linux8.3 の仮想マシンを作成します。

## 仮想マシンのプロファイル作成
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
<kbd><img src=./images/hyper-v/006.png /></kbd>
</br>

#### 世代の指定
<kbd><img src=./images/hyper-v/007.png /></kbd>

#### メモリの割り当て
<kbd><img src=./images/hyper-v/008.png /></kbd>

#### ネットワークの構成
<kbd><img src=./images/hyper-v/009.png /></kbd>

#### 仮想ハードディスクの接続
<kbd><img src=./images/hyper-v/010.png /></kbd>

#### インストールオプション
<kbd><img src=./images/hyper-v/011.png /></kbd>

#### 仮想マシンの新規作成ウィザードの完了
<kbd><img src=./images/hyper-v/012.png /></kbd>

#### 
<kbd><img src=./images/hyper-v/013.png /></kbd>


## Red Hat Enterprise Linux8.3 インストール開始
<kbd><img src=./images/hyper-v/014.png /></kbd>


<kbd><img src=./images/hyper-v/015.png /></kbd>



<kbd><img src=./images/hyper-v/016.png /></kbd>


#### 言語の選択
<kbd><img src=./images/hyper-v/017.png /></kbd>


#### インストール概要
ここでrootパスワード作成とインストール先デバイスを指定。</br>
<kbd><img src=./images/hyper-v/018_0.png /></kbd>
</br>

まずrootパスワード作成。</br>
<kbd><img src=./images/hyper-v/018_1.png /></kbd>
</br>

次にインストール先デバイスを選択します。赤枠で囲まれたエリアをクリック。</br>
<kbd><img src=./images/hyper-v/018_2.png /></kbd>
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
<kbd><img src=./images/hyper-v/020.png /></kbd>



<kbd><img src=./images/hyper-v/021.png /></kbd>


## sudo権限設定
<!-- <kbd><img src=./images/hyper-v/022.png /></kbd> -->

rootユーザーでログインするため、「アカウントが見つかりませんか？」をクリック</br>
<kbd><img src=./images/hyper-v/022_1.png /></kbd>
</br>

ユーザー名：root とし「次へ」</br>
<kbd><img src=./images/hyper-v/022_2.png /></kbd>
</br>

root のパスワードを記入し「サインイン」</br>
<kbd><img src=./images/hyper-v/022_3.png /></kbd>
</br>

Welcome!画面でこのＯＳで利用する言語を指定</br>
<kbd><img src=./images/hyper-v/023.png /></kbd>
</br>

また、位置情報サービスに関してオン/オフを決定</br>
<kbd><img src=./images/hyper-v/025.png /></kbd>
</br>

<kbd><img src=./images/hyper-v/024.png /></kbd>
</br>

「オンラインアカウントへの接続」ですが、まだネットワークへの接続もできていないので「スキップ」</br>
<kbd><img src=./images/hyper-v/026.png /></kbd>
</br>

使用準備完了！「Red Hat Enterprise Linuxを使い始める(S)」をクリック</br>
<kbd><img src=./images/hyper-v/027.png /></kbd>
</br>

やっとログインできました。</br>
<kbd><img src=./images/hyper-v/028.png /></kbd>
</br>

<!--
<kbd><img src=./images/hyper-v/029.png /></kbd>
</br>
-->
    
ターミナルを起動するため、左上の[アクティビティ]－[端末]をクリック</br>    
<kbd><img src=./images/hyper-v/030.png /></kbd>

sudo設定のためターミナルに```visudo```と入力。</br>
<kbd><img src=./images/hyper-v/032.png /></kbd>
</br>

```:101```と打って101行目に移動</br>
ちなみに行番号表示は```:set number```</br>
<kbd><img src=./images/hyper-v/033.png /></kbd>
</br>

キーボードの```i```を押して編集モードへ移行。101行目に```testuser ALL=(ALL) ALL```と入力。</br>
キーボードの[ESC]を押して編集モードを終了し、さらにviを保存＆終了するために```:wq```を入力</br>
<kbd><img src=./images/hyper-v/034.png /></kbd>
</br>

rootユーザーからログアウト</br>
<kbd><img src=./images/hyper-v/034_1.png /></kbd>
</br>

<kbd><img src=./images/hyper-v/034_2.png /></kbd>
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

ネットワークへの接続状況を確認するため```ip a```とターミナルへ入力</br>
赤枠で示すように「eth0」ネットワークへは接続されていないようです。</br>
<kbd><img src=./images/hyper-v/046.png /></kbd>
</br>

<!--
<kbd><img src=./images/hyper-v/047.png /></kbd>
</br>
-->

右上の[電源ボタン]-[有線オフ]-[接続]をクリック</br>
<kbd><img src=./images/hyper-v/048.png /></kbd>
</br>

<kbd><img src=./images/hyper-v/049.png /></kbd>


<kbd><img src=./images/hyper-v/050.png /></kbd>


<kbd><img src=./images/hyper-v/051.png /></kbd>


<kbd><img src=./images/hyper-v/052.png /></kbd>


<kbd><img src=./images/hyper-v/053.png /></kbd>


<kbd><img src=./images/hyper-v/054.png /></kbd>


## Power Shell 文字化け対策
<kbd><img src=./images/hyper-v/055_1.png /></kbd>


<kbd><img src=./images/hyper-v/055_2.png /></kbd>


<kbd><img src=./images/hyper-v/056.png /></kbd>


## サブスクリプション登録
<kbd><img src=./images/hyper-v/057.png /></kbd>


<kbd><img src=./images/hyper-v/058.png /></kbd>


<kbd><img src=./images/hyper-v/059.png /></kbd>


<kbd><img src=./images/hyper-v/060.png /></kbd>




<kbd><img src=./images/hyper-v/062.png /></kbd>


<kbd><img src=./images/hyper-v/063.png /></kbd>


<kbd><img src=./images/hyper-v/064.png /></kbd>

