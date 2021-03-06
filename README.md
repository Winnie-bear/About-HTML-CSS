### 自适应布局
- 三栏布局
  - 左右宽度固定，中间自适应
  - 上下高度固定，中间自适应
- 两栏布局
  - 左宽度固定，右自适应
  - 右宽度固定，左自适应
  - 上高度固定，下自适应
  - 下高度固定，上自适应
  
 ### 七种方案的优缺点
  - 浮动布局 
    - 局限性：浮动元素是脱离文档流，需要清除浮动，这个处理不好的话，会带来很多问题，比如高度塌陷等
    - 优点：比较简单，兼容性也较好
  - 绝对定位布局
    - 局限性：绝对定位是脱离文档流的，意味着下面的所有子元素也会脱离文档流，这就导致了这种方法的有效性和可使用性是比较差的
    - 优点：快捷方便，而且也不容易出问题
  - flex 布局
    - 局限性：不能兼容IE8及以下浏览器
    - 优点：CSS3新出的布局方式，是为了解决上述两种布局方式的不足而出现的，是比较完美的。而且移动端的布局也常用flexbox
  - 表格布局
    - 局限性：当其中一个单元格高度超出的时候，两侧的单元格也是会跟着一起变高，而这种效果有时候不是我们想要的
    - 优点：兼容性很好，在flex布局不兼容时，可以尝试表格布局
  - grid 布局
    - 局限性：只支持高版本的浏览器；grid某些属性不易懂
    - 优点：真正的 css 框架，和 flex 相比，它是二维的，而 flex 是一维的；做大布局使用，grid-gap 属性非常好用
  - 圣杯布局 VS 双飞翼布局
    - 布局要求(相同点)：
      - 三列布局，中间宽度自适应，两边定宽
      - 中间栏要在浏览器中优先展示渲染
      - 允许任意列的高度最高
    - 不同点：
      - 圣杯布局：借助的是非主要元素(left、right)覆盖了其父元素(container)的padding值所占据的宽度。也就是，同一个杯子，非主要元素只是占据了全部容器的padding值部分
      - 双飞翼布局：给中间部分(center)添加一个外层元素(container)，非主要元素(left、right)所占据的空间是主要部分(center)的margin空间。也就是，像鸟的两个翅膀，与主要部分脱离
    - 优缺点：
      - 缺点：最好设置页面最小宽度，要不然当页面缩放到一定程度时，页面布局会被破坏，影响浏览
      - 优点：允许任意列的高度最高，比表格布局灵活性高
- 当中间部分内容超出已知高度时，哪些方案可以正常显示
  - grid布局、flex布局、table布局、绝对定位布局、圣杯布局、双飞翼布局
  - 前三者是三个部分的高度一起增加，flex布局和grid布局可以分别通过设置align-items为flex-start、start解决；后三者是只有中间部分高度变高，两侧高度不受影响
