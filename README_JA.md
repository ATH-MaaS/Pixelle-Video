<h1 align="center">🎬 Pixelle-Video —— AI 完全自動ショート動画エンジン</h1>

<p align="center"><a href="README_EN.md">English</a> | <a href="README.md">中文</a> | <b>日本語</b></p>

<p align="center">
  <a href="https://www.youtube.com/watch?v=uUkx-lRxLjc" target="_blank"><img src="https://img.shields.io/badge/🎥 Video%20Tutorial-EA4C89" alt="動画チュートリアル"></a>
  <a href="https://github.com/AIDC-AI/Pixelle-Video/releases" target="_blank"><img src="https://img.shields.io/badge/📦 Windows-50C878" alt="Windows パッケージ"></a>
  <a href="https://aidc-ai.github.io/Pixelle-Video" target="_blank"><img src="https://img.shields.io/badge/📘 Documentation-4A90E2" alt="ドキュメント"></a>
  <a href="https://github.com/AIDC-AI/Pixelle-Video/stargazers"><img src="https://img.shields.io/github/stars/AIDC-AI/Pixelle-Video.svg" alt="Stargazers"></a>
  <a href="https://github.com/AIDC-AI/Pixelle-Video/issues"><img src="https://img.shields.io/github/issues/AIDC-AI/Pixelle-Video.svg" alt="Issues"></a>
  <a href="https://github.com/AIDC-AI/Pixelle-Video/network/members"><img src="https://img.shields.io/github/forks/AIDC-AI/Pixelle-Video.svg" alt="Forks"></a>
  <a href="https://github.com/AIDC-AI/Pixelle-Video/blob/main/LICENSE"><img src="https://img.shields.io/github/license/AIDC-AI/Pixelle-Video.svg" alt="License"></a>
</p>

https://github.com/user-attachments/assets/a42e7457-fcc8-40da-83fc-784c45a8b95d

**トピック**を入力するだけで、Pixelle-Video が自動的に次のことを行います:
- ✍️ 動画の台本を作成
- 🎨 AI 画像/動画を生成  
- 🗣️ 音声ナレーションを合成
- 🎵 BGM を追加
- 🎬 ワンクリックで動画を作成


**ハードルゼロ、編集経験ゼロ** - 動画制作を、一文を入力するのと同じくらい簡単にします!


## 🖥️ Web インターフェースのプレビュー

![Web UI インターフェース](resources/webui_en.png)


## 📋 最近の更新

- ✅ **2026-06-01**: WebUI に API メディアモデルの直接設定を追加しました。画像/動画プロバイダーの認証情報、Base URL、プロバイダーごとのプロキシ切り替えを含みます
- ✅ **2026-01-26**: Motion Transfer パイプラインを追加しました — 参照動画と画像をアップロードしてモーションを転写できます。
- ✅ **2026-01-14**: 「Digital Human」と「Image-to-Video」パイプラインを追加し、多言語 TTS 音声に対応しました
- ✅ **2026-01-06**: RunningHub の 48G VRAM マシンに対応しました
- ✅ **2025-12-28**: RunningHub の同時実行数の上限を設定可能にし、LLM の構造化データ応答の処理を改善しました
- ✅ **2025-12-17**: ComfyUI API Key の設定、Nano Banana モデルへの対応、API テンプレートのカスタムパラメーターを追加しました
- ✅ **2025-12-10**: サイドバーに FAQ を組み込み、edge-tts のバージョンを固定して TTS サービスの不安定さを解消しました
- ✅ **2025-12-08**: 複数の台本分割モード(段落/行/文)に対応し、直接プレビューできるようにテンプレート選択を改善しました
- ✅ **2025-12-06**: 動画生成 API の URL パス処理を修正し、クロスプラットフォーム互換性を確保しました
- ✅ **2025-12-05**: Windows オールインワンパッケージのダウンロードを追加し、画像・動画解析ワークフローを最適化しました
- ✅ **2025-12-04**: 新機能「Custom Media」 - 自分の写真/動画をアップロードすると、AI による解析と台本生成が行われます
- ✅ **2025-11-18**: RunningHub の並列処理、履歴ページの追加、動画タスクの一括作成に対応しました


## ✨ 主な機能

- ✅ **完全自動生成** - トピックを入力するだけで、完成した動画を自動生成します
- ✅ **AI スマートコピーライティング** - トピックに基づいてナレーションをインテリジェントに作成するため、自分で台本を書く必要はありません
- ✅ **AI 生成画像** - 各文に美しい AI イラストが付きます
- ✅ **AI 生成動画** - AI 動画生成モデル(WAN 2.1 など)に対応し、動きのある動画コンテンツを作成できます
- ✅ **モデル API の直接呼び出し** - DashScope、OpenAI、Seedream、Seedance、Kling などの画像/動画生成サービスを直接呼び出せます
- ✅ **AI 生成音声** - Edge-TTS、Index-TTS をはじめとする多くの主要な TTS ソリューションに対応しています
- ✅ **BGM** - BGM を追加して、動画の雰囲気を高められます
- ✅ **ビジュアルスタイル** - 複数のテンプレートから選んで、独自の動画スタイルを作れます
- ✅ **柔軟なサイズ** - 縦長、横長など、さまざまな動画サイズに対応しています
- ✅ **複数の AI モデル** - GPT、Qwen、DeepSeek、Ollama などに対応しています
- ✅ **アトミック機能の柔軟な組み合わせ** - ComfyUI / RunningHub のワークフローと API モデルの直接呼び出しに対応し、画像、動画、TTS、VLM などの機能を必要に応じて入れ替えられます


## 📊 動画生成パイプライン

Pixelle-Video はモジュール式の設計を採用しており、動画生成のプロセス全体が明確で簡潔です:

![動画生成フロー](resources/flow_en.png)

入力テキストから最終的な動画出力まで、プロセス全体は明確でシンプルです: **台本生成 → 画像プランニング → フレームごとの処理 → 動画合成**

各ステップは柔軟にカスタマイズでき、さまざまな AI モデル、音声エンジン、ビジュアルスタイルなどを選んで、個々の制作ニーズに応えられます。


## 🎬 動画サンプル

以下は Pixelle-Video で実際に生成した事例で、さまざまなテーマやスタイルの動画の仕上がりを紹介しています:

### 📱 拡張モジュール動画ショーケース

<table>
<tr>
<td width="33%">
<h3>👤 AI デジタルアバター</h3>
<video src="https://github.com/user-attachments/assets/7c122563-c2e0-4dcd-a73c-25ba1d4fa2dd" controls width="100%"></video>
<p align="center"><b>韓国語を話す AI アバター</b></p>
</td>
<td width="33%">
<h3>🖼️ 画像から動画へ</h3>
<video src="https://github.com/user-attachments/assets/5b4eef17-07d0-4bde-9748-2ed68cc9888e" controls width="100%"></video>
<p align="center"><b>アニメーション化したカートゥーン動画</b></p>
</td>
<td width="33%">
<h3>💃 モーション転写</h3>
<video src="https://github.com/user-attachments/assets/7b1240bc-e965-434c-b343-118ec4793d4f" controls width="100%"></video>
<p align="center"><b>踊る子猫</b></p>
</td>
</tr>
</table>

### 📱 縦長動画ショーケース

<table>
<tr>
<td width="33%">
<h3>🌄 ドキュメンタリー&ライフスタイル – デフォルトテンプレート</h3>
<video src="https://github.com/user-attachments/assets/e6716c1d-78de-453d-84c2-10873c8c595f" controls width="100%"></video>
<p align="center"><b>旅路の風景</b></p>
</td>
<td width="33%">
<h3>🔍 文化の解剖 – デフォルトテンプレート</h3>
<video src="https://github.com/user-attachments/assets/f5de75f6-135a-4ab4-9f5f-079f649764d5" controls width="100%"></video>
<p align="center"><b>サンタの正体</b></p>
</td>
<td width="33%">
<h3>🔭 科学的探究 – デフォルトテンプレート</h3>
<video src="https://github.com/user-attachments/assets/ceb8b0df-8331-4e1f-88e7-db5b295a1c1d" controls width="100%"></video>
<p align="center"><b>なぜ私たちはまだ地球外文明を見つけられないのか?</b></p>
</td>
</tr>
<tr>
<td width="33%">
<h3>🌱 自己成長 – クローン音声</h3>
<video src="https://github.com/user-attachments/assets/1bad9a49-df83-4905-9cc8-9a7640e9c7d8" controls width="100%"></video>
<p align="center"><b>自分をレベルアップする方法</b></p>
</td>
<td width="33%">
<h3>🧠 深い思考 – デフォルトテンプレート</h3>
<video src="https://github.com/user-attachments/assets/663b705a-2aea-44bc-b266-4bb27aa255a8" controls width="100%"></video>
<p align="center"><b>反脆弱性を理解する</b></p>
</td>
<td width="33%">
<h3>🏯 歴史&文化 – 静止フレーム</h3>
<video src="https://github.com/user-attachments/assets/56e0a018-fa99-47eb-a97f-fc2fa8915724" controls width="100%"></video>
<p align="center"><b>資治通鑑(統治の助けとなる総合的な鏡)</b></p>
</td>
</tr>
<tr>
<td width="33%">
<h3>☀️ 感動ストーリー – クローン音声</h3>
<video src="https://github.com/user-attachments/assets/4687df95-dd21-4a7b-b01e-f33a7b646644" controls width="100%"></video>
<p align="center"><b>冬の日差し</b></p>
</td>
<td width="33%">
<h3>📜 小説の映像化 – カスタム台本</h3>
<video src="https://github.com/user-attachments/assets/d354465e-3fa8-40b4-93e9-61ad75ef0697" controls width="100%"></video>
<p align="center"><b>闘破蒼穹(Battle Through the Heavens)</b></p>
</td>
<td width="33%">
<h3>🧬 知識解説 – Qwen 画像生成</h3>
<video src="https://github.com/user-attachments/assets/8ac21768-41ce-4d41-acdd-e3dd3eb9725a" controls width="100%"></video>
<p align="center"><b>健康のための必須ヒント</b></p>
</td>
</tr>
</table>

### 🖥️ 横長動画ショーケース

<table>
<tr>
<td width="50%">
<h3>💰 副業で稼ぐ - 映画テンプレート</h3>
<video src="https://github.com/user-attachments/assets/c9209d4e-73a6-4b82-aaad-cf102248c9e2" controls width="100%"></video>
<p align="center"><b>副業で稼ぐ</b></p>
</td>
<td width="50%">
<h3>🏛️ 歴史解説 - カスタムテンプレート</h3>
<video src="https://github.com/user-attachments/assets/a767c452-d5f1-4cff-bb34-b80fff0d4c3e" controls width="100%"></video>
<p align="center"><b>資治通鑑からの洞察</b></p>
</td>
</tr>
</table>

> 💡 **ヒント**: これらの動画はすべて、トピックのキーワードを入力するだけで AI が完全自動で生成したものです。動画編集の経験は一切必要ありません!

<div id="tutorial-start" />

## 🚀 クイックスタート

### 🪟 Windows オールインワンパッケージ(Windows ユーザーにおすすめ)

**Python、uv、ffmpeg のインストールは不要で、すぐに使えます!**

👉 **[Windows オールインワンパッケージをダウンロード](https://github.com/AIDC-AI/Pixelle-Video/releases/latest)**

1. 最新の Windows オールインワンパッケージをダウンロードして展開します
2. `start.bat` をダブルクリックして Web インターフェースを起動します
3. ブラウザで http://localhost:8501 が自動的に開きます
4. 「⚙️ System Configuration」で LLM API と画像生成サービスを設定します
5. 動画の生成を始めましょう!

> 💡 **ヒント**: パッケージにはすべての依存関係が含まれているため、環境を手動でインストールする必要はありません。初回利用時は API キーを設定するだけです。


### ソースからインストール(macOS / Linux ユーザー、またはカスタマイズが必要なユーザー向け)

#### 前提条件

始める前に、Python パッケージマネージャー `uv` と動画処理ツール `ffmpeg` をインストールする必要があります:

##### uv のインストール

お使いのシステムでのインストール方法は、uv の公式ドキュメントをご覧ください:  
👉 **[uv インストールガイド](https://docs.astral.sh/uv/getting-started/installation/)**

インストール後、ターミナルで `uv --version` を実行して、インストールが成功したことを確認してください。

##### ffmpeg のインストール

**macOS**
```bash
brew install ffmpeg
```

**Ubuntu / Debian**
```bash
sudo apt update
sudo apt install ffmpeg
```

**Windows**
- ダウンロード URL: https://ffmpeg.org/download.html
- ダウンロード後に展開し、`bin` ディレクトリをシステム環境変数 PATH に追加します

インストール後、ターミナルで `ffmpeg -version` を実行して、インストールが成功したことを確認してください。


#### ステップ 1: プロジェクトをクローンする

```bash
git clone https://github.com/AIDC-AI/Pixelle-Video.git
cd Pixelle-Video
```

#### ステップ 2: Web インターフェースを起動する

```bash
# Run with uv (recommended, will automatically install dependencies)
uv run streamlit run web/app.py
```

ブラウザで http://localhost:8501 が自動的に開きます

#### ステップ 3: Web インターフェースで設定する

初回利用時は「⚙️ System Configuration」パネルを展開し、次の項目を入力します:
- **LLM 設定**: AI モデル(Qwen、GPT など)を選択し、API Key を入力します
- **ComfyUI / RunningHub 設定**: ワークフローベースの画像・動画・音声生成を使いたい場合は、ローカルの ComfyUI または RunningHub API Key を設定します
- **API メディアモデル設定**: DashScope、OpenAI、ARK、Kling などの画像/動画モデルプロバイダーを直接使う場合は、API Key、Base URL、プロキシオプションを設定します

設定後、「Save Configuration」をクリックすれば、動画の生成を始められます!

<div id="tutorial-end" />

## 💻 使い方

Web インターフェースを開くと、3 カラムのレイアウトが表示されます。各部分について詳しく説明します:


### ⚙️ システム設定(初回利用時に必須)

初回利用時は設定が必要です。「⚙️ System Configuration」パネルをクリックして展開します:

#### 1. LLM 設定(大規模言語モデル)
動画の台本の生成に使用します。

**プリセットのクイック選択**  
- ドロップダウンメニューからプリセットモデル(Qwen、GPT-4o、DeepSeek など)を選択します
- 選択すると、base_url と model が自動的に入力されます
- 「🔑 Get API Key」リンクをクリックして登録し、キーを取得します

**手動設定**  
- API Key: キーを入力します
- Base URL: API のアドレス
- Model: モデル名

#### 2. ComfyUI / RunningHub 設定
ComfyUI ワークフローを通じて、動画用の画像、動画クリップ、音声を生成するために使用します。

**ローカルデプロイ(推奨)**  
- ComfyUI URL: ローカル ComfyUI サービスのアドレス(デフォルトは http://127.0.0.1:8188)
- 「Test Connection」をクリックして、サービスが利用可能であることを確認します

**クラウドデプロイ**  
- RunningHub API Key: クラウド画像生成サービスのキー

#### 3. API メディアモデル設定
ComfyUI/RunningHub に依存せず、画像、動画、アセット解析のモデルプロバイダーを直接呼び出すために使用します。

**対応プロバイダー**
- OpenAI / GPT Image: GPT 画像生成モデル用
- DashScope / Wan / HappyHorse: Alibaba Tongyi Wan の画像・動画生成用
- Volcengine ARK / Seedream / Seedance: Seedream の画像生成と Seedance の動画生成用
- Kling AI: Kling の動画生成用

**設定項目**
- API Key / Access Key / Secret Key: プロバイダーの認証情報
- Base URL: モデルサービスのエンドポイント。WebUI には公式のデフォルト値があらかじめ入力されています
- ローカルプロキシ: 例 `http://127.0.0.1:9090`
- プロキシを使用: プロバイダーごとに、リクエストをローカルプロキシ経由で送るかどうかを個別に選択できます
- モデルのリクエストパラメーターを出力: プロンプト、モデル名、入力ファイルのパスをターミナルに出力するデバッグオプション

> 💡 ComfyUI または RunningHub のみを使う場合は、API メディアモデル設定は空のままで構いません。`api/...` ワークフローを選ぶ場合は、先に対応するプロバイダーの認証情報を設定してください。

設定後、「Save Configuration」をクリックします。


### 📝 コンテンツ入力(左カラム)

#### 生成モード
- **AI Generated Content**: トピックを入力すると、AI が自動的に台本を作成します
  - 向いているケース: 動画を素早く生成したく、台本は AI に任せたい場合
  - 例: 「なぜ読書習慣を身につけるべきか」
- **Fixed Script Content**: 完成した台本を直接入力し、AI による作成をスキップします
  - 向いているケース: すでに台本が用意されていて、そのまま動画を生成したい場合

#### BGM(背景音楽)
- **No BGM**: 音声ナレーションのみ
- **Built-in Music**: プリセットの BGM(default.mp3 など)を選択します
- **Custom Music**: 自分の音楽ファイル(MP3/WAV など)を `bgm/` フォルダーに置きます
- 「Preview BGM」をクリックして音楽をプレビューします


### 🎤 音声設定(中央カラム)

#### TTS ワークフロー
- ドロップダウンメニューから TTS ワークフローを選択します(Edge-TTS、Index-TTS などに対応)
- システムが `workflows/` フォルダー内の TTS ワークフローを自動的にスキャンします
- ComfyUI に詳しい方は、TTS ワークフローをカスタマイズできます

#### 参照音声(オプション)
- 音声クローン用の参照音声ファイルをアップロードします(MP3/WAV/FLAC などの形式に対応)
- 音声クローンに対応した TTS ワークフロー(Index-TTS など)で使用できます
- アップロード後、その場で試聴できます

#### プレビュー機能
- テスト用のテキストを入力し、「Preview Voice」をクリックして仕上がりを試聴します
- 参照音声を使ったプレビューにも対応しています


### 🎨 ビジュアル設定(中央カラム)

#### 画像生成
AI が生成する画像のスタイルを決めます。

**ComfyUI ワークフロー**  
- ドロップダウンメニューから画像生成ワークフローを選択します
- ローカルデプロイ(selfhost)とクラウド(RunningHub)のワークフローに対応しています
- 対応するプロバイダーの認証情報を設定すれば、`api/...` の画像モデル直接呼び出しワークフローにも対応します
- デフォルトでは `image_flux.json` を使用します
- ComfyUI に詳しい方は、自分のワークフローを `workflows/` フォルダーに置けます

**画像サイズ**  
- 生成する画像の幅と高さを設定します(単位: ピクセル)
- デフォルトは 1024x1024 で、必要に応じて調整できます
- 注意: モデルによってサイズの制限が異なります

**プロンプトのプレフィックス**  
- 画像全体のスタイルを制御します(英語で記述する必要があります)
- 例: Minimalist black-and-white matchstick figure style illustration, clean lines, simple sketch style
- 「Preview Style」をクリックして仕上がりを確認します

#### 動画テンプレート
動画のレイアウトとデザインを決めます。

**テンプレートの命名規則**  
- `static_*.html`: 静的テンプレート(AI 生成メディアなし、テキストのみのスタイル)
- `image_*.html`: 画像テンプレート(AI 生成画像を背景に使用)
- `video_*.html`: 動画テンプレート(AI 生成動画を背景に使用)

**使い方**  
- ドロップダウンメニューからテンプレートを選択します。サイズ(縦長/横長/正方形)ごとにグループ化して表示されます
- 「Preview Template」をクリックして、カスタムパラメーターで仕上がりを確認します
- HTML に詳しい方は、`templates/` フォルダーに自分のテンプレートを作成できます
- 🔗 [すべてのテンプレートのプレビューを見る](https://aidc-ai.github.io/Pixelle-Video/user-guide/templates/#built-in-template-preview)

#### API 動画生成
動的な動画テンプレートや拡張ワークフローを使用する場合、API 動画モデルを直接呼び出してクリップを生成できます。

- DashScope Wan / HappyHorse、Kling、Seedance などの動画モデルに対応しています
- 解像度、アスペクト比、長さ、ウォーターマーク、ネイティブ音声など、モデルに応じたオプションを表示します
- ネットワーク/ダウンロードの再試行と、コンテンツ審査で失敗した場合の LLM によるプロンプト中立化の再試行に対応しています
- Custom Media ワークフローでは、API 動画セグメントがナレーション音声の長さに合わせるよう試み、隣接するセグメントの情報を使って連続性を高めます


### 🎬 動画の生成(右カラム)

#### 生成ボタン
- すべてのパラメーターを設定したら、「🎬 Generate Video」をクリックします
- リアルタイムで進捗を表示します(台本生成中 → 画像生成中 → 音声合成中 → 動画合成中)
- 完了後、動画のプレビューが自動的に表示されます

#### 進捗表示
- 現在のステップをリアルタイムで表示します
- 例: 「Frame 3/5 - Generating Image」

#### 動画プレビュー
- 生成後に自動的に再生されます
- 動画の長さ、ファイルサイズ、フレーム数などを表示します
- 動画ファイルは `output/` フォルダーに保存されます


### ❓ よくある質問

**Q: 初回の利用にはどれくらい時間がかかりますか?**  
A: 生成時間は動画のフレーム数、ネットワーク状況、AI の推論速度によって異なりますが、通常は数分以内に完了します。

**Q: 動画の出来に満足できない場合はどうすればよいですか?**  
A: 次のことを試してみてください:
1. LLM モデルを変更する(モデルによって台本のスタイルが異なります)
2. 画像サイズとプロンプトのプレフィックスを調整する(画像のスタイルを変更)
3. TTS ワークフローを変更するか、参照音声をアップロードする(音声の仕上がりを変更)
4. 別の動画テンプレートやサイズを試す

**Q: コストはどれくらいかかりますか?**  
A: **このプロジェクトは完全無料での運用に対応しています!**

- **完全無料のソリューション**: LLM に Ollama(ローカル)+ ComfyUI のローカルデプロイ = コスト 0
- **おすすめのソリューション**: LLM に Qwen(非常に低コストでコストパフォーマンスが高い)+ ComfyUI のローカルデプロイ
- **クラウドソリューション**: LLM に OpenAI + 画像に RunningHub(コストは高めですが、ローカル環境が不要)

**選び方の提案**: ローカルに GPU がある場合は完全無料のソリューションを、そうでない場合は Qwen(コストパフォーマンスが高い)の利用をおすすめします


## 🤝 参考にしたプロジェクト

Pixelle-Video の設計は、以下の優れたオープンソースプロジェクトから着想を得ています:

- [Pixelle-MCP](https://github.com/AIDC-AI/Pixelle-MCP) - ComfyUI MCP サーバー。AI アシスタントから ComfyUI を直接呼び出せます
- [MoneyPrinterTurbo](https://github.com/harry0703/MoneyPrinterTurbo) - 優れた動画生成ツール
- [NarratoAI](https://github.com/linyqh/NarratoAI) - 映画解説の自動化ツール
- [MoneyPrinterPlus](https://github.com/ddean2009/MoneyPrinterPlus) - 動画制作プラットフォーム
- [ComfyKit](https://github.com/puke3615/ComfyKit) - ComfyUI ワークフローのラッパーライブラリ

これらのプロジェクトのオープンソース精神に感謝します!🙏


## 💬 コミュニティ

以下の QR コードをスキャンしてコミュニティに参加すると、最新情報や技術サポートを受けられます:

| Discord コミュニティ | WeChat グループ |
| ---- | ---- |
| <img src="resources/discord.png" alt="Discord コミュニティ" width="250" /> | <img src="resources/wechat.png" alt="WeChat グループ" width="250" /> |


## 📢 フィードバックとサポート

- 🐛 **問題が発生した場合**: [Issue](https://github.com/AIDC-AI/Pixelle-Video/issues) を提出してください
- 💡 **機能の提案**: [Feature Request](https://github.com/AIDC-AI/Pixelle-Video/issues) を提出してください
- ⭐ **Star をつける**: このプロジェクトが役に立ったら、ぜひ Star で応援してください!


## 📝 ライセンス

このプロジェクトは Apache License 2.0 の下で公開されています。詳細は [LICENSE](LICENSE) ファイルをご覧ください。

## 📚 研究シリーズ

| フレームワーク  | 論文  |
|:---:|---|
| <img src="https://github.com/HITsz-TMG/VideoClaw/blob/main/FilmAgent-pics/framework.png" width="420" alt="FilmAgent フレームワーク"/> | **[SIGGRAPH Asia 2024] FilmAgent: Automating Virtual Film Production Through a Multi-Agent Collaborative Framework**<br>*Zhenran Xu, Longyue Wang, Jifang Wang, Zhouyi Li, Senbao Shi, Xue Yang, Yiyu Wang, Baotian Hu, Jun Yu, Min Zhang*<br>[[Paper](https://arxiv.org/pdf/2501.12909)] [[GitHub](https://github.com/HITsz-TMG/VideoClaw/blob/main/FilmAgent)] |
| <img src="https://github.com/AIDC-AI/ComfyUI-Copilot/blob/main/assets/Framework-v3.png" width="420" alt="Anim-Director の結果"/> | **[ACL 2025] ComfyUI-Copilot: An Intelligent Assistant for Automated Workflow Development**<br>*Zhenran Xu, Xue Yang, Yiyu Wang, Qingli Hu, Zijiao Wu, Longyue Wang, Weihua Luo, Kaifu Zhang, Baotian Hu, Min Zhang*<br>[[Paper](https://aclanthology.org/2025.acl-demo.61/)] [[GitHub](https://github.com/AIDC-AI/ComfyUI-Copilot)] |
| <img src="https://raw.githubusercontent.com/HITsz-TMG/Anim-Director/main/AniMaker/assets/pipeline.png" width="420" alt="AniMaker パイプライン"/> | **[SIGGRAPH Asia 2025] AniMaker: Multi-Agent Animated Storytelling with MCTS-Driven Clip Generation**<br>*Haoyuan Shi, Yunxin Li, Xinyu Chen, Longyue Wang, Baotian Hu, Min Zhang*<br>[[Paper](https://doi.org/10.1145/3757377.3764009)] [[GitHub](https://github.com/HITsz-TMG/Anim-Director/tree/main/AniMaker)] |


## ⭐ Star 履歴

[![Star 履歴チャート](https://api.star-history.com/svg?repos=AIDC-AI/Pixelle-Video&type=Date)](https://star-history.com/#AIDC-AI/Pixelle-Video&Date)
