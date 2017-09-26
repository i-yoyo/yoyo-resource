## yoyo-resource

### plist规则

- yoyo-resource.plist中version表示的是tag，即：根据当前yoyo-resource.plist来获取资源，需要获取指定tag路径下的资源。同时也表示，一旦该git仓库的资源有更新，也要同时为该仓库增加tag，并且修改yoyo-resource.plist中的version值为最新的tag。

- 本仓库中的所有plist中的Dictionary（Root节点除外）和Array类型，都表示一层文件路径（一层文件夹），路径的起点为仓库的根目录，即仓库最外层yoyo-resource.plist所在位置。所有需要用到的资源，都必须填写在plist中，plist中也可以包含另一个plist。如此一来，形成以yoyo-resource.plist文件为起点的一条资源链。

- 规定所有tag标志必须为由两个英文小点分割的三段数字组合，如：1.0.0

- 所有plist中的Dictionary：key表示资源备注名，value表示资源的真实文件名。

- yoyo-resource.plist文件作为整个资源连的起始点，必须始终在master分支下，并且，yoyo-resource.plist的更新也需要在master分支下。

- 按照以上规则，请求方只需要请求并解析yoyo-resource.plist文件，并能得到一条完整的资源链。同时，还能支持版本更新行为。

### 其他

- yoyo-resource.plist固定链接：[https://raw.githubusercontent.com/i-yoyo/yoyo-resource/master/yoyo-resource.plist](https://raw.githubusercontent.com/i-yoyo/yoyo-resource/master/yoyo-resource.plist)

- 示例资源：Radar(Default).mp3 tag:1.0.0 链接：[https://raw.githubusercontent.com/i-yoyo/yoyo-resource/1.0.0/Ringtone/RINGTONES/Radar(Default).mp3](https://raw.githubusercontent.com/i-yoyo/yoyo-resource/1.0.0/Ringtone/RINGTONES/Radar(Default).mp3)
