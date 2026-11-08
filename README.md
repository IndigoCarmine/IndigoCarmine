<div align="center">

#  IndigoCarmine

研究で使う化学ソフトウェアを作っています。<br>
I build chemistry software for my research.

<a href="https://skillicons.dev"><img src="https://skillicons.dev/icons?i=rust,python,dart,blender,linux&theme=light" alt="Rust, Python, Dart, Blender, Linux"></a>

</div>


# 最近の作業 / Recent work


##  Open DrawChemistry

<table>
<tr>
<td width="120" align="center" valign="top">
<a href="https://github.com/IndigoCarmine/open_draw_chemistry"><img src="https://raw.githubusercontent.com/IndigoCarmine/open_draw_chemistry/master/resources/icon.png" width="100" alt="Open DrawChemistry icon"></a>
</td>
<td valign="top">

**[open_draw_chemistry](https://github.com/IndigoCarmine/open_draw_chemistry)** — 無料・オープンソースの構造式エディタ。ChemDraw ファイルを開け、命名・解析・3D 構築までできます。<br>
A free, open-source structure editor. It opens ChemDraw files and can name and analyse structures and build them in 3D.

[![Website](https://img.shields.io/badge/website-open__draw__chemistry-7c5cff?logo=googlechrome&logoColor=white)](https://indigocarmine.github.io/open_draw_chemistry-site/en/)
[![Release](https://img.shields.io/github/v/release/IndigoCarmine/open_draw_chemistry?color=7c5cff)](https://github.com/IndigoCarmine/open_draw_chemistry/releases/latest)
![Rust](https://img.shields.io/badge/Rust-000000?logo=rust&logoColor=white)
![Platforms](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey)
![License](https://img.shields.io/badge/license-AGPL--3.0-blue)

</td>
<td width="220" align="center" valign="top">
<img src="https://raw.githubusercontent.com/IndigoCarmine/open_draw_chemistry/master/docs/images/analysis-panel.png" width="200" alt="Analysis panel: formula, exact mass, m/z, elemental analysis and IUPAC name">
</td>
</tr>
</table>


## ⌬ 化学構造の描画まわり / Drawing chemical structures

|  Repository | 説明 / Description |
|---|---|
|  [**chembuider-rs**](https://github.com/IndigoCarmine/chembuider-rs) | Open DrawChemistry の中核になっている、egui の 2D 構造式エディタウィジェット。<br>The egui 2D structure-editor widget at the core of Open DrawChemistry. |
| [**cdx_file_rs**](https://github.com/IndigoCarmine/cdx_file_rs) | ChemDraw の CDX/CDXML ファイルを読み書き・描画する Pure Rust ライブラリ。<br>A pure-Rust library for reading, writing and rendering ChemDraw CDX/CDXML files. |
| [**moleucle_3dview_rs**](https://github.com/IndigoCarmine/moleucle_3dview_rs) | egui 上で動く wgpu の 3D 分子ビューア。MD サイズの系まで扱えます。<br>A wgpu 3D molecule viewer that runs inside egui and scales to MD-sized systems. |
|[**molecule_optimizer_rs**](https://github.com/IndigoCarmine/molecule_optimizer_rs) | RDKit から UFF・MMFF94・DistGeom を移植した Pure Rust の分子力学（構造最適化、配座探索、スキャン）。<br>Pure-Rust molecular mechanics (optimization, conformer search, scans) with UFF, MMFF94 and DistGeom ported from RDKit. |
|  [**acauda-embed**](https://github.com/IndigoCarmine/acauda-embed) | 外部アプリで編集したオブジェクトを文書に埋め込むための IPC プロトコル（COM 不使用）。<br>An IPC protocol for embedding objects edited in external apps into documents, without COM. |

<p align="center">
<img src="https://raw.githubusercontent.com/IndigoCarmine/cdx_file_rs/master/sample_img/png/Reaction.png" width="520" alt="A reaction scheme rendered by cdx_file_rs"><br>
<sub>cdx_file_rs で描画した ChemDraw ファイル / A ChemDraw file rendered by cdx_file_rs</sub>
</p>


## 🧬 分子動力学（GROMACS） / Molecular dynamics

| | Repository | 説明 / Description |
|:-:|---|---|
| 🐱 | [**manul_cat_rs**](https://github.com/IndigoCarmine/manul_cat_rs) | GROMACS のトポロジー（.top）とインデックス（.ndx）の分子間相互作用の設定を GUI で確認するツール。<br>A GUI for checking the intermolecular interaction settings in GROMACS .top and .ndx files. |
| 🛡️ | [**gmx_harness**](https://github.com/IndigoCarmine/gmx_harness) | EM → NVT → NPT → 本計算、Martini、AWH、BAR などの計算一式をファイルとスクリプトとして生成。`plan → preview → write` の流れで書き込み前に衝突を確認するので、AI エージェントも安全に扱えます。<br>Generates complete simulation pipelines as files and scripts. A `plan → preview → write` flow checks for conflicts before writing, so AI agents can use it safely. |


## 📊 解析・図 / Analysis and figures

| | Repository | 説明 / Description |
|:-:|---|---|
| 📈 | [**fit_it**](https://github.com/IndigoCarmine/fit_it) | デスクトップのカーブフィッティングアプリ。<br>A desktop curve-fitting application. |
| 🖼️ | [**figs_rs**](https://github.com/IndigoCarmine/figs_rs) | 論文の図やポスターを、TOML で構造と制約を書いて組むツール（開発中）。<br>Composes paper figures and posters from structure and constraints written in TOML (in development). |


# 🤖 AIとCodingに対する宣誓

ここに置いてあるコードの一部はClaude Codeに書かせています。Commitを確認いただければ明らかでしょう。私もプログラマーではなくなってしまったのだと思います。Agentic Codingの速度で人力のレビューするのは不可能で、それをする必要もないと思います。そこで、開発をAIに合わせるために意図的にレビューしていません。バグが有っても困らないものと、問題があれば使用感で気づけるものはコードを読んでいません。

GUIのレイアウト、CLIの出力整形、図の見た目、Blenderのスクリプト、ビルド周りは全部AIに任せていて、動いたらそれで終わりにしています。おかしければ実行した時点で気づくので。一方で、MDの計算設定の生成や解析、熱力学モデルのフィッティング、データの前処理は、生成させたあとで式のレベルまで自分で読んでいます。AIのPRはできるだけ厳しく審査していきます。中間的な問題には、テストを活用して確認しています。

以上は自分のリポジトリでの話です。**ほかのOSSに関わる場合は、内容によらず確実に自分で確認していきます。**


# 🤖 My policy on AI and code

Some of the code here was written by Claude Code, as the commit history makes clear. As agentic coding has advanced, reviewing everything by hand has become impossible, so I deliberately skip review in places in order to keep development fast. There is only one criterion for what gets reviewed: whether a bug would fail visibly.

GUI layout, CLI output formatting, how figures look, Blender scripts, and build tooling are left entirely to the AI, and once it runs I consider it done. Anything wrong shows up the moment I run it. Generating and analyzing MD simulation settings, fitting thermodynamic models, and preprocessing data are a different matter. I read those myself, down to the equations, after they are generated, and I review the AI's pull requests as strictly as I can. Reading everything doesn't scale as the code grows, though, so I put more weight on keeping the work in a form I can verify by independent calculation. For the cases in between, I check that the tests assert what I actually expect.

All of the above applies to my own repositories. **When I contribute to someone else's open source project, I check the code myself without exception.**


# 📈 Stats

![](http://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=IndigoCarmine&theme=github)

![](http://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=IndigoCarmine&theme=github) ![](http://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=IndigoCarmine&theme=github)
![](http://github-profile-summary-cards.vercel.app/api/cards/stats?username=IndigoCarmine&theme=github) ![](http://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=IndigoCarmine&theme=github&utcOffset=8)
