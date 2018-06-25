## フォトコラージュ

このカードでは、CSSを使ってHTML要素を正確に配置し、写真のコラージュを作成する方法を学びます。

![](images/photoCollageWithText_wide.png)

+ あなたのページに `div` を追加し、好きなだけ多くの画像を入れてください。 `div` と `img` 要素 `id` 値を与えます。

```html
    <div id="photoBox" class="relPos">
        <img id="imgHorse" class="absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <img id="imgTeaCat" class="absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
    </div>
```

写真は、コードに表示されている順序でWebページ上に順に表示されます。

+ CSSファイルで、 `div`内の要素に次のCSSクラスを追加します。 

```css
    .absPos {位置：絶対; }
```

+ 次に、プロパティ `位置を追加する必要があります。` をコンテナ自体に追加し、そのサイズを定義します。 これにより、他の要素の位置が、容器に対して</strong> に対して（すなわち、容器内で） **ようにする。</li> </ul> 
    
    ```css
        .relPos {位置：相対; } #photoBox {width：800px;高さ：400px; }
    ```
    
    + 次に、 **idセレクタ** を使って各要素のスタイルルールのセットを作成し、サイズ（`幅` および/または `高さ` プロパティ）とその正確な位置を設定します。
    
    要素の位置を定義するには、使用できる4つの特性がある： `左`、 `右`、 `トップ`、及び `底`。 それらは、エッジのそれぞれが親のエッジからどれくらい離れているかを表します。 いずれかの使用 `トップ` 又は `ボトム` 垂直位置のために、いずれか `左` 又は `右` 水平位置のため。
    
    ![上、左、下、右のプロパティが親コンテナにどのように関連しているかを示すダイアグラム](images/cssPositionProperties.png)
    
    + あなたの写真の各々の正確な位置を選択し、プロパティのいずれかを使用 `左に`、 `右`、 `トップ`、及び `底部` あなたのCSSルールでそれらの位置を定義します。 たとえば、このコードでは、catピクチャを上から100ピクセル、左から60ピクセル配置します。
    
    ```css
        #imgTeaCat {width：250px;上：100ピクセル。左：60ピクセル。 }
    ```
    
    注：位置の値は負の値にすることもできます。 負の値を使用すると、指定したエッジのいずれかで、コンテナの外に要素が移動します。
    
    ### 物事を重ねる
    
    画像の一部が重なっていることがあります。 しかし、あなたはどのように上に行くのを選ぶのですか？
    
    + 2つの画像を選択し、それらの画像が重なる位置を与えます。
    
    + 余分なプロパティを追加する、 `z-index：10;` をそれらの1つに追加し、 `z-インデックス：7を追加します。` を他方に接続する。
    
    + あなたのウェブページ上の結果を見てください。
    
    ![](images/horse10Cat7.png)
    
    + 今度は `z-index` 値を入れ替えて、 `7` と `10` が逆の方向になるようにします。 あなたのウェブページに違いはありますか？
    
    ![](images/horse7Cat10.png)
    
    ## \---崩壊\---
    
    ## title：z-indexはどのように機能しますか？
    
    `z-index` プロパティを使用すると、2つ以上の要素がどのように重なるかを決めることができます。 値には任意の整数を指定できます。
    
    **数字が** の要素は、パイルの **上** に、言い換えれば **正面**終わります。 次に高い数字の要素は、それより後ろにあり、他の要素の前にあります。他のすべての要素の背後にある最も低い番号の要素に到達するまで続きます。
    
    \--- /崩壊\---
    
    イメージだけでなく、この方法でHTML要素を配置することができます。 たとえば、 `p` 要素を使用して写真にテキストを追加することができます。
    
    \---挑戦\---
    
    ## 課題：写真コラージュを作る
    
    + 下に示すような独自のコラージュを作成してみてください！ 異なる `z-インデックス` 値と一緒に正確な位置合わせを使用して、オーバーラップ効果を望むように得ることができます。
    
    - - ヒント - -
    
    \---ヒント\---
    
    以下は、私のアイルランドのウェブサイトの写真コラージュのHTMLコードです。 `div`中に6枚の写真と1つのテキストがあります。
    
    ```html
        <div id="photoBox" class="relPos">
            <img id="imgStreet" class="collagePhoto absPos" src="ireland-1474045_640.jpg" alt="Irish town" />
            <img id="imgTeaCat" class="collagePhoto absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
            <img id="imgCoast" class="collagePhoto absPos" src="cattle-2369463_640.jpg" alt="Cows at the coast" />
            <img id="imgTrees" class="collagePhoto absPos" src="ireland-2614852_640.jpg" alt="Tree tunnel" />
            <img id="imgSheep" class="collagePhoto absPos" src="sheep-456989_640.jpg" alt="Sheep on the road" />
            <img id="imgHorse" class="collagePhoto absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
            <p id="photoText" class="absPos">アイルランド</p>
        </div>
    ```
    
    \--- /ヒント\---
    
    \---ヒント\---
    
    コラージュ内の各写真の位置を設定するCSSルールは次のとおりです。
    
    ```css
        #imgHorse {width：120px; top：200px;左：390ピクセル。 z-インデックス：10; } #imgSheep {width：200px;}上：100ピクセル。左：20ピクセル。 z-インデックス：8; } #imgCoast {width：150px; top：250px;左：10ピクセル。 z-インデックス：5; } #imgTrees {width：110px;} top：65px;左：205ピクセル。 Z-インデックス：9; } #imgTeaCat {width：250px;}上：210ピクセル;左：160ピクセル。 z-インデックス：7; } #imgStreet {width：180px; top：90px;左：310px; z-インデックス：6; } #photoText {font-family： "ブラシスクリプトMT";色：ライトグリーン; font-size：4em;左：35ピクセル。上：15ピクセル。 z-インデックス：20; }
    ```
    
    \--- /ヒント\---
    
    \---ヒント\---
    
    私が使ったCSSクラスは次のとおりです：
    
    ```css
        。collagePhoto {border：1px solid white; } .relPos {位置：相対; } .absPos {位置：絶対; }
    ```
    
    \--- /ヒント\---
    
    - - /ヒント - -
    
    ![テキストの上に写真のコラージュ](images/photoCollageExample.png)
    
    \--- /チャレンジ\---