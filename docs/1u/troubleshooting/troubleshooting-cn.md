If you encounter some situations where you can't simply connect directly, here will be some suggestions.

## Cannot discover devices in Home Assistant

在多数情况下，只要配置网络后，传感器就会广播自己的地址，而Home Assistant就能自动发现设备。  

但可能一些情况会影响这个发现过程：  
- 如果路由器屏蔽了设备间的互相访问，设备是无法发现，也无法连接的。比如传感器连接在隔离的访客网络。
- 如果一个传感器在Home Assistant已经添加，但是又删除了，此时不会再次被发现。除非重启Home Assistant。这个行为在Home Assistant 2023.06版本已经存在。
