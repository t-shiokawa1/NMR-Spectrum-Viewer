# NMR Spectrum Viewer

[English](#english) | [日本語](#日本語)

## English

A single-file browser application for viewing and analyzing Bruker NMR data.<br>
No installation or server is required—just open `index.html` in a browser.

### Features

- Load raw Bruker FID and processed spectrum data
- Overlay or stack up to 10 spectra
- Adjust phase, window functions, zero filling, and display intensity
- Calibrate the ppm axis manually or from residual solvent peaks
- Detect peaks, integrate signals, and analyze multiplets and coupling constants
- Add text, marks, shaded regions, images, and magnified views
- Reference possible impurities and display their positions on the spectrum
- Export PNG images, spectrum CSV files, and analysis reports
- Save and restore work sessions as JSON
- English and Japanese interfaces with dark and light themes

### Supported data

The viewer accepts a Bruker dataset containing either of the following:

```text
<dataset>/
├── fid
├── acqus
└── pdata/
    └── 1/
        ├── 1r
        └── procs
```

- Raw data: `fid` + `acqus`
- Processed data: `pdata/1/1r` + `pdata/1/procs`

### Getting started

1. Open `index.html` in Chrome or Edge.
2. Drag and drop a Bruker dataset folder—the numbered expno folder—onto the application.
3. Use the tools above the spectrum for peak detection, integration, calibration, and other analysis.
4. Use the **Export** menu to save images, CSV data, analysis reports, or sessions.

You can also drop multiple dataset folders, or a parent folder containing them, to load several spectra at once.

### Basic controls

| Action | Result |
| --- | --- |
| Scroll over the spectrum | Change display intensity |
| Scroll over the δ axis | Zoom the ppm range |
| Drag the δ axis | Pan the ppm range |
| Drag over the spectrum | Zoom to a region |
| Right-drag / Shift + drag | Pan the ppm range |
| Double-click | Show the full spectrum |
| `Ctrl/Cmd + Z` | Undo |
| `Ctrl/Cmd + Y` | Redo |

More shortcuts are available under **Settings → Keyboard** in the application.

### Data privacy

All spectrum loading and analysis take place locally in your browser. The NMR data you open is not uploaded to an external server.

---

## 日本語

Bruker形式のNMRデータをブラウザ上で表示・解析する、単一HTMLファイルのビューアです。<br>
インストールやサーバーは不要で、`index.html` をブラウザで開くだけで使用できます。

### 主な機能

- Brukerの生FIDおよび処理済みスペクトルの読み込み
- 複数スペクトルの重ね表示・縦並び表示（最大10件）
- 位相、窓関数、ゼロフィリング、表示強度の調整
- ppm軸の校正と残留溶媒ピークによる自動校正
- ピーク検出、積分、多重線・カップリング定数の解析
- テキスト、マーク、塗りつぶし、画像、拡大図などの注釈
- 不純物候補の参照・スペクトル上への表示
- PNG画像、CSVスペクトル、CSV解析レポートの出力
- 作業状態のJSON保存・再読み込み
- 日本語・英語表示、ダーク・ライトテーマ

### 対応データ

次のいずれかを含むBrukerデータセットを読み込めます。

```text
<dataset>/
├── fid
├── acqus
└── pdata/
    └── 1/
        ├── 1r
        └── procs
```

- 生データ：`fid` + `acqus`
- 処理済みデータ：`pdata/1/1r` + `pdata/1/procs`

### 使い方

1. `index.html` をChromeまたはEdgeで開きます。
2. Brukerのデータセットフォルダ（番号付きのexpnoフォルダ）を画面へドラッグ＆ドロップします。
3. スペクトル上部のツールを使ってピーク検出、積分、校正などを行います。
4. 「出力」メニューから画像、CSV、解析レポート、セッションを保存できます。

複数のデータセットフォルダ、またはそれらを含む親フォルダもまとめてドロップできます。

### 基本操作

| 操作 | 内容 |
| --- | --- |
| スペクトル上でスクロール | 表示強度の変更 |
| δ軸上でスクロール | ppm範囲の拡大・縮小 |
| δ軸をドラッグ | ppm範囲の移動 |
| スペクトル上をドラッグ | 範囲ズーム |
| 右ドラッグ／Shift + ドラッグ | ppm範囲の移動 |
| ダブルクリック | スペクトル全体を表示 |
| `Ctrl/Cmd + Z` | 元に戻す |
| `Ctrl/Cmd + Y` | やり直す |

詳しいショートカットは、アプリ内の「設定」→「キーボード」で確認できます。

### データの取り扱い

スペクトルの読み込みと解析はブラウザ内で行われます。読み込んだNMRデータが外部サーバーへアップロードされることはありません。

---

## Repository contents

```text
index.html   # Application
README.md    # Documentation
```
