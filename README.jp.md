# PQViewer (Builder)

[English](RAEDME.md)

---

## 概要

**PQViewer (Builder)** は、GitHub Pages 上で動作する WebGL2 ベースの分子・結晶構造ビューア兼ビルダーです。
[PQViewer (Builder)](https://mfukudaqed.github.io/PQViewer_Builder/)のページへブラウザでアクセスするだけで利用でき、
構造データ、ボリュームデータ、ベクトル場・テンソル場をインタラクティブに可視化・編集できます。


## 主な機能

- **ファイル入出力**
  - `xyz`, `cif`, `cube`, `fieldcube`, `scene json` のドラッグ & ドロップ読み込み
  - `xyz`, `cif`, `scene json`, `PNG`, `OBJ`, `CSV` などの出力
  - CIF 読み込み時の occupancy / disorder 設定

- **構造表示・編集**
  - 原子・結合・格子セルの 3D 表示
  - 原子の追加、削除、複製、元素変更、移動、回転、ミラー、反転、整列
  - 手動結合、結合削除、重複原子統合
  - セル編集、スーパーセル生成、周期境界表示
  - 原子グループ化、可視性、不透明度の制御

- **表示・レンダリング**
  - WebGL2 による高速描画
  - impostor / line / mesh 系レンダリング
  - 原子ラベル、結合色、アウトライン、デプスキュー
  - 背景色、テーマ、フォント、アクセントカラーの変更
  - PNG スケール指定付き画像出力

- **等値面・ボリューム可視化**
  - Cube データに基づく等値面表示
  - 正負等値面、透明度、カラーマップ、色 cube による表面着色
  - crop / cap / contour 表示
  - RCP プリセット

- **断面表示**
  - 軸座標、1点 + 法線、3点指定による断面定義
  - 2D スカラー map、等高線、軸目盛り、ラベル、フォント設定
  - 断面上の原子・フィールドグリフ表示
  - 断面用カラーバーと PNG 出力
  - MathJax による注釈テキスト

- **ベクトル場・テンソル場表示**
  - FieldCube データの読み込み
  - 3D arrow, line, tensor principal axes, ellipsoid, star, astroid などの表示
  - magnitude / component / tensor quantity による色付け
  - クリッピング、サンプリング、スケール、カラーバー設定
  - 断面パネルとの連携

- **Lagrange 解析**
  - Lagrange 面の抽出・表示
  - Lagrange 点探索
  - density isosurface による clipping
  - atom pair ごとの面分割と積分
  - OBJ / CSV 出力

- **Surface Builder**
  - Miller 指数に基づく面プレビュー
  - slab 生成、真空層設定、終端解析
  - 吸着サイト生成、pivot への移動、CSV 出力

- **Polyhedra 解析**
  - 中心元素・配位元素・cutoff に基づく配位多面体表示
  - 周期像を考慮した解析
  - OBJ / CSV 出力

- **操作性**
  - Blender 風 / legacy のマウス操作切替
  - pivot marker、view gizmo、rotate gizmo
  - ショートカット編集、import / export、reset
  - UI 検索、折り畳みパネル、リサイズ可能な plot / section / colorbar

## 使い方

1. ブラウザで  [PQViewer (Builder)](https://mfukudaqed.github.io/PQViewer_Builder/)ページを開きます。
1. `xyz`, `cif`, `cube`, `fieldcube`, `scene json` などのファイルをページまたは描画領域にドラッグ & ドロップします。
1. Control Panel から構造編集、等値面、断面、ベクトル/テンソル場、Lagrange 解析などを操作します。
1. 必要に応じて PNG、XYZ、CIF、OBJ、CSV、Scene JSON を出力します。


## 必要環境

- WebGL2 対応のブラウザ
  - Chrome, Edge, Firefox, Safari など
- JavaScript が有効であること
- MathJax CDN へアクセス可能であること（数式注釈を使う場合）

## ライセンス

このプロジェクトは **Mozilla Public License 2.0 (MPL-2.0)** のもとで公開されます。

MPL-2.0 はファイル単位のコピーレフトライセンスです。再配布や改変を行う場合は、MPL-2.0 の条件に従ってください。実際に公開する際は、リポジトリに `LICENSE` ファイルを追加することを推奨します。

## クレジット

- 本 Viewer は **GPT-5.5** を用いて作成されました。
- WebGL2, HTML5 Canvas, JavaScript を用いて実装されています。
- 数式注釈には MathJax を利用します。

---
