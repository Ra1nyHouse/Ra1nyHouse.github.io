---
layout: post
tags: [other]
---

　直接在注册表中修改键位映射关系

　　注册表位置：[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layout]  如果没有此键，就新建一个

　　新建一个二进制值的Key，名叫：Scancode Map

　　输入如下的值：

　　00,00,00,00

　　00,00,00,00

　　03,00,00,00

　　3A,00,1D,00

　　1D,00,3A,00

　　00,00,00,00

　　前两行和最后一行，都是固定的，全部为0。第三行，表示你修改了几个键，其实我们只是改了两个键，不过最后那一行也要算进去，所以是3。

　　重点是在第四行和第五行。3A00，代表Caps Lock，  1D00，代表Ctrl。这一行，意思即为，将Caps Lock映射为Ctrl

　　第五行，就不用说了，意思刚好相反。

　　修改完毕后，重新登录Windows即可生效！

　　下面附上各个键位值的参考：

　　Escape 01 00

　　Tab 0F 00

　　Caps Lock 3A 00

　　Left Alt 38 00

　　Left Ctrl 1D 00

　　Left Shift 2A 00

　　Left Windows 5B E0

　　Right Alt 38 E0

　　Right Ctr l1D E0

　　Right Shift 36 00

　　Right Windows 5C E0

　　Backspace 0E 00

　　Delete 53 E0

　　Enter 1C 00

　　Space 39 00

　　Insert 52 E0

　　HOME 47 E0

　　End 4F E0

　　Num Lock 45 00

　　Page Down 51 E0

　　Page Up 49 E0

　　Scroll Lock 46 00
