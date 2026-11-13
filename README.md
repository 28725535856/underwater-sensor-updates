# 水下传感器更新

当前版本1.1.5（21）

无需拆板或烧录。按要求，界面、复制和Excel统一显示阻值：最近1～4个有效ADC取均值后按4700*m/(255-m)换算；采集信息页记录处理方法。超过750ms间隙、超量程会重置窗口，不补造时间点。新增残包1500ms未补齐时有限次重读同一缓存（最多2次），不重启采样。147项测试、签名与实际Java增量还原通过；手机待验证。该处理没有改变8位ADC硬件分辨率。

清单：https://raw.githubusercontent.com/28725535856/underwater-sensor-updates/main/updates/latest.json
