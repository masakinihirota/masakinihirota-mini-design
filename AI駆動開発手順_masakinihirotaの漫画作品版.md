todo

ユーザーの
auth.usersをpublic.root-accounts
にコピー
トリガーを使う

動作確認






# Webアプリの規模

Webアプリを分類すると
シンプル 1つだけの機能
小規模 2,3個の機能がある、DBを使う
中規模 複数の機能やユーザー管理などがあり、本格的なアプリ。
大規模 1000-1万人ぐらいを使うことを想定したWebアプリ

この設計書は中規模のWebアプリです。

# AI駆動開発手順_masakinihirota-miniの漫画作品版

構想、概要
要件定義
仕様書
設計書
実装手順
を書きます。

※これはmasakinihirota-vnsの基本的な機能のみの実装です。



👇 構想、概要は本家のファイルと同じものです。

--- 構想、概要


VNS masakinihirota

# VNS（Value Network Service）とは

VNSは、SNS（Social Network Service）とは異なる、**価値観**で繋がる新しい形のネットワークサービスです。

* SNSは（狭義では） social network service
社会的な繋がりを作り上げるネットワークです。

* VNSは value network service
価値観で繋がりを作り上げるネットワークです。

日本国憲法は、表現の自由と個人の尊重を保障していますが、SNSでは表現の自由が何よりも優先されているようにおもいます、VNSでは個人の尊重をすることを優先します。
具体的には相手にネガティブな言葉を使うことが出来ません。

## 方式

SNSは
トップダウン方式です。
トップダウンとはいきなり全世界の人と繋がれます。
そこからフォロワーを自由に選びます。

VNSは
ボトムアップ方式です。
ボトムアップとは自分と同じ価値観、信頼できる人とグループを作り、人との和を広げています。


## 目標

インターネットの世界を一部でも平和にするという目標にします。

## SNSの代わりにVNSを作る意味

個人の尊重 ：SNSが表現の自由を重視するのに対し、VNSは個人の尊厳を最優先します。

日本国憲法にはそれぞれ

表現の自由は、言論の自由を含む、あらゆる形態の意思表明の自由を保障します。

個人の尊厳は、人格の尊重を含む、あらゆる形態の個人としての価値を保障します。

表現の自由を制限しようという話ではなく、
ともに保証されている表現の自由と個人の尊厳がぶつかりあった時VNSでは個人の尊厳の優先順位を高く設定するという意味です。
実質的に規制になってしまいますがVNSサイト内限定でのことなのでどうかご理解をお願いします。

安心・安全な場所 ：SNSのような自由な発言ができる反面、ネガティブな批判も自由にできてしまう環境ではなく、VNSは個人を尊重し、表現の自由よりも優先度が上にすることで安心で安全な場所を提供します。
イメージとして、ホワイト企業の職場です。

価値観の共有 ：同じ価値観を持つグループを作ることを目的としており、自身の価値観を表明する場です。他者の価値観を広める場ではありません。

VNSは銀の弾丸ではないとわかっています、根本的に人がヘイトを撒き散らすことを止めることは出来ないでしょう、ただ理性的に、人間として立ち止まることは出来るはずです。

これはSNSを規制させないための、そして弱い人間の為の逃げ道だとご理解ください。



## ポジティブな言葉とネガティブな言葉

単純に比較して、
ネガティブな言葉はポジティブな言葉に比べて数倍の力を持っています。
これは公平ではありません、

複数のポジティブな言葉は1つのネガティブな言葉に負けます。



グループ ：グループ内で問題を解決します。

## 世界の棲み分け

SNSの世界に疲れたらVNSの世界に
VNSの世界で癒やされたら、SNSで戦いに

SNSとVNSはユーザーがどこで活動するか自由に選択できます。

## マインドマップ

		人のつながりのマインドマップ図



## SNSとの違い

| 項目 | SNS（Social Network Service） | VNS（Value Network Service） |
| :--- | :------------------------ | :-------------- |
| 繋がり方 | 社会的な繋がり（友人、同僚、趣味仲間など） | 価値観による繋がり（好きなもの、考え方など） |
| 重視する価値 | 表現の自由 | 個人の尊重（安心・安全な場所の提供） |
| ネットワーク | トップダウン方式（全世界と繋がり、フォロワーを選ぶ） | ボトムアップ方式（価値観でグループを作り、和を広げる） |
| 情報の見え方 | 異なる価値観の人とも繋がれる（相互許可なしに情報が見える場合が多い） | 異なる価値観の人とは相互許可がないと情報が見えない |
| 目的 | 社会的なネットワーク構築、情報発信、コミュニケーションなど | 価値観を共有するグループ作り、安心安全な居場所の提供 |
| 重要視するもの | 表現の自由 | 個人の尊厳 |
| 参加に必要な要素 | 社会的な属性（名前、性別、職業、学校、人種など）が重視される場合がある | 個人の識別と言語（母語） + 価値観 |
| コミュニティ | 多様性があるが、批判やネガティブな発言も自由 | 同じ価値観を持つ人が集まる、安心安全なコミュニティを目指す（オアシス宣言に基づく） |
| リーダーシップ | トップダウン型、プラットフォーム運営者が主導 | ボトムアップ型、自分がリーダーになるorユーザーが自由にリーダーを選べる |

VNSは、従来のSNSのように社会的な繋がりを広げるのではなく、**価値観を共有する人々が集まり、安心して繋がれる場所**を提供することを目指しています。

## VNS（Value Network Service）の詳細

価値観で繋がりを作るサイトです。

価値観サイト ：VNSのサービスを提供するサイトの総称です。
価値観 ：人が物事を判断する基準となる大切な考えや信念。VNSでは、 自身が見聞き・体験し価値を感じたもの 、 自分自身の考え を指します。
例：ピーチパイが好き、特定の作品が好き、特定の考え方に共感するなど

グループ ：同じ価値観を持つ人々が集まるコミュニティ。VNSの主な目的は、このグループ作りを支援することです。
グループ単位で問題を解決していきます。

リーダー ：自分がリーダーになるor自分が自由にリーダーを選びます。各グループはリーダーを持つことができ、リーダーはグループを裁量でコントロールします。

ボトムアップ方式 ：VNSは、まず価値観を共有する信頼できる人々とグループを作り、そこから徐々にネットワークを広げていくボトムアップ方式を採用しています。
グループ同士は、同じ価値観をもちます、リーダーの判断で横の繋がりを持つことができます、それはアライアンスとしてグループ同士をつなげます。

安心・安全な場所 ：VNSは、名前、性別、職業、学校、人種など、社会的な属性に関係なく、 価値観 のみで繋がれるネットワークです。誹謗中傷などがなく、安心して安全に交流できる場所を目指しています。



# masakinihirotaとは

## 名前の由来

インターネットという情報の洪水の中からまっさきに価値ある情報を拾い上げるサービスです。

[洪水から物を拾い上げる画像]

洪水の中から拾い上げた価値がある作品を好き同士の人とマッチング。

インターネットというその大量の情報の中から自分の好きなものを見つけるのは大変です。
その中から価値のある物を拾い上げるサイト。
オアシスという場所で静養しながらゆっくりと作品を楽しむ場所を目指します。
そして疲れが癒えたら、作品からもらったパワーを使い、仲間と一緒になにか作ったりしましょう。



## キャッチフレーズ

「昨日僕が感動した作品を、今日の君はまだ知らない。」



## サイト

真っ先に拾った (masakinihirota)
[https://masakinihirota.com/](https://masakinihirota.com/)


## コンセプト

名前などの属性情報を伏せて、価値観のみで合うかどうかの判断を行い、合いそうな人同士で一緒に何かを行う場所。
人間ではなく価値観をマッチングさせます。
好きな人同士をマッチングするのではなく
好きな価値観同士かどうかをマッチングさせます。

同じ価値観で繋がるシステムを作ります。

言うなれば、ネット上の属性情報がない、名刺であり、履歴書であり、自己紹介カードにあたります。

価値観サイトのマッチングとは
友人
仕事
パートナー
終活

好きな作品を登録してもらいリストを作り、そのリスト同士でマッチングを行い、
同じ好きな作品同士の人たちをつなげ、友人になる切っ掛けを作るサイトです。
自身の価値観を名刺や履歴書のようにつくり、それを自動的にマッチングするサービスです。

相手はどんな人間なのか、何を大切に思っているのか、何に対して興味を持っているのかがわかります。

そして、同じ価値観を持った人同士が繋がりを持ちグループを作り、
喋り、
遊び
学び
想像し
物を作り
人と交流していきます。

そうして関係を発展させて一緒に仕事をするなど、より深い人間関係を作っていきます。

価値観が合わない人と無理して付き合う必要はありません。

インターネット上で集まりなにかします、
もし外部のサービスを使っていてそこでのサービスが終わっても絆が途切れることはありません。

また、相手がどのような価値観を持っているかを知ってからコミュニケーションを図ることが出来ます。

価値観サイトでは属性情報がないので、その人の能力やスキルで判断されます。

他にも、
自分から見た他人のユーザープロフィールも作ることが出来ます。
ユーザープロフィールを作るのに、自分自身であるという制限はありません。

価値観サイトでは同じ価値観の人と、一緒に遊ぶことを想定しています。
例えば、あるオンラインゲームAを遊んでいて、サービス終了になったとしても、同じ価値観を持つ人が、別のオンラインゲームBで一緒に遊ぶことが出来ます。
従来ならばフレンドなどを一緒に誘って次のゲームでもまた一緒に遊んでましたが、
価値観サイトで、例えばマナーの良い人、チートなどを使わない人、と一緒に同じ価値観を持つ人といっしょに遊ぶことが出来るようになります。

言うなれば、自分が作成し、育てた環境を他のオンラインゲームでも持ち回りできるようになります。



## ユーザープロフィールの項目

基本情報
名前
使用言語
好きなもの :今、未来、人生
価値観
スキル



## 価値観サイトのコミュニケーション

価値観サイトでは、
最低限必要な要素は、個別識別できる名前と、母語や第二言語です。

名前は個人を識別し、
母語や第二言語はコミュニケーションを滑らかにします。

逆に不要なのは、
年齢、経歴、学歴、職歴、宗教、出身地、性自認や性的指向、居住地、職業、人種、国籍、障碍、家族構成、年収などはすべて不要です。
ただし、必要な要素ならば表明することが出来ます。

## 主な目標

プロフィール、自己紹介、名刺、履歴書のようなもの

好きな作品を登録してもらう。

友人関連
適切な距離感のある友人を作る。

仕事関連
婚活関連
適切な距離感のある人間関係を作る。

仲間を作るということがエコーチェンバー現象というのは、
人間が人間関係を作る、社会性の友人関係の否定です。




ネット上の悪意を退ける

自分の作品を宣伝
好きな作品を知る
フルリモート、ホワイトワーク就職


## ライフワークバランス

価値観サイトのmasakinihirotaでは仕事とプライベートは切っても切り離せるものではないという前提で作られています。

職友婚一体という考え方
職場
友人
結婚
という人間関係の形成

ライフワークバランスバランスのためのコネクションサイトとも言えます。

趣味が仕事であり、仕事が遊びであり、遊びが仕事でありやりがいでもある、その関係から人との関係を作り、恋人を作り、最後は終活をしていく人生の流れ。



# オアシス宣言とは

VNS、masakinihirotaにおけるコミュニティ運営の基本理念です。

## 目的

インターネットを情報の砂漠と捉え、VNSを 翼を休めるオアシス のような場所とすることを目指します。


### masakinihirota、価値観サイトの目的

#### 差別化を考える

結婚するまでではなく、結婚後の生活も見る

つまり就職、生活、終活

#### 相談できる相手を探す

人に言えない悩み
基本的に信頼できるプロに相談するべき



## モットー

「褒めるときは大きな声でみんなの前で、叱るときは二人きりで小さな声で。」

## 宣言内容 :
    1. インターネット上で翼を休める場所、砂漠の中で命の水を授かる場所を作ります。
    2. 広告はユーザー側に主導権があります。
    3. 共通の価値観を持った人々のオアシスという場所を作ります。
    4. お互いの価値観を認めるのならば、誰もが参加できます。
    5. きれいな世界、優しい世界を守り、広めます。誰もが争うことなく休憩する場所であることを目指します。誰もが笑顔になれる場所です。

## イメージ

イメージとしてはホワイト企業の職場です。

## ルール

オアシス宣言を守る上でのルール :
ネガティブな発言の禁止
建設的な意見は歓迎
クリエイターの尊重
相手の価値観の尊重
マナーの良い交流
ユーザー主導の広告
ネタバレ等の禁止

* オアシス宣言
masakinihirota (masakinihirota)
https://github.com/masakinihirota

* 参考動画: 【公式】『テイルズ オブ リバース』「断頭台の演説」(EN sub) - YouTube: [https://www.youtube.com/watch?v=q8_9ckoVV5M](https://www.youtube.com/watch?v=q8_9ckoVV5M)

あなたの美味しいと感じる心に種族はありますか？

たとえ知らない同士の間柄であっても同じように感じる価値観はあるはずです。
同じ価値観がわかれば、話すきっかけが出来るとおもいます。
そして似た価値観同士でグループを作り、なにか一緒に行いましょう。

例えば、ピーチパイ好きの人がいれば、その人は VNS において「ピーチパイ好き」という価値観を持つグループに属しているとみなされます。VNS では、属性(性自認や性的指向、年齢、経歴など)はすべて不要で、同じ価値観を持つことが重要視されます。



# 人間宣言

## 人間は

人間は誰しもが間違うものです、その失敗を認め成長していきます。

アインシュタインの動画

アインシュタイン名言 - YouTube
https://www.youtube.com/shorts/wxSE3mI6JdU

本田宗一郎「失敗することを恐れるより，何もしないことを恐れろ」と言ったという。

人間は誰でも間違いを犯す不完全な存在であるという考え方。間違いを活かすことの重要性を認識します。

人間宣言とは人間とはロボットのように100％完璧ではなく
かならず間違えるということ、大切なのはその間違えをその後にどう活かすかということ。
間違いを犯したり、失敗したりします。

当たり前のことなのですが、
それを許せない人が数多くいます。



## SNSの剣とVNSの盾

SNSは自由な発言を可能にする道具として普及しましたが、誹謗中傷などの問題も生じてます。
これを剣とすると、
VNSを「盾」として導入し、安心・安全なコミュニティを構築します。
VNSは、ユーザーを管理下に置き、誹謗中傷や荒らし行為からユーザーを保護します。

また、表現の自由の優先度を下げ、個人を尊重することでコミュニティ全体の安全性を向上させます。

これにより、ユーザー自身が道具を使い分けることで、SNSの「剣」としての力を最大限に活用しつつ、VNSという「盾」によってユーザーを守ります。




## 自分で決めるリーダー

自分のリーダーを自分で決めることが出来ます。
オンラインの特徴を活かし、
ユーザープロフィールからマッチングを行い、自分の価値観にあった人を探すことが出来ます。
もしいなければ自分がリーダーになることも可能です。

オンラインでは自分の意志一つで切り替えることが可能です。

# 基本価値観

多様な価値観を認めるか？
	はい
	いいえ

頼れる人はいるか？
	はい
	いいえ

正直か？
	はい
	いいえ

責任感があるか？
	はい
	いいえ

時間を守るか？
	はい
	いいえ

他人を思いやれるか？
	はい
	いいえ

困っている人を助けられるか？
	はい
	いいえ

友だちが欲しいか？
	はい
	いいえ

ピーチパイが好きか？
	はい
	いいえ

協調性はあるか？
	はい
	いいえ

コミュニケーション能力はあるか？
	はい
	いいえ

自分の意見をまっすぐに伝えられるか？
	はい
	いいえ

いまは幸せか？
	はい
	いいえ

仕事はうまくいっているか？
	はい
	いいえ

仕事にやり甲斐はあるか？
	はい
	いいえ

趣味はあるか？
	はい
	いいえ

好きな人はいるか？
	はい
	いいえ

推しはいるか？
	はい
	いいえ

感情をコントロールできる？
	はい
	いいえ



--- 要件定義

1. ユーザー登録・ログイン
ユーザーがアカウントを作成し、ログインできる機能。
2. ユーザープロフィール作成
好きな漫画作品に関する情報を登録できるユーザープロフィールを作成できる機能。
3. 漫画作品登録
ユーザーが好きな漫画作品を登録できる機能。
4. 作品リスト表示
登録された漫画作品を一覧表示できる機能。
5. 自動マッチング
ユーザーの登録した漫画作品に基づいて、価値観の近いユーザーを自動的にマッチングする機能。
6. グループ機能
同じ価値観を持つユーザー同士がグループを形成できる基本的な機能。

- 仕様書
1. ユーザー登録・ログイン

	OAuth認証を利用します。
	アカウント作成時にいくつかの質問（価値観、好きな漫画のジャンルなど）をできるようにします。

2. ユーザープロフィール作成

	ニックネーム、使用言語などの基本情報に加え、好きな漫画作品（今、未来、人生で読みたい・読んだ作品）を登録できる項目を設けます。

3. 漫画作品登録

	公式とユーザーの2種類があります。
	作品名、作者名などの基本情報を登録できます。
	ユーザー登録作品として扱います。
	評判の良い作品は公式リストに移動できるようにします。

4. 作品リスト表示

	登録された漫画作品を一覧で表示します。
	キーワード検索などの絞り込み機能は含めません。

5. 自動マッチング

	ユーザーが登録した好きな漫画作品のリストを比較し、共通の作品が多いユーザーをマッチング候補として提示します。
	「自分が褒めてない作品を褒めている人はマイナス効果」といった複雑なアルゴリズムは含めません。

6. グループ機能

	ユーザーは興味のある漫画作品に関するグループを自動的または手動で作成できます。
	グループにはリーダー（作成者）とメンバーが存在します。
	グループ内でのコミュニケーション機能は本バージョンでは含めません。



--- 設計書

# masakinihirota
	漫画作品

## ルートアカウント
	ユーザーを識別するID
	ログインしたユーザーの管理
	ユーザープロフィールの作成
		1アカウントにつき、複数のユーザープロフィールを作成できます。
		ポイントを消費します。
		ポイントが残っていても、一定数以上は作れません。
	ユーザープロフィールの管理
		複数のユーザープロフィールをリスト化して管理します。
	ユーザープロフィールの最新の状態をまとめて管理
		複数のユーザープロフィールの最新の状態をリスト化して管理します。
	ポイントを所持しています。
		ユーザープロフィールを作りすぎないなどの効果、上限設定が出来ます。
	グループに適用するルールの設定
		例
		オアシス宣言を守る

## ユーザープロフィール
	基本情報
		名前（個別識別できる名前）
		使用言語
	ユーザープロフィールの目的
		仕事の仲間を探す
		趣味の仲間を探す
		婚活の相手を探す
		終活の仲間を探す
	ユーザープロフィールの最新の状態
		例
		現在、積極的に仕事を探している
		現在、積極的に漫画仲間を探している
		現在、積極的に友人を探している
	ユーザーが作った作品
	ユーザーがアウトプットしている場所
		GitHub
		Qiita、Zenn
		Pixiv
		その他
	好きな作品
	 	今
			今、読んでいる好きな作品
			ネタバレ禁止の会話を心がける
	 	未来
			読みたい作品、未発売の作品、発売予定の作品
	 	人生
			評価が確定した作品
			ネタバレありの会話が可能
	評価
		ティア方式で評価します。
		好きな作品を登録時に評価をします。
		絶対相対評価で行います。
	ユーザープロフィールを作成毎に、自動的にグループのリーダーになります。
	マッチングで、メンバーを増やします。

## オープンソース、オープンデーター
	基本的な情報はすべて公開されます。
	信用してもらうにはこれが一番早く正確であり、誰もが検証できることを目指します。

# ランディングページ
	masakinihirota（漫画作品版）の説明、サイトの趣旨がわかるように記述します。

# アカウント作成 ログイン画面
	OAuth認証を使用します。アカウント作成時に好きな漫画のジャンルなどの質問を設けることを検討します。

# メニュー
	基本的なナビゲーションメニューを設置します。





# ルートアカウント
## ユーザー基本情報
ユーザーを識別するID、アカウント情報などを管理します。

## ユーザープロフィールの管理
ユーザーが作成したプロフィール情報を管理します。

## 信頼度
初期バージョンでは、GitHubアカウントやGoogle認証の有無などの基本的なチェック項目のみを考慮します。

## ユーザープロフィールの状態をまとめて管理
ユーザープロフィールの最新の状態（例：現在、積極的に漫画仲間を探しているかなど）を管理する機能は、必要最低限の形で実装を検討します。

## 自分のグループの価値観ルール
グループ内でどのような行為を禁止するかをリーダーが設定できる機能は、初期バージョンでは基本的なネガティブな発言の禁止程度とします。





# ユーザープロフィール
## 新規ユーザープロフィール
### ユーザープロフィール作成の目的
趣味（漫画仲間探し）を主な目的とします。

## 基本ユーザープロフィール
好きな漫画作品に関する情報を登録するプロフィール。
### 最新の状態
現在、積極的に漫画について語り合える仲間を探しているかなどの状態を設定できるようにします。

### ユーザーの基本情報
名前（ニックネーム）、使用言語。

### ユーザーが作った作品
自身で制作した漫画作品などを登録できる項目を設けます。

### ユーザーがアウトプットしている場所とそのアカウント
自身のブログやSNSアカウントなど、漫画に関するアウトプットを行っている場所の情報を登録できるようにします。

### 好きな作品の時制
#### 今、未来、人生情報
それぞれの時制で好きな漫画作品を登録します。

#### 今の価値観情報
現在読んでいる漫画、連載中の作品などを登録します。ネタバレ禁止の注意喚起を行います。

#### 未来の価値観情報
これから読みたい漫画、購入予定の漫画などを登録します。

#### 人生の価値観情報
読了済みで評価が確定した、人生で特に好きな漫画作品を登録します。これらの作品についてはネタバレありの会話が可能となることを示唆します。

### ティア評価

登録済みの作品のリストの中から選んで、ユーザープロフィールに登録します。
その時同時に評価も出来ます。

評価の方法はティア評価で、絶対相対評価を採用します。

#### 絶対相対評価とは？

絶対評価をした作品を最初に選びます。
2番目以降の評価する作品はすべて相対評価で行います。

絶対評価について: 一番面白い作品をティア1に登録します。
相対評価について: 絶対評価した作品と同じぐらい好きならティア1、もしくはひとつ下のティア2に登録します。


そして次から評価する作品は絶対評価した作品とは相対的に評価していきます。

絶対評価した作品は一番好きなのでそれ以上の評価にはなりません。
相対評価した作品は、絶対評価した作品と同じぐらい好きティア1か、もしくはひとつ下のティア2にいれる評価となります。
作品を追加していく時にこれを繰り返していきます。

それぞれのティアには複数の作品を登録可能です。

ティアには面白い作品と評価した物を登録します。
普通かそれ以下の場合は
普通もしくは自分には合わなかった作品として登録します。
まだ読んでいる途中などで評価が未確定の作品は
未評価の作品として登録します。

##### 絶対相対評価の例

ティア1
	進撃の巨人(*一番好き)
	沈黙の艦隊
	龍と苺

ティア2
	MAJOR
	数字であそぼ
	その着せ替え人形は恋をする

ティア3
	MOONLIGHT MILE
	弱虫ペダル

普通もしくは自分には合わなかった作品
	かげきしょうじょ
	私たちはどうかしている
	2.5次元の誘惑
	異世界おじさん

未評価の作品
	シャングリラフロンティア
	神様のバレー
	ラーメン赤猫
	ダイヤモンドの功罪




# 作品関連
## 作品リスト
登録されている漫画作品を一覧表示します。

## 作品登録
ユーザーが好きな漫画作品を登録できます。





# マッチング機能

## 自動マッチング
ユーザーの登録した好きな漫画作品に基づいて、共通点が多いユーザーを自動的にマッチングします。

マッチングの方法
相手とのユーザープロフィールに登録している作品数を比較し、共通点の多いユーザー同士をマッチングします。

### マッチングの基準
マッチングは、作品数だけでなく、評価の高い作品やジャンルの好みも考慮します。

### アルゴリズム
簡単な条件で候補を見つけ、
その候補のユーザープロフィールから、
詳細な解析結果、AIによる分析を表示します。

AIに互いの価値観を読み込んでもらって、解析します。



## 手動マッチング
ランダムに他のユーザーのプロフィールを表示するなどの機能は、初期バージョンでは検討しません。

## マッチング後の価値観比較機能
マッチングしたユーザー同士で、登録している好きな漫画作品を比較できる画面を表示します。





# グループ機能
## リーダー
グループを作成したユーザーがリーダーとなります。メンバーの管理などを行います。

## メンバー
グループに参加したユーザーです。

## 自動グループ機能
共通の好きな漫画作品を持つユーザー同士が自動的にグループを作成する機能を検討します。

## 手動グループ機能
ユーザーが任意にグループを作成したり、他のユーザーを招待してグループを形成したりできる機能を検討します。





# 管理画面
初期バージョンでは、基本的なユーザー管理機能のみを備えたシンプルな管理画面を想定します。

# その他
特にありません。


# 画面遷移図




---実装手順

# 実装の考え方

1. 設計書の徹底的な理解
2. 実装する小さな機能の選定と優先順位付け
3. 技術スタックの準備と開発環境の構築

4. データベース設計
5. 選定した小さな機能の実装
6. テストの実装と実行
7. バージョン管理と継続的インテグレーション (CI)
8. デプロイとフィードバック
9. 反復と改善(4．まで戻って繰り返します。)

重要なのは、各機能が独立しているだけでなく、最終的にはシステム全体として整合性を持つように設計することです。

そのため、初期段階からシステム全体のアーキテクチャをある程度見据えておくことが重要になります。


# スターター

👇 土台となるスターターがあります。

nextjs/saas-starter: Get started quickly with Next.js, Postgres, Stripe, and shadcn/ui.
https://github.com/nextjs/saas-starter

README.mdには以下のように記載されています。

```
# Getting Started
git clone https://github.com/nextjs/saas-starter
cd saas-starter
pnpm install

# Running Locally
# Use the included setup script to create your .env file:

pnpm db:setup

```

スターターを利用して、ユーザー登録・ログイン、ユーザープロフィール作成（好きな漫画登録含む）、漫画作品登録、作品リスト表示、自動マッチング、基本的なグループ機能の実装を優先的に行います。

スターターをuithub化し、NotebookLMに読み込ませる手順は、必要に応じて実施します。

※uithubとうサービスがあります。



# 機能
masakinihirotaの漫画作品の登録と
ユーザープロフィールを作る

# 採用技術
## フロントエンド
*	***Next.js** : Reactベースのフレームワーク。
*	***React** : ユーザーインターフェース構築。
*	***Shadcn/UI** : UIコンポーネントライブラリ。
*	***Radix UI** : アクセシブルなUIコンポーネント。
*	***Tailwind CSS** : CSSフレームワーク。

## バックエンド
*	***Node.js** : JavaScriptランタイム。
*	***Supabase** : オープンソースFirebase代替（データベース、認証）。
*	***Drizzle ORM** : 型安全なORM。
*	***Hono** : 高速なWebフレームワーク（APIサーバー）。

## 状態管理
*	***Zustand** : 軽量な状態管理ライブラリ。

## テスト
*	***Vitest** : 高速なユニットテストフレームワーク。
*	***Jest** : テストフレームワーク。

## バリデーション
*	***Zod** : 型安全なスキーマバリデーションライブラリ。

## 支払い処理
*	*初期バージョンでは実装しません。

## その他
*	***Vercel** : ホスティングプラットフォーム。
*	***GitHub** : ソースコード管理。

# 開発環境
Windows 10
Visual Studio Code
PowerShell
Git
Docker
Node.js

SupabaseはローカルのDockerを立ち上げSupabaseのコンテナを利用します。
ローカルのSupabaseで開発して、運用時にサーバーのSupabaseに切り替えます。

APIはHonoを使用します。

ルーティングは
Next.jsのApp routerを使用します。



# 実装ルール

一貫性のある命名規則

機能を追加した後でテストを書きます。
	*ユニットテスト
	*E2Eテスト

コードにコメントを書きます。

ドキュメントの作成
	*ドキュメントは最新の状態を保ちます。



# 具体的な実装

## 事前に下準備

事前に自分が使いたいライブラリの
基礎的な使い方を実装しておきます。

例えばNext.jsのAPI部分をHonoに変えたい場合は
Honoで実装しておきます。
フォーム部分をConformで実装をしておいたりします。

サンプルを提供しておくよりも
実装時に最小限なコードを書いておくことで
その実装をそのままアプリに反映してくれます。

## DBのスキーマ

DBのスキーマは別に設計を詰めておいたほうがいいとおもいます。
DBのスキーマファイルも自動で作ってくれますが、
余計なエンティティが追加されたりします。

Webアプリの肝部分なのでしっかりと固めておきます。



## 実際に実装をしてもらう


AIが誤解しないようにできるだけ詳しく書きます。
何度もラリーをして、設計を詰めていきます。

ClineはPlanモードで行います。

Auto-approveでEdit filesは許可しません。
実際に実装するときに、ClineをActモードにしてEdit filesを許可します。

タスク分解をします。
優先する機能順に実装していきます。




* 作品登録機能
DBに漫画を登録していきます。
ブラウザ画面から漫画作品を登録できます。
SupabaseのDBに登録された漫画作品を登録します。
Drizzle ORMを使用して型安全なORMを実装します。
Server actionで実装します。


* 登録作品のリスト表示
DBに保存された漫画のリストを表示します。

* ルートアカウントの作成
ログインしたユーザーを管理します。
この機能はスターターでログインしたユーザーを利用して
Supabaseのpublicにルートアカウントテーブルを作って管理します。

* ユーザープロフィールの作成
ログインしたユーザーは複数のユーザープロフィールを作成できます。

ユーザープロフィールは
仕事用
友人用
遊び用
婚活用
終活用
などの目的を選んで作ります。

* ユーザープロフィールに作品を追加
登録した漫画作品の中から選んでユーザープロフィールに登録します。

* マッチング機能
ユーザープロフィール同士を比べて
価値観が近い人を探します。

* グループ機能
マッチングで似た価値観を見つけたらグループに入れます。
グループのリーダーは自分が自動でなります。
マッチングで見つけた人はメンバーになります。

メンバーの状態はウォッチです。

ウォッチとはただ相手を見ているだけの状態です。
相手に見ていることを知らせたい場合は
フォローという状態に更新します。

グループ内の状態
ウォッチ
フォロー
の2種類があります。



---Clineの使用方法

# Cline

## Clineのインストール

1. VSCodeの拡張機能からClineをインストールします。

## Clineの設定

1. Clineを起動し、Planモードを選択します。
2. Clineの設定を行います。
	*- Clineのチャット欄の下にあるAuto-approveを開き、それぞれのオプションを設定します。

### Read files and directories
ファイルを読むことを許可します。

### Edit files
これ許可しないとファイルを生成せず、作ってとお願いしたことがClineの中だけで作ったことになります。

### Execute safe commands
危険なコマンド以外実行することを許可します。

### Use the browser
ブラウザを使うことを許可します。

### Use MCP servers
簡単に言うと、外部(ネット上)の情報にClineがアクセスするための許可です。



## 設計書と実装手順の準備

0. Gitでリポジトリを作成し、設計書と実装手順をMarkdownファイルで用意します。
gitでバージョン管理をしておけばいつでも戻ることが出来ます。

```terminal
git init

```

1. Webアプリの設計書を読み込みます。
	*- 設計書の内容を確認します。
	*- Markdownファイルに設計書を書きます。
2. 同じMarkdownファイルに実装手順を書きます。

## Clineへの読み込み

1. 設計書と実装手順を書いたファイルをClineに読み込ませます。
	*- コピペするか、ファイル名で指示します。

## Planモードでの確認

1. ClineのPlanモードで設計書の内容を確認し、実装手順を確認します。
2. 画面遷移図を作成します。
3. エラーハンドリングのフローを確認します。
4. 必要に応じて設計書に修正を加えます。
5. 修正後、再度ClineのPlanモードで内容を確認します。

## Planモードの終了
設計書、実装手順を満足にかけたらPlanモードの終了です。

つぎはその設計書、実装手順を用いて
タスク分解をします。

タスク分解をしたリストをAIに作ってもらいます。

出来上がったリストを
Google Keep
https://keep.google.com/u/0/
に貼り付けて、
メニューの3点リーダーのアイコンを開けて、
チェックボックスを表示すると
簡易なtodoリストが出来ます。

このtodoリストを使用しながら実装を
AIに頼んでいきます。

Actモードに入る前に、gitでバージョン管理をしておけばいつでも戻ることが出来ます。



## Actモードでの実装


1. 設計書の内容に満足したら、ClineのActモードで実装を開始します。
2. 実装が完了したら、テストを行います。
3. テスト後、必要に応じて修正を加えます。
4. 修正後、再度テストを実施し、最終チェックを行います。

現実のコードとCline上の認識が一致しているかを考えてもらう。
「*****はまだ出来ていません。もういちどソースコードを見直してみてください。」


### 生成されたコードの理解

ClineのActモードでファイルを生成して、
その出力されたコードを理解します、
わからない箇所があればそこの動作をAIに聞きます。
何がどう実装されたかが理解が出来てからGitでコミットします。



### コマンドの手動実行

Clineは外部に影響を与える `npm run系` のコマンドを実行しません。

例えば、Drizzleを利用してSupabaseにテーブルを追加する時、

```terminal
npm run db:push

```
Drizzle ORMのコマンドを手動実行して、
テーブルを追加する必要がありました。



### Tips

- Clineの設定は慎重に行い、必要なオプションを適切に設定しましょう。
- Markdownファイルに設計書と実装手順をまとめておくと、後で見返す際に便利です。
- Planモードでしっかりと確認を行い、実装に移る前に不明点を解消しておきましょう。
- テスト結果をドキュメントに記録し、次回の参考にしましょう。

Planモードで設計書と実装手順を何度も編集します。
「もう一度設計書を評価してみてください。」
「改善提案: 不明点、曖昧な部分、修正したほうがいい箇所などがありましたら教えてください。」

とClineに伝えて、何度でも満足行くまで設計書を検討します。



