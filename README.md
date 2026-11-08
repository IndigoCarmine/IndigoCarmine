

# AIとCodingに対する宣誓

ここに置いてあるコードの一部はClaude Codeに書かせています。Commitを確認いただければ明らかでしょう。私もプログラマーではなくなってしまったのだと思います。Agentic Codingの速度で人力のレビューするのは不可能で、それをする必要もないと思います。そこで、開発をAIに合わせるために意図的にレビューしていません。バグが有っても困らないものと、問題があれば使用感で気づけるものはコードを読んでいません。

GUIのレイアウト、CLIの出力整形、図の見た目、Blenderのスクリプト、ビルド周りは全部AIに任せていて、動いたらそれで終わりにしています。おかしければ実行した時点で気づくので。一方で、MDの計算設定の生成や解析、熱力学モデルのフィッティング、データの前処理は、生成させたあとで式のレベルまで自分で読んでいます。AIのPRはできるだけ厳しく審査していきます。中間的な問題には、テストを活用して確認しています。

以上は自分のリポジトリでの話です。**ほかのOSSに関わる場合は、内容によらず確実に自分で確認していきます。**


# My policy on AI and code

Some of the code here was written by Claude Code, as the commit history makes clear. As agentic coding has advanced, reviewing everything by hand has become impossible, so I deliberately skip review in places in order to keep development fast. There is only one criterion for what gets reviewed: whether a bug would fail visibly.

GUI layout, CLI output formatting, how figures look, Blender scripts, and build tooling are left entirely to the AI, and once it runs I consider it done. Anything wrong shows up the moment I run it. Generating and analyzing MD simulation settings, fitting thermodynamic models, and preprocessing data are a different matter. I read those myself, down to the equations, after they are generated, and I review the AI's pull requests as strictly as I can. Reading everything doesn't scale as the code grows, though, so I put more weight on keeping the work in a form I can verify by independent calculation. For the cases in between, I check that the tests assert what I actually expect.

All of the above applies to my own repositories. **When I contribute to someone else's open source project, I check the code myself without exception.**


# 最近の作業

ここ数か月は、研究で使う化学ソフトウェアをRustで作り直すことに時間を使っています。

**化学構造の描画まわり**
- [open_draw_chemistry](https://github.com/IndigoCarmine/open_draw_chemistry) — 無料・オープンソースの構造式エディタ。ChemDrawファイルを開け、命名・解析・3D構築までできます（[Webサイト](https://indigocarmine.github.io/open_draw_chemistry-site/en/)）。
- [chembuider-rs](https://github.com/IndigoCarmine/chembuider-rs) — 上のエディタの中核になっている、eguiの2D構造式エディタウィジェット。
- [cdx_file_rs](https://github.com/IndigoCarmine/cdx_file_rs) — ChemDrawのCDX/CDXMLファイルを読み書き・描画するPure Rustライブラリ。
- [moleucle_3dview_rs](https://github.com/IndigoCarmine/moleucle_3dview_rs) — egui上で動くwgpuの3D分子ビューア。MDサイズの系まで扱えます。
- [molecule_optimizer_rs](https://github.com/IndigoCarmine/molecule_optimizer_rs) — RDKitからUFF・MMFF94・DistGeomを移植したPure Rustの分子力学（構造最適化、配座探索、スキャン）。
- [openbabel_rs](https://github.com/IndigoCarmine/openbabel_rs) — OpenBabelのRustバインディング。
- [acauda-embed](https://github.com/IndigoCarmine/acauda-embed) — 外部アプリで編集したオブジェクトを文書に埋め込むためのIPCプロトコル（COM不使用）。

**分子動力学（GROMACS）**
- [manul_cat_rs](https://github.com/IndigoCarmine/manul_cat_rs) — GROMACSのトポロジー（.top）とインデックス（.ndx）の分子間相互作用の設定をGUIで確認するツール。
- [gmx_harness](https://github.com/IndigoCarmine/gmx_harness) — EM→NVT→NPT→本計算、Martini、AWH、BARなどの計算一式をファイルとスクリプトとして生成するライブラリ。AIエージェントが安全に扱えるよう、`plan → preview → write` の流れで書き込み前に衝突を確認します。

**解析・図**
- [fit_it](https://github.com/IndigoCarmine/fit_it) — デスクトップのカーブフィッティングアプリ。
- [figs_rs](https://github.com/IndigoCarmine/figs_rs) — 論文の図やポスターを、TOMLで構造と制約を書いて組むツール（開発中）。


# Recent work

Over the past few months I have been rebuilding the chemistry software I use for research in Rust.

**Drawing chemical structures**
- [open_draw_chemistry](https://github.com/IndigoCarmine/open_draw_chemistry) — a free, open-source structure editor. It opens ChemDraw files and can name and analyse structures and build them in 3D ([website](https://indigocarmine.github.io/open_draw_chemistry-site/en/)).
- [chembuider-rs](https://github.com/IndigoCarmine/chembuider-rs) — the egui 2D structure-editor widget at the core of the editor above.
- [cdx_file_rs](https://github.com/IndigoCarmine/cdx_file_rs) — a pure-Rust library for reading, writing and rendering ChemDraw CDX/CDXML files.
- [moleucle_3dview_rs](https://github.com/IndigoCarmine/moleucle_3dview_rs) — a wgpu 3D molecule viewer that runs inside egui and scales to MD-sized systems.
- [molecule_optimizer_rs](https://github.com/IndigoCarmine/molecule_optimizer_rs) — pure-Rust molecular mechanics (geometry optimization, conformer search, scans), with UFF, MMFF94 and DistGeom ported from RDKit.
- [openbabel_rs](https://github.com/IndigoCarmine/openbabel_rs) — Rust bindings to OpenBabel.
- [acauda-embed](https://github.com/IndigoCarmine/acauda-embed) — an IPC protocol for embedding objects edited in external applications into documents, without COM.

**Molecular dynamics (GROMACS)**
- [manul_cat_rs](https://github.com/IndigoCarmine/manul_cat_rs) — a GUI for checking the intermolecular interaction settings in GROMACS topology (.top) and index (.ndx) files.
- [gmx_harness](https://github.com/IndigoCarmine/gmx_harness) — generates complete simulation pipelines (EM → NVT → NPT → production, Martini, AWH, BAR) as files and scripts. It follows a `plan → preview → write` flow that checks for conflicts before writing anything, so AI agents can use it safely.

**Analysis and figures**
- [fit_it](https://github.com/IndigoCarmine/fit_it) — a desktop curve-fitting application.
- [figs_rs](https://github.com/IndigoCarmine/figs_rs) — composes paper figures and posters from structure and constraints written in TOML (in development).


![](http://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=IndigoCarmine&theme=github)

![](http://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=IndigoCarmine&theme=github) ![](http://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=IndigoCarmine&theme=github)
![](http://github-profile-summary-cards.vercel.app/api/cards/stats?username=IndigoCarmine&theme=github) ![](http://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=IndigoCarmine&theme=github&utcOffset=8)
