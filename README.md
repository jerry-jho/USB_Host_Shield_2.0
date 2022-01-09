# USB Host Library Rev. 2.0

The code is released under the GNU General Public License.

此代码来自 https://github.com/felis/USB_Host_Shield_2.0

为WROOM ESP32 + USB Shield Mini 国产版 + 无线XBox控制器特别修改

安装方法：

安装官方版，下载本Repo后覆盖 文档\Arduino\libraries\USB_Host_Shield_Library_2.0


# 硬件连接

[![](https://github.com/jerry-jho/USB_Host_Shield_2.0/u2-768x318.gif)]

割开USB接口与2.2K电阻之间的导线。用万用表确认断路。

然后连接如下：

（USB向上，芯片朝向你自己，从上到下编号。Gxx是ESP32模组的GPIO编号）

UHS左1（SS）-> G13
UHS左2（MOSI）-> G23
UHS左3（MISO）-> G19
UHS左4（SCK）-> G18
UHS左9（3V3）-> 3V3
UHS左11（GND）-> GND
UHS右1（INT）-> G26
UHS右1左侧（5V）-> 5V
UHS右10（RST）-> 3V3（也可以接到任意GPIO，然后在setup置位）

# getRAW 函数的使用

这个效率稍微高一些，定义如下：

addr = 0，控制器id
addr = 1，0x14
addr = 2，十字右|十字左|十字下|十字上|x|x|back|start
addr = 3，Y|X|B|A|x|x|RB|LB
addr = 4，LT模拟
addr = 5，RT模拟
addr = 7，左摇杆左右（左：-128，右：127）
addr = 9，左摇杆上下（下：-128，上：127）
addr = 11，右摇杆左右（左：-128，右：127）
addr = 13，右摇杆上下（下：-128，上：127）
