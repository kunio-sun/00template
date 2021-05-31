# 00template
マークアップ用テンプレート
+ margin,paddingは競合させすぎないように個別で記入
+ mediaQuery使用時には必ず@mixin mqDown()を使用

## BEM記法 block element modifierに準じたclassの命名
+ block(塊要素) 「 キャメルケース 」
+ element(inner要素) 「 _ 」
+ modifier(修飾子) 「 - 」
で区切ることにする

### 格納ファイル
|  変数定義、関数定義  |  共通部品の定義は  |  外部デベロッパーが作成したimportファイル  |
| ---- | ---- | ---- |
|  ./_init.scssに格納  |  ./modules内に格納  |  ./vendor内に格納  |


### module(共通部品)にbackgroundImageURLを指定する時
相対パスがややこしくなっているためinit.scssで定義した変数を使い
$imagePathFromStyleRoot + 画像名にする

### @keyframeを共通部品(module)に使用する場合
必ず部品名 == animation-nameで統一

共通部品以外に適応させたい場合は適宜共通部品名以外で設定
