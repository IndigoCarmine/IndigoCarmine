

# AIとCodingに対する宣誓

ここに置いてあるコードの一部はClaude Codeに書かせています。Commitを確認いただければ明らかでしょう。私もプログラマーではなくなってしまったのだと思います。Agentic Codingの速度で人力のレビューするのは不可能だと思い、それをする必要もないと思います。そこで、開発をAIに合わせるために意図的にレビューしていません。バグが有っても困らないものと、問題があれば使用感で気づけるものはコードを読んでいません。

GUIのレイアウト、CLIの出力整形、図の見た目、Blenderのスクリプト、ビルド周りは全部AIに任せていて、動いたらそれで終わりにしています。おかしければ実行した時点で気づくので。一方で、MDの計算設定の生成や解析、熱力学モデルのフィッティング、データの前処理は、生成させたあとで式のレベルまで自分で読んでいます。AIのPRはできるだけ厳しく審査していきます。中間的な問題には、テストを活用して確認しています。

以上は自分のリポジトリでの話です。**ほかのOSSに関わる場合は、内容によらず確実に自分で確認していきます。**


# My policy on AI and code

Some of the code here was written by Claude Code, as the commit history makes clear. As agentic coding has advanced, reviewing everything by hand has become impossible, so I deliberately skip review in places in order to keep development fast. There is only one criterion for what gets reviewed: whether a bug would fail visibly.

GUI layout, CLI output formatting, how figures look, Blender scripts, and build tooling are left entirely to the AI, and once it runs I consider it done. Anything wrong shows up the moment I run it. Generating and analyzing MD simulation settings, fitting thermodynamic models, and preprocessing data are a different matter. I read those myself, down to the equations, after they are generated, and I review the AI's pull requests as strictly as I can. Reading everything doesn't scale as the code grows, though, so I put more weight on keeping the work in a form I can verify by independent calculation. For the cases in between, I check that the tests assert what I actually expect.

All of the above applies to my own repositories. **When I contribute to someone else's open source project, I check the code myself without exception.**


![](http://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=IndigoCarmine&theme=github)

![](http://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=IndigoCarmine&theme=github) ![](http://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=IndigoCarmine&theme=github)
![](http://github-profile-summary-cards.vercel.app/api/cards/stats?username=IndigoCarmine&theme=github) ![](http://github-profile-summary-cards.vercel.app/api/cards/productive-time?username=IndigoCarmine&theme=github&utcOffset=8)
