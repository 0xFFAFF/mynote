## PCB各层

1. Top-Layer 顶层
2. Bottom-Layer 底层
3. Keepout-Layer 禁止布线层

    画个框，框中可以放置器件或者走线

4. Top-Overlay 顶层丝印层

    可以写字的层，常用来标注器件位置，编号等

5. Bottom-Overlay 底层丝印层
6. Top-Paste 顶层助焊层

    是机器贴片时要用的，是对应所有贴片元件的焊盘的，大小与 top layer/bottom layer层一样，是用来开钢网漏锡用的。

7. Bottom-Paste 底层助焊层
8. Top-Solder 顶层阻焊层

    阻止绿油覆盖

9. Bottom-Solder 底层阻焊层
10. Drill-Guide 过孔引导层

    过孔及焊盘的坐标

11. Drill Drawing 过孔钻孔层

    焊盘及过孔的尺寸描述层

12. Multilayer  多层

    抽象层，用来与各层之间建立电器关系，通常***过孔和焊盘***设置在这一层
