## 照片拼贴

在这张卡上，您将学习如何使用CSS精确定位HTML元素并制作照片拼贴。

![](images/photoCollageWithText_wide.png)

+ 添加` div `到页面上，并在其中放置尽可能多的图像。 给出`div`和`img`元素`id`值。

```html
    <div id="photoBox" class="relPos">
        <img id="imgHorse" class="absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <img id="imgTeaCat" class="absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
    </div>
```

照片将按照在代码中的显示顺序依次显示在网页上。

+ 在您的CSS文件中，为` div中的元素添加以下CSS类` ： 

```css
    .absPos {
        position: absolute;
    }
```

+ 接下来，您需要添加属性` position：relative; `容器本身并为其定义尺寸。 这样就可以相对于**定义其他元素的位置** （即在容器内）。

```css
    .relPos {
        position: relative;
    }

    #photoBox {
        width: 800px;
        height: 400px;
    }
```

+ 然后使用**id 选择器**为每个元素创建一套样式规则来设置他们的大小(`宽`和/或`身高`属性) 以及他们的确切位置。

要定义元素的位置，可以使用四个属性：`left` ，`right` ，`top`和`bottom` 。 它们表示每个边缘应距父对象的边缘多远。 使用` top `或` bottom `表示垂直位置，`left `或`right`为水平位置。

![该图显示了top，left，bottom和right属性与父容器的关系](images/cssPositionProperties.png)

+ 选择您每张图片的确切位置，并使用任意属性`left`， `right`, `top`, 和`bottom`, 以在您的 CSS 规则中定义那些职位。 例如，此代码将猫的图片从顶部放置100个像素，从左侧放置60个像素：

```css
    #imgTeaCat {
        width: 250px;
        top: 100px;
        left: 60px;
    }
```

注意：位置值也可以为负！ 如果使用负值，它将把元素推到容器外部，超出指定的边缘。

### 使事物重叠

您可能需要重叠一些图片。 但你如何选择哪个在上面？

+ 选择两个图像，并赋予它们使其重叠的位置。

+ 添加额外的属性，`z-index: 10; ` 到其中一个, 然后添加`z-index: 7; ` 到另一个。

+ 查看您网页上的结果。

![](images/horse10Cat7.png)

+ 现在交换` z-index `值，这样` 7 `和` 10 `反过来。 您在网页上看到任何不同吗？

![](images/horse7Cat10.png)

## \--- collapse \---

## 标题：z-index如何工作？

`z-index`属性让您决定两个或多个元素应如何重叠。 该值可以是任何整数。

**最高**编号的元素最终是**最高**的位置，或用其他语言说是在**前面**。 编号次高的元素位于其后，位于其他元素的前面，依此类推，直到到达编号最小的元素，该元素出现在所有其他元素的后面。

\--- /collapse \---

您可以通过这种方式放置任何HTML元素，而不仅仅是图像。 例如，您可以使用` p `元素在照片上添加一些文字。

\--- challenge \---

## 挑战：制作照片拼贴

+ 尝试创建自己的照片拼贴，如下图所示！ 使用精确位置和不同的`z-index`值来获得你想要的重叠效果。

\--- hints \---

\--- hint \---

下面是我的爱尔兰网站上照片整理的 HTML 代码。 在`div`内有六张照片和一张文本。

```html
    <div id="photoBox" class="relPos">
        <1 />
        <2 />
        <3 />
        <4 />
        <5 />
        <6 />
        <p id="photoText" class="absPos">爱尔兰</p>
    </div>
```

\--- /hint \---

\--- hint \---

以下是CSS规则，可为拼贴中的每张图片设置位置：

```css
    #imgHorse {
        width: 120px;
        top: 200px;
        left: 390px;
        z-index: 10;
    }
    #imgSheep {
        width: 200px;
        top: 100px;
        left: 20px;
        z-index: 8;
    }
    #imgCoast {
        width: 150px;
        top: 250px;
        left: 10px;
        z-index: 5;
    }
    #imgTrees {
        width: 110px;
        top: 65px;
        left: 205px;
        z-index: 9;
    }
    #imgTeaCat {
        width: 250px;
        top: 210px;
        left: 160px;
        z-index: 7;
    }
    #imgStreet {
        width: 180px;
        top: 90px;
        left: 310px;
        z-index: 6;
    }
    #photoText {
        font-family: "brush script MT";
        color: lightgreen;
        font-size: 4em;
        left: 35px;
        top: 15px;
        z-index: 20;
    }
```

\--- /hint \---

\--- hint \---

这里是我使用的 CSS 类：

```css
    .collagePhoto {
        border: 1px solid white;
    }
    .relPos {
        position: relative;
    }
    .absPos {
        position: absolute;
    }
```

\--- /hint \---

\--- /hints \---

![顶部带有文字的照片拼贴](images/photoCollageExample.png)

\--- /challenge \---