# SVGに対応していないブラウザでは代替のPNGを表示する

## Demo
https://sutara79.github.io/demo-svg-fallback/

下記の記事を参考にしてデモを作成しました。  
[SVGをIE等のブラウザ対応を考慮して使う方法まとめ（SVGのフォールバック画像など）｜2.IDEA](http://2ndidea.com/svg/svg-fallbacks/)

## html5shivとの併用を推奨
公式ページで必要な判定機能だけを選んで、最小の要領に抑えたファイルをダウンロードできます。  
その際、IE8でもHTML5タグを認識させる「html5shiv」をファイルに含めることができるので、是非そうすることをお勧めします。  
下記のURLを開くと、すでにSVGの判定とhtml5shivだけを選択した状態になっているので、すぐにビルドできます。  
ただし、「Add CSS classes」のチェックは外したほうがいいです。  
https://modernizr.com/download?svg-shiv

## CDNからModernizrを使う場合の注意
Modernizrは下記のCDNから利用できます。  
https://cdnjs.com/libraries/modernizr

ただし、Modernizrは下記のCSSクラスを追加します。  
下記と同名のクラス名を既に使っていてスタイル指定を記述していると、思わぬレイアウト崩れが生じるので注意してください。

- js
- flexbox
- flexboxlegacy
- canvas
- canvastext
- webgl
- no-touch
- geolocation
- postmessage
- websqldatabase
- indexeddb
- hashchange
- history
- draganddrop
- websockets
- rgba
- hsla
- multiplebgs
- backgroundsize
- borderimage
- borderradius
- boxshadow
- textshadow
- opacity
- cssanimations
- csscolumns
- cssgradients
- cssreflections
- csstransforms
- csstransforms3d
- csstransitions
- fontface
- generatedcontent
- video
- audio
- localstorage
- sessionstorage
- webworkers
- applicationcache
- svg
- inlinesvg
- smil
- svgclippaths

(公式: https://modernizr.com/docs/#using-modernizr-with-css )