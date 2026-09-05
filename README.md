# skills

AI エージェント用の skill 置き場です。[skills.sh](https://skills.sh/) CLI でインストールできます。

> 本リポジトリの business-model-diagram skill は、株式会社図解総研の「ビジネスモデル図解ツールキット」(©図解総研) の方法に基づいています。同ツールキット配布版 Ver.4.2 (2020-06-10) は CC BY 4.0 で配布されており、本 skill はその方法に学んで独自に記述したものです。ツールキットの素材 (画像・図形データ) は複製していません。

## インストール

```bash
npx skills add halsk/skills --skill business-model-diagram
```

対応エージェント: Claude Code / Cursor / GitHub Copilot / Windsurf ほか (skills.sh CLI が対応するもの)

## 利用可能なスキル

| スキル | 説明 |
|--------|------|
| business-model-diagram | 指定された資料を典拠に、ビジネスモデル図解ツールキット (©図解総研, CC BY 4.0) の方法に基づくビジネスモデル図解を自己完結 HTML/SVG で作成する |

### business-model-diagram の特徴

この skill の背骨は「捏造させないこと」です。資料に書かれていない主体やカネの流れを、もっともらしく作ってしまうのがこの種の道具の最大の失敗です。そこで次を義務づけています。

- 主体・矢印・補足の 1 つ 1 つに典拠 (ファイル名や URL) を持たせ、典拠のないものは図に載せない
- 分からないマスは空のままにする。埋めるために推測を置かない (ツールキット自身が「全部埋まる必要はない」と明記しています)
- 推測を載せる場合は点線と「推定」の明示を必須にする
- 図と対で根拠表 (要素・典拠・確度) を必ず出す。図だけを出さない

出力は外部 CDN・フォントに依存しない 1 ファイルの HTML/SVG で、明るい配色・暗い配色の両方で読めます。

## 出所と権利関係

- 方法の出所: 「ビジネスモデル図解ツールキット 配布版」Ver.4.2 (2020-06-10)、©株式会社図解総研。同版のスライド内に CC BY 4.0 (表示 4.0 国際) と商用利用可の記載があります。
- 同ツールキットは現在、図解総研から有償で販売されています ([図解総研の製品ページ](https://zukai.co/blogs/project/bizmodel_toolkit))。本 skill が依拠するのは CC BY 4.0 で配布された上記の版です。
- 本 skill の文書とテンプレート (`template.html`) はすべて独自に書き起こしたもので、ツールキットのファイル・素材は本リポジトリに含まれていません。再配布もしていません。
- 詳細は [skills/business-model-diagram/SOURCE.md](skills/business-model-diagram/SOURCE.md) を参照してください。

## ライセンス

本リポジトリの内容は MIT License ([LICENSE](LICENSE)) で利用できます。business-model-diagram の方法は ©図解総研 (CC BY 4.0) に帰属します。出力する図解には出所の表示を必ず含めてください。
