# USB Host Library Rev. 2.0

The code is released under the GNU General Public License.

此代码来自 https://github.com/felis/USB_Host_Shield_2.0

硬件连接

  1. SS -> IO13
  2. SINT -> IO35
  3. SCLK -> IO18
  4. MISO -> IO19
  5. MOSI -> IO23
  6. SRST -> IO5
  7. SINT -> IO35


## XBOX360 getRAW 函数的使用

这个效率稍微高一些，定义如下：

1. addr = 0，控制器id
2. addr = 1，0x14
3. addr = 2，十字右|十字左|十字下|十字上|x|x|back|start
4. addr = 3，Y|X|B|A|x|x|RB|LB
5. addr = 4，LT模拟
6. addr = 5，RT模拟
7. addr = 7，左摇杆左右（左：-128，右：127）
8. addr = 9，左摇杆上下（下：-128，上：127）
9. addr = 11，右摇杆左右（左：-128，右：127）
10. addr = 13，右摇杆上下（下：-128，上：127）
