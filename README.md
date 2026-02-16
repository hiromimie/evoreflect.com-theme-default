# EvoReflect Default Theme

EvoReflect用のデフォルトテーマです。Draculaカラースキームにインスパイアされたダークテーマと、Solarizedベースのライトテーマを提供し、レスポンシブデザインに対応しています。

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
├── theme.json       # テーマ定義ファイル（JSON形式）
├── gui-theme.json   # GUIテーマ定義（オプション）
├── avatar/          # アバター画像（Issue #1189）
│   ├── user.svg     # ユーザーアバター
│   └── assistant.svg # アシスタントアバター
├── README.md        # このファイル
└── LICENSE          # MITライセンス
```

## 機能

- **Light/Darkモード対応** (Issue #7, #717, #725): ライトモードとダークモードを切り替え可能
- **レスポンシブデザイン対応** (Issue #716): モバイル、タブレット、デスクトップに最適化されたレイアウト
- **ハイブリッドテーマ**: CLI（terminal）とGUI（Web）の両方で使用可能
- **カスタムアバター** (Issue #1189): テーマカラーに合わせたSVGアバター画像を同梱

## カラーパレット

### ダークモード (Dracula ベース)

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

### ライトモード (Solarized ベース)

CLIテーマとGUIテーマの両方でSolarized Lightをベースにした暖色系のクリームカラーパレットを採用しています（Issue #7）。

#### CLIテーマ

| カラー | コード | 用途 |
|--------|--------|------|
| Primary | `#268bd2` | メインアクセント（ブルー） |
| Secondary | `#2aa198` | セカンダリアクセント（シアン） |
| Accent | `#d33682` | 強調色（マゼンタ） |
| Background | `#fdf6e3` | 背景色（クリーム） |
| Foreground | `#657b83` | 前景色（テキスト） |
| Success | `#859900` | 成功表示（グリーン） |
| Error | `#dc322f` | エラー表示（レッド） |
| Warning | `#b58900` | 警告表示（イエロー） |

#### GUIテーマ

目に優しく見やすい配色を採用しています。Solarized Light推奨の本文テキスト色（`#657b83`）を使用し、コンポーネント専用のCSS変数も定義しています。

| カラー | コード | 用途 |
|--------|--------|------|
| Background Primary | `#fdf6e3` | 背景色（クリーム） |
| Background Secondary | `#eee8d5` | セカンダリ背景（サイドバー/ヘッダ/フッタ） |
| Foreground Primary | `#657b83` | 前景色（本文テキスト） |
| Foreground Secondary | `#586e75` | セカンダリ前景色 |
| Accent Primary | `#cb4b16` | メインアクセント（オレンジ） |
| Accent Secondary | `#d33682` | セカンダリアクセント（マゼンタ） |
| Success | `#859900` | 成功表示（グリーン） |
| Error | `#dc322f` | エラー表示（レッド） |
| Warning | `#b58900` | 警告表示（イエロー） |

**Skeleton UI対応CSS変数（全グラデーション）:**

GUIのサイドバー、ヘッダ、フッタ、パネル等の背景色を正しく適用するため、Skeleton UIが認識する形式の全グラデーション変数を定義しています。

- `--color-surface-50` ～ `--color-surface-900`: 背景色グラデーション（Solarized Lightベース）
- `--color-primary-50` ～ `--color-primary-900`: プライマリ色グラデーション（オレンジ系）
- `--color-secondary-50` ～ `--color-secondary-900`: セカンダリ色グラデーション（マゼンタ系）

## レスポンシブデザイン

このテーマは、以下のブレークポイントで最適化されています：

| デバイス | ブレークポイント | 説明 |
|---------|----------------|------|
| Mobile | `< 768px` | スマートフォン向け |
| Tablet | `768px - 1439px` | タブレット向け |
| Desktop | `>= 1440px` | デスクトップ向け |

### レスポンシブ機能

- **サイドバー自動折りたたみ**: モバイル・タブレットでは自動的にサイドバーが折りたたまれます
- **可変フォントサイズ**: 画面サイズに応じてフォントサイズが最適化されます
- **フレキシブルレイアウト**: チャットエリアやコンテンツ幅が画面サイズに応じて調整されます

## ライセンス

MIT License
