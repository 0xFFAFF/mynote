# HFSS 仿真要点
---

## 常见激励设置
1. :star:**port**：最常用的一个端口设置
   - **circuit** 适用于电路的Layout
   - **Floquet Port** 多用于相控阵的仿真，配合主从边界条件一起使用
   - **Modal Lumped Port**模式集总端口
   - **modal Wave Port**模式波端口
   - **terminal Lumped Port** 终端集总端口
   - **terminal Wave Port** 终端波端口
2. **Incident Wave**：入射波激励，多用于RCS的仿真

**PS**：设置波端口要和**空气盒子**重合，其宽度是微带线宽度的**5倍**及以上，高度是厚度**6-10**倍，集总端口不和空气盒子接触，在物体内部或边沿

---

## 常见求解类型
1. **HFSS**
2. :star:**HFSS with hybrid and arrays**(比较常用，就选用这个)
3. **Elign mode** 本征模

---

## 求解设置
在左侧树状卡中找到**Analysis**，可以添加求解设置

---

## 变量设置
变量分为**Project Variable**和**Local Variable**，其中**Project Variable**变量的设置需要在变量名前＋ **$**

