# EvoReflect Default Theme

EvoReflect用のデフォルトテーマです。Draculaカラースキームにインスパイアされたダークテーマを提供します。

## インストール

このテーマはEvoReflect本体の `src/themes/default/` にサブモジュールとして含まれています。

```bash
# サブモジュールを含めてクローン
git clone --recursive https://github.com/hiromimie/evoreflect.com.git

# または既存のリポジトリでサブモジュールを初期化
git submodule update --init --recursive
```

## テーマ構造

```
evoreflect.com-theme-default/
├── theme.yaml       # テーマ定義ファイル
├── README.md        # このファイル
└── LICENSE          # MITライセンス
```

## カラーパレット

| カラー | コード | 用途 |
|--------|--------|------|
| Primary | `#bd93f9` | メインアクセント（パープル） |
| Secondary | `#8be9fd` | セカンダリアクセント（シアン） |
| Accent | `#ff79c6` | 強調色（ピンク） |
| Background | `#282a36` | 背景色 |
| Foreground | `#f8f8f2` | 前景色（テキスト） |
| Success | `#50fa7b` | 成功表示（グリーン） |
| Error | `#ff5555` | エラー表示（レッド） |
| Warning | `#ffb86c` | 警告表示（オレンジ） |

## ライセンス

MIT License
