**論文タイトル**: Denoising Diffusion Probabilistic Models

**著者**: Jonathan Ho, Ajay Jain, Pieter Abbeel

**発表年**: 2020

**ジャーナル**: NeurIPS 2020

## 要約
本論文は、拡散確率モデル (diffusion probabilistic models) を使用した高品質な画像合成の手法を紹介しています。このモデルは、非平衡熱力学に基づく確率的な潜在変数モデルであり、特にLangevin力学を用いたノイズ除去スコアマッチングと結び付けて、新しい重み付け変分境界の下でトレーニングされます。CIFAR-10データセットにおいて、最先端のFIDスコアとInceptionスコアを達成し、ProgressiveGANに匹敵するサンプル品質を示しています。

## キーポイント
- **高品質な画像生成**: 拡散確率モデルは、逐次的にデータにノイズを加えた後、そのノイズを逆過程で除去することで、高品質な画像サンプリングを実現しています。
- **Langevin力学とノイズ除去スコアマッチングの融合**: 拡散モデルの逆過程はLangevin力学を用いたノイズ除去スコアマッチングと等価であり、これにより複数のノイズレベルでのデータ復元が可能になります。
- **簡便かつ効果的なパラメータ化**: 拡散過程のガウス遷移を活用し、モデルのパラメータ化が単純化され、効率的なトレーニングが可能です。
- **CIFAR-10およびLSUNデータセットでの成果**: CIFAR-10においてInceptionスコア9.46、FIDスコア3.17という最先端の結果を達成し、LSUN 256x256データセットでもProgressiveGANに匹敵する画像品質を示しています。
- **変分境界によるトレーニング**: 重み付け変分境界を用いた学習が、モデルの性能を最大化し、ノイズ除去とサンプル品質を向上させる要因となっています。
- **逐次的な損失の圧縮**: 拡散モデルのサンプリング過程は進行的なロッシー圧縮（逐次的デコード）の一種とみなすことができ、一般的な自己回帰デコードの拡張となっています。
- **生成過程の効率化**: サンプル生成の過程において、Langevin力学に基づく進行的なデコードが行われることで、全体的な生成効率が向上しています。

## リンク
[論文のリンク](https://github.com/hojonathanho/diffusion)