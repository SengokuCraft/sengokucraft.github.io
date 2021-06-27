# 戦国クラフトのホームページの中身

これは戦国クラフトのホームページの中身です。  

[https://sengokucraft.github.io/](https://sengokucraft.github.io/)  
にて公開しています。  
ぜひご覧ください。  

また、開発中([developブランチ](https://github.com/SengokuCraft/sengokucraft.github.io/tree/develop))の物は  
[https://sengokucraft.github.io/develop/](https://sengokucraft.github.io/develop/)  
にて公開しています。  
レビューしていただけると幸いです。  

## License

あなたがこのリポジトリ内の著作物を使用、利用、複製および配布をする場合、  
[ライセンス](/LICENSE.md)を全て読みこれに同意する必要があります。  

ライセンスの内容を簡単に説明すると、  

Apacheライセンス2.0みたいな扱いでいいけど、  
そのまま全部流用してサイトを公開したりしちゃだめだよ。  
サイトのcssをコピーしてちょっといじっておんなじデザインを使うみたいな、  
コードとかを一部をコピーして(いじって)使うとかなら全然いいよ。  
だけどちゃんと  
```
このデザインは戦国クラフト(https://sengokucraft.github.io/)のcssを改変して使用しています。
```
みたいな文章をサイトとかソースコードとかに書かないとだめだよ。  
ライセンスはこれと同じかこれよりも厳しい物になら変えて公開してもいいよ。  
ちゃんとそのライセンスも明記してね。  

という内容です。  
ですがあなたがこのリポジトリ内の著作物を使用、利用、複製および配布をする場合は必ず[本文](/LICENSE.md)をきちんと読み同意する必要があるのでご注意ください。  

## Gitの管理方針

### Git Flow

基本的にはGitFlowに従う。  
`main`から`develop`ブランチを切り、  
そこを起点に様々な`feature/*`ブランチを切りそれぞれ完成したら検証し`develop`にマージ。  
バグの修正の場合は`bugfix/*`ブランチとする。  
公開中のホームページにデプロイしたい際は`develop`から`release/*.*`を切ってそこでデバッグを行いバグを直し大丈夫そうなら`main`と`develop`にマージし`main`ブランチのマージコミットにバージョンのタグを付与。  
公開中のホームページにバグが見つかった場合は`main`から`hotfix/*`を切りバグを直し大丈夫そうなら`main`と`develop`にマージし`main`ブランチのマージコミットにバージョンのタグを付与。  
また`feature/*`ブランチなどはなるべくissueを建ててからissue番号を載せたブランチ名にして切りたい。  

### GitHub Pages

ホームページは(現時点では) GitHub Pages を利用し公開する。  
[gh-pagesブランチ](https://github.com/SengokuCraft/sengokucraft.github.io/tree/gh-pages) を公開。  
[mainブランチ](https://github.com/SengokuCraft/sengokucraft.github.io/tree/main) に更新があれば GitHub Actions を使用し自動で`/docs`ディレクトリをデプロイ。  
[developブランチ](https://github.com/SengokuCraft/sengokucraft.github.io/tree/develop) に更新があれば自動で`/docs`ディレクトリを`/develop`以下にデプロイ。  
