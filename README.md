
## OpenCore BigSur-Beta AMD EFI  
基于OpenCore 0.61和macOS BigSur Beta4制作  

<img src="https://github.com/wnnce/OpenCore-AMD-BigSur-Beta/blob/master/img/1.png?raw=true" width="70%" height="70%" align="middle">  

**我的系统配置**  
CPU  AMD Ryzen 5 2600X  
主板  ASUS ROX X470i  
显卡  蓝宝石Rx470公版  
内存  cuso DDR4 2666 16G*2 (OC到3600)  
硬盘  三星970EVO+海力士PC601+紫光S100  
网卡  板载英特尔i211+AX200
### 使用的Kext
+ Lilu.kext
- VirtualSMC.kext
+ AppleALC.kext
- itlwmx.kext
+ NVMeFix.kext
- RadeonBoost.kext
+ SmallTreeIntel82576.kext
- USBPorts.kext
- SMCAMDProcessor.kext
+ WhateverGreen.kext  
  
<img src="https://github.com/wnnce/OpenCore-AMD-BigSur-Beta/blob/master/img/4.png?raw=true" width="70%" height="70%" align="middle">  

SSDT-EC-USBX.aml(修复EC控制器和USB供电  (必需))  
SSDT-RHUB.aml(修复USB控制器 (可选 未加载))  
SSDT-SBUS-MCHC.aml(修复SMBus(可选))  
SSDT-UIAC.aml(修复USB端口映射 在我的电脑上不工作 最终使用USBPorts.kext修复(可选 未加载))  
<img src="https://github.com/wnnce/OpenCore-AMD-BigSur-Beta/blob/master/img/3.png?raw=true" width="70%" height="70%" align="middle"> 

### 存在的问题
1. 无法睡眠，睡眠会睡死无法唤醒（可能是电源管理引起的）
2. Wifi可以通过[itlwmx.kext](https://github.com/OpenIntelWireless/itlwm)工作，但是速度比较慢。 
3. 没有电源管理([AMDRyzenCPUPowerManagement.kext](https://github.com/trulyspinach/SMCAMDProcessor)在BigSur Beta4上不工作)  

<img src="https://github.com/wnnce/OpenCore-AMD-BigSur-Beta/blob/master/img/2.png?raw=true" width="70%" height="70%" align="middle">   
  
<img src="https://github.com/wnnce/OpenCore-AMD-BigSur-Beta/blob/master/img/5.png?raw=true" width="70%" height="70%" align="middle"> 