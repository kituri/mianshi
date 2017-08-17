# Android命名规范

>**1.包（packages）**
采用反域名命名规则，全部使用小写字母。一级包名为com，二级包名为meitun，三级包名为mama，四级包名为模块名或层级名，五级为业务细化。

例：com.google.play.model.common


>**2.类（classes）**

名词，采用大驼峰命名法，尽量避免缩写，除非该缩写是众所周知的，  比如HTML,URL，如果类名称中包含单词缩写，则单词缩写的每个字母均应大写。（若有全称太长的情况，优先使用约定俗成的缩

写，其次使用每个单词的大写，这种情况请少出现。例：PstMainFragment ---> PagerSlidingTabMainFragment）

例：CarFragment、BaseFragmentActivity


>**3.接口（interface）**
命名规则与类一样采用大驼峰命名法，多以able或ible结尾，
如interface Runna ble ;
interface Accessible 。

例：Viewable、Populatable。


>**4.方法（methods）**
动词或动名词，采用小驼峰命名法例如:onCreate(),run()

例：
initXX() | 初始化相关方法,使用init为前缀标识，如初始化布局initView()
isXX()   | checkXX()方法返回值为boolean型的请使用is或check为前缀标识
getXX()  | 返回某个值的方法，使用get为前缀标识


>**5.变量（variables）**
采用小驼峰命名法。类中控件名称必须与xml布局id保持一致。
用统一的量词通过在结尾处放置一个量词，就可创建更加统一的变量，它们更容易理解，也更容易搜索。例如，请使用strCustomerFirst和strCustomerLast，而不要使用strFirstCustomer和strLastCustomer。

例：
    mAdapter     (类内变量）
    btn_login    (与xml布局id保持一致的Button类型变量，布局id命名规范请详见“9”）
         

>**6.常量（Constants）**
全部大写,采用下划线命名法.例如：MIN_WIDTH

例：TYPE_BROSWER


>**7.资源文件（图片drawable文件夹下）**
全部小写，采用下划线命名法，加前缀区分
命名模式：类型名称缩写_逻辑名称/common_逻辑名称
如果有多种形态如按钮等除外如btn_xx.xml（selector）

例：
     btn_xx          | 按钮图片使用btn_整体效果（selector）
     btn_xx_normal   | 按钮图片使用btn_正常情况效果
     btn_xx_press    | 按钮图片使用btn_点击时候效果
     bg_head         | 背景图片使用bg_功能_说明
     def_search_cell | 默认图片使用def_功能_说明
     icon_more_help  | 图标图片使用icon_功能_说明


>**8.资源布局文件（XML文件（layout布局文件））**
全部小写，采用下划线命名法。

1)．contentview命名, Activity默认布局，Fragment默认布局，不加任何后缀。
    Activity缩写为ac，Fragment缩写为fr。
    
例：ac_main.xml、fr_car.xml


2)．Dialog命名：dialog_描述.xml

例：dialog_normal.xml (Dialog命名)


2)．PopupWindow命名：ppw_描述.xml

例：pop_info.xml (Dialog命名)

3)．adapter的子布局：功能模块_item.xml

例：item_coupon.xml   (item、cell的命名)

4). contentview中的布局。做为Activity或Fragment中的子布局，在contentview的命名后，跟上逻辑名称后缀。

例：ac_main_login.xml （意为：在main这个Activity中的一个login布局）


>**9.layout中的id命名**
命名模式为：view缩写_模块名称_view的逻辑名称

特例:

Button         |    btn

除了以上这个特例，其他2个单词以上的一律取开头2个英文字幕做为大写。

例：ImageView  |    iv

