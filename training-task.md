# GitHub / Next.js 基本操作確認課題

## 1. 目的

この課題は、本番実装に入る前に、実装担当者がGitHubとNext.js / Reactの基本操作をできるか確認するためのものです。

今回確認する内容は以下です。

- GitHubのリポジトリをVS Codeで自分のPCにcloneできる
- `README.md`を編集できる
- VS CodeのSource Controlで変更状況を確認できる
- VS CodeのSource Controlで変更ファイルをステージできる
- VS Codeでcommitできる
- VS CodeのPublish BranchまたはSync ChangesでGitHubに変更を送れる
- Pull Requestを作成できる
- `npm install`で必要なパッケージを入れられる
- `npm run dev`でNext.jsを起動できる
- ブラウザでNext.jsの画面を確認できる
- `page.tsx`の文字を変更できる
- 変更内容がブラウザ画面に反映されることを確認できる

この課題では、本格的なゲーム画面の実装は行いません。

今回作るゲームは、一人称視点の暗号推理ゲームです。ただし、この課題ではゲーム機能は作らず、開発に参加するための最低限の操作確認だけを行います。

## 2. 対象者

この課題の対象者は、以下の実装担当者です。

- @かまぼこ(本物)
- @ほっそー

プロダクト開発メンバーは以下です。

- @ly(らい)：PM、音
- @ささかまぼこ。：UI、絵
- @かまぼこ(本物)：実装
- @ほっそー：実装

実装担当者は初心者想定です。わからないことがあれば、途中で報告してください。

## 3. 期限

期限は以下です。

```text
[PMが記入：例 2026/07/01 23:59まで]
```

期限までにPull Requestを作成し、提出先にPull RequestのURLを送ってください。

## 4. 課題一覧

今回やる課題は以下です。

- GitHubリポジトリをVS Codeでcloneする
- VS Codeで作業用ブランチを作る
- `npm install`を実行する
- `npm run dev`を実行する
- ブラウザでNext.js画面を確認する
- `README.md`に自分の名前を追記する
- `page.tsx`の表示文字を変更する
- 変更した文字がブラウザに反映されることを確認する
- Source Controlで変更状況を確認する
- Source Controlで変更ファイルをステージする
- VS Codeでcommitする
- Publish BranchまたはSync ChangesでGitHubに変更を送る
- Pull Requestを作成する

今回やらなくてよいことは以下です。

- 本格的なゲーム画面実装
- コンポーネント分割
- propsの利用
- stateの利用
- onClickの利用
- 正誤判定
- リザルト表示

## 5. 作業手順

### 5.1 リポジトリをcloneする

まず、GitHubのリポジトリURLを確認してください。

```text
[PMが記入：GitHubリポジトリURL]
```

VS Codeを開き、Command Paletteから `Git: Clone` を選びます。

表示された入力欄に、PMから共有されたGitHubリポジトリURLを貼り付けます。

clone先のフォルダを選び、cloneが終わったらVS Codeでリポジトリを開きます。

### 5.2 作業用ブランチを作る

VS Code左下のブランチ名をクリックし、`Create new branch` を選びます。

ブランチ名は `work/担当者-training` の形にします。

例：@かまぼこ(本物) の場合

```text
work/kamaboko-training
```

例：@ほっそー の場合

```text
work/hosso-training
```

### 5.3 必要なパッケージを入れる

Next.jsを動かすために必要なパッケージを入れます。

```bash
npm install
```

完了まで少し時間がかかる場合があります。

エラーが出ずに終わればOKです。

### 5.4 Next.jsを起動する

開発サーバーを起動します。

```bash
npm run dev
```

成功すると、ターミナルに以下のようなURLが表示されます。

```text
http://localhost:3000
```

ブラウザで以下を開いてください。

```text
http://localhost:3000
```

Next.jsの画面が表示されればOKです。

`npm run dev`を実行しているターミナルは、Next.jsを動かし続けるために使います。Git操作はターミナルではなく、VS CodeのSource Controlで行ってください。

### 5.5 README.mdを編集する

`README.md`を開き、自分の名前を追記してください。

追記する場所が決まっていない場合は、ファイルの一番下に以下のように追記してください。

@かまぼこ(本物) の場合：

```md
## 基本操作確認

- @かまぼこ(本物)：確認済み
```

@ほっそー の場合：

```md
## 基本操作確認

- @ほっそー：確認済み
```

すでに `## 基本操作確認` がある場合は、見出しを増やさず、自分の名前だけを追加してください。

### 5.6 page.tsxを編集する

`page.tsx`を探して開きます。

よくある場所は以下のどちらかです。

```text
src/app/page.tsx
```

```text
app/page.tsx
```

ファイル内に、画面に表示されている文字があります。その文字を以下のように変更してください。

```text
GitHub / Next.js 基本操作確認中
```

自分の名前も入れる場合は、以下のようにしてもOKです。

```text
GitHub / Next.js 基本操作確認中：@かまぼこ(本物)
```

または：

```text
GitHub / Next.js 基本操作確認中：@ほっそー
```

この課題では、見た目を整える必要はありません。文字が変わればOKです。

### 5.7 ブラウザで変更を確認する

ブラウザで以下を開いている状態にします。

```text
http://localhost:3000
```

`page.tsx`で変更した文字が画面に表示されていることを確認してください。

表示が変わらない場合は、以下を確認してください。

- ファイルを保存したか
- `npm run dev`が止まっていないか
- 開いているURLが `http://localhost:3000` か
- 編集したファイルが `page.tsx` か

### 5.8 VS Codeで変更状況を確認する

VS Code左側のSource Controlを開きます。

`README.md`と`page.tsx`がChangesに表示されていることを確認してください。

### 5.9 変更ファイルをステージする

Source Controlで、`README.md`と`page.tsx`の横にある `+` を押してステージします。

ステージできると、ファイルがStaged Changesに移動します。

### 5.10 VS Codeでcommitする

Source ControlのMessage欄にcommitメッセージを書きます。

```text
docs: GitHubとNext.jsの基本操作確認
```

その後、Commitボタンを押します。

### 5.11 GitHubへ変更を送る

VS CodeのSource Controlで、Publish BranchまたはSync Changesを押します。

`work/kamaboko-training` の場合：

```text
work/kamaboko-training
```

`work/hosso-training` の場合：

```text
work/hosso-training
```

自分で別のブランチ名にした場合は、そのブランチ名に合わせてください。

### 5.12 Pull Requestを作成する

GitHubのリポジトリページを開きます。

push後に `Compare & pull request` のようなボタンが表示されたら、それを押してください。

Pull Requestの向きは以下にします。

```text
base: [PMが記入：例 main]
compare: 自分の作業ブランチ
```

Pull Requestのタイトルは以下にしてください。

```text
docs: GitHubとNext.jsの基本操作確認
```

Pull Requestの本文には以下を書いてください。

```md
## 確認したこと

- README.mdを編集しました
- npm installを実行しました
- npm run devでNext.jsを起動しました
- ブラウザで画面を確認しました
- page.tsxの文字を変更しました
- 変更が画面に反映されることを確認しました
```

作成できたら、Pull RequestのURLを提出してください。

## 6. 使用するコマンドとVS Code操作

Git操作はVS CodeのSource Controlで行います。

ターミナルで使用するコマンドは以下です。

```bash
npm install
```

```bash
npm run dev
```

VS Codeで行うGit操作は以下です。

- `Git: Clone` でリポジトリをcloneする
- 左下のブランチ名から `work/担当者-training` ブランチを作る
- Source Controlで変更ファイルを確認する
- Source Controlで変更ファイルをステージする
- Source Controlでcommitする
- Publish BranchまたはSync ChangesでGitHubへ送る
- GitHub上でPull Requestを作成する

この課題では、`git clone`、`git switch`、`git status`、`git add`、`git commit`、`git push` は使いません。

## 7. 完了条件

以下をすべて満たしたら、この課題は完了です。

- VS CodeでGitHubリポジトリをcloneできている
- VS Codeで自分用の `work/*` ブランチを作成できている
- `npm install`が完了している
- `npm run dev`でNext.jsを起動できている
- ブラウザで `http://localhost:3000` を開けている
- `README.md`に自分の名前を追記している
- `page.tsx`の表示文字を変更している
- 変更した文字がブラウザ上で確認できている
- Source Controlで変更状態を確認している
- Source Controlで変更ファイルをステージしている
- VS Codeでcommitしている
- Publish BranchまたはSync ChangesでGitHubに変更を送っている
- Pull Requestを作成している
- Pull RequestのURLを提出している

## 8. 提出物

提出するものは以下です。

- 作成したPull RequestのURL
- Next.js画面を開いたスクリーンショット
- `page.tsx`の文字変更が反映された画面のスクリーンショット

提出先は以下です。

```text
[PMが記入：例 Discordの開発チャンネル / Googleスプレッドシート / DM]
```

提出時のメッセージ例：

```text
GitHub / Next.js 基本操作確認課題が完了しました。

Pull Request：
[ここにURL]

確認したこと：
- npm install 実行済み
- npm run dev 実行済み
- ブラウザ表示確認済み
- README.md 編集済み
- page.tsx 文字変更済み
```

## 9. 評価基準

この課題では、コードの完成度やゲーム画面の見た目は評価しません。

評価するのは以下です。

- 指示通りにVS Codeでリポジトリをcloneできているか
- 自分用の `work/*` ブランチをVS Codeで作れているか
- `npm install`を実行できているか
- `npm run dev`を実行できているか
- ブラウザでNext.js画面を確認できているか
- `README.md`を編集できているか
- `page.tsx`を編集できているか
- 編集内容が画面に反映されることを確認できているか
- Source Controlで変更状況を確認できているか
- Source Controlで変更ファイルをステージできているか
- VS Codeでcommitできているか
- Publish BranchまたはSync ChangesでGitHubに変更を送れているか
- Pull Requestを作成できているか
- 詰まったときに状況を説明して報告できるか

以下は評価対象外です。

- 画面デザインの良さ
- ゲームらしい見た目になっているか
- コンポーネント分割ができているか
- Reactのstateを使えているか
- クリック処理を作れているか
- ゲームの正誤判定を作れているか

## 10. 詰まったときの報告方法

詰まった場合は、長時間ひとりで悩み続けずに報告してください。

報告先は以下です。

```text
[PMが記入：例 @ly(らい) にDiscordで連絡]
```

報告するときは、以下の情報を送ってください。

- どの手順で止まったか
- 実行したコマンド
- 表示されたエラーメッセージ
- 今の画面のスクリーンショット
- 自分で試したこと

報告例：

```text
手順5.3の npm install で止まりました。

実行したコマンド：
npm install

表示されたエラー：
[ここにエラー文を貼る]

試したこと：
ターミナルを開き直してもう一度実行しましたが、同じエラーが出ました。

スクリーンショット：
[画像を添付]
```

エラー文は省略せず、できるだけそのまま貼ってください。
