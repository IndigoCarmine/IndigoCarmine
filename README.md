<div align="center">

# IndigoCarmine

分子集合体（超分子）化学の研究をしています。分子を設計し、集合させ、その構造と熱力学を調べるまでの各段階で使うアプリを自作しています。<br>
I work on molecular assembly (supramolecular) chemistry, and I build my own apps for each step from designing molecules to studying how they assemble.

<a href="https://skillicons.dev"><img src="https://skillicons.dev/icons?i=rust,python,dart,linux&theme=light" alt="Rust, Python, Dart, Linux"></a>

</div>


# 最近の作業 / Recent work

## 1. 集合体の熱力学を解析し、図にする / Analysing assembly thermodynamics and making figures

<table>
<tr>
<td width="100" align="center"></td>
<td>

**[fit_it](https://github.com/IndigoCarmine/fit_it)** — 超分子重合のデータを解析するためのデスクトップのフィッティングアプリ。isodesmic・cooperative（核サイズ N、温度依存・濃度依存）・両経路の競合モデルを備え、複数濃度の冷却曲線をグローバルフィットして ΔH・ΔS・核形成ペナルティを誤差付きで求めます。JASCO の UV-Vis データ（温度スキャン）を直接読み込めます。<br>
A desktop fitting app for supramolecular polymerization. It has isodesmic, cooperative (nucleus size N, temperature- and concentration-dependent) and competing-pathway models, and globally fits cooling curves at several concentrations to give ΔH, ΔS and the nucleation penalty with errors. It reads JASCO UV-Vis temperature scans directly.

</td>
</tr>
<tr>
<td width="100" align="center"></td>
<td>

**[sp_fitting_models](https://github.com/IndigoCarmine/sp_fitting_models)** — 同じ超分子重合モデル群の Python ライブラリ版。<br>
The same supramolecular polymerization models as a Python library.

</td>
</tr>
</table>


<p align="center">
<a href="https://github.com/IndigoCarmine/fit_it"><img src="https://raw.githubusercontent.com/IndigoCarmine/fit_it/master/docs/manual/images/17_overlay.png" width="820" alt="fit_it: global fit of cooling curves at four concentrations"></a><br>
<sub>fit_it：4 濃度の冷却曲線を温度依存 cooperative モデルでグローバルフィット / Global fit of cooling curves at four concentrations with a temperature-dependent cooperative model</sub>
</p>


## 2. 集合体を見る / Imaging assemblies

<table>
<tr>
<td width="100" align="center"><a href="https://github.com/IndigoCarmine/afm_files"><img src="https://raw.githubusercontent.com/IndigoCarmine/afm_files/master/assets/AppIcon.iconset/icon_256x256.png" width="80" alt="Kintuba AFM Viewer icon"></a></td>
<td>

**[Kintuba AFM Viewer](https://github.com/IndigoCarmine/afm_files)** — Bruker Nanoscope の AFM ファイル（.spm）を一覧・表示・解析するアプリ。集合体の形態観察に使っています。高さマップ、多項式ラインフラットニング、カラーマップ調整に対応。<br>
Browses, displays and analyses Bruker Nanoscope AFM files (.spm), which I use to look at assembly morphology: height maps, polynomial line flattening and colour-map control.

</td>
</tr>
</table>


## 3. 集合体をシミュレーションする / Simulating assemblies (GROMACS)

<table>
<tr>
<td width="100" align="center"><a href="https://github.com/IndigoCarmine/manul_cat_rs"><img src="https://raw.githubusercontent.com/IndigoCarmine/manul_cat_rs/master/resources/icon.png" width="80" alt="manul_cat_rs icon"></a></td>
<td>

**[manul_cat_rs](https://github.com/IndigoCarmine/manul_cat_rs)** — GROMACS の構造・トポロジー・インデックス・トラジェクトリを見て確かめるビューア。もとは `.top` に書いた分子間相互作用の設定ミスを見つけるために作り、今は粗視化系や表面も扱えます。<br>
A viewer for checking GROMACS structures, topologies, index files and trajectories. It started as a way to catch mistakes in intermolecular interactions defined in `.top` files and now also handles coarse-grained systems and surfaces.

</td>
</tr>
<tr>
<td width="100" align="center"><a href="https://github.com/IndigoCarmine/kuromame-rs"><img src="https://raw.githubusercontent.com/IndigoCarmine/kuromame-rs/master/resources/icon-512.png" width="80" alt="Kuromame icon"></a></td>
<td>

**[Kuromame](https://github.com/IndigoCarmine/kuromame-rs)** — PDB / GRO / TOP / MOL2 を 3D で眺め、原子を選んで残基名を書き換えるアプリ。`.top` と `.gro` の残基名を同期できます。分子や部位ごとに残基名を分けておけば、Blender の [Molecular Nodes](https://github.com/BradyAJohnston/MolecularNodes) で残基名ごとに色分けして描画できます。<br>
Views PDB / GRO / TOP / MOL2 files in 3D and lets you select atoms and rename residues, keeping `.top` and `.gro` in sync. Giving each molecule or part its own residue name lets you colour them separately in Blender with [Molecular Nodes](https://github.com/BradyAJohnston/MolecularNodes).

</td>
</tr>
<tr>
<td width="100" align="center"></td>
<td>

**[gmx_harness](https://github.com/IndigoCarmine/gmx_harness)** — EM → NVT → NPT → 本計算、Martini（粗視化）、AWH、BAR などの計算一式をファイルとスクリプトとして生成するライブラリ。`plan → preview → write` の流れで書き込み前に衝突を確認するので、AI エージェントにも安全に使わせられます。<br>
Generates complete simulation pipelines (including Martini coarse-graining, AWH and BAR) as files and scripts, with a `plan → preview → write` flow that checks for conflicts so AI agents can use it safely.

</td>
</tr>
<tr>
<td width="100" align="center"></td>
<td>

**[gplot](https://github.com/IndigoCarmine/gplot)** — GROMACS の `.xvg` と PLUMED の `COLVAR` をすぐ見るための xmgrace 風プロッタ。Wayland 環境で xmgrace が安定して動かなかったので作りました。<br>
A quick xmgrace-style plotter for GROMACS `.xvg` and PLUMED `COLVAR` files, written because xmgrace was unstable on Wayland.

</td>

</table>


## 4. 分子を設計する / Designing molecules

<table>
<tr>
<td width="100" align="center"><a href="https://github.com/IndigoCarmine/open_draw_chemistry"><img src="https://raw.githubusercontent.com/IndigoCarmine/open_draw_chemistry/master/resources/icon.png" width="80" alt="Open DrawChemistry icon"></a></td>
<td>

**[Open DrawChemistry](https://github.com/IndigoCarmine/open_draw_chemistry)** — 無料・オープンソースの構造式エディタ。ChemDraw ファイルを開け、3D 構築までできます。さらに、描いたモノマーから**環・積層・らせん・結晶格子の集合体**を組み立て、原子の衝突チェックや多次元エネルギースキャン、ソフトコア最適化で集合体構造を検討できます。<br>
A free, open-source structure editor. It opens ChemDraw files and gives the formula, exact mass, m/z, elemental analysis and IUPAC name, and builds structures in 3D. It also **assembles monomers into rings, stacks, helices and crystal lattices**, and lets you examine the assembly with clash checks, multi-dimensional energy scans and soft-core optimization.

[![Website](https://img.shields.io/badge/website-open__draw__chemistry-7c5cff?logo=googlechrome&logoColor=white)](https://indigocarmine.github.io/open_draw_chemistry-site/en/)
[![Release](https://img.shields.io/github/v/release/IndigoCarmine/open_draw_chemistry?color=7c5cff)](https://github.com/IndigoCarmine/open_draw_chemistry/releases/latest)

</td>
</tr>

</table>


<p align="center">
<img src="https://raw.githubusercontent.com/IndigoCarmine/open_draw_chemistry/master/docs/images/analysis-panel-ja.png" height="280" alt="Open DrawChemistry analysis panel">
&nbsp;&nbsp;&nbsp;
<img src="https://raw.githubusercontent.com/IndigoCarmine/cdx_file_rs/master/sample_img/png/Reaction.png" height="180" alt="A ChemDraw reaction scheme rendered by cdx_file_rs"><br>
<sub>左：Open DrawChemistry の解析パネル　右：cdx_file_rs で描画した ChemDraw ファイル<br>Left: Open DrawChemistry analysis panel. Right: a ChemDraw file rendered by cdx_file_rs</sub>
</p>


# AIとCodingに対する宣誓

ここに置いてあるコードの一部はClaude Codeに書かせています。Commitを確認いただければ明らかでしょう。私もプログラマーではなくなってしまったのだと思います。Agentic Codingの速度で人力のレビューするのは不可能で、それをする必要もないと思います。そこで、開発をAIに合わせるために意図的にレビューしていません。バグが有っても困らないものと、問題があれば使用感で気づけるものはコードを読んでいません。

GUIのレイアウト、CLIの出力整形、図の見た目、Blenderのスクリプト、ビルド周りは全部AIに任せていて、動いたらそれで終わりにしています。おかしければ実行した時点で気づくので。一方で、MDの計算設定の生成や解析、熱力学モデルのフィッティング、データの前処理は、生成させたあとで式のレベルまで自分で読んでいます。AIのPRはできるだけ厳しく審査していきます。中間的な問題には、テストを活用して確認しています。

以上は自分のリポジトリでの話です。**ほかのOSSに関わる場合は、内容によらず確実に自分で確認していきます。**


# My policy on AI and code

Some of the code here was written by Claude Code, as the commit history makes clear. As agentic coding has advanced, reviewing everything by hand has become impossible, so I deliberately skip review in places in order to keep development fast. There is only one criterion for what gets reviewed: whether a bug would fail visibly.

GUI layout, CLI output formatting, how figures look, Blender scripts, and build tooling are left entirely to the AI, and once it runs I consider it done. Anything wrong shows up the moment I run it. Generating and analyzing MD simulation settings, fitting thermodynamic models, and preprocessing data are a different matter. I read those myself, down to the equations, after they are generated, and I review the AI's pull requests as strictly as I can. Reading everything doesn't scale as the code grows, though, so I put more weight on keeping the work in a form I can verify by independent calculation. For the cases in between, I check that the tests assert what I actually expect.

All of the above applies to my own repositories. **When I contribute to someone else's open source project, I check the code myself without exception.**


# Stats

![](http://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=IndigoCarmine&theme=github)

![](http://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=IndigoCarmine&theme=github) ![](http://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=IndigoCarmine&theme=github)
![](http://github-profile-summary-cards.vercel.app/api/cards/stats?username=IndigoCarmine&theme=github) ![](http://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=IndigoCarmine&theme=github&utcOffset=8)
