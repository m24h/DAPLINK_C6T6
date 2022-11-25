Modified from a modified copy of JiXin DAP-Link source codes, to fit STM32F103C6T6, which has only 32kB ROM and 10kB RAM.
There's only a HID interface for debug and a CDC serial port for COM-like usage.
HSE of STM32 is a 8MHz oscillator oscillator.
The hardware GPIO pins (which can be modifed in file "DAP_config.h"):
    A9: serial TX
    A10: serial RX
    SWDIO: SWDIO
    SWCLK: SWCLK
    A6: nRESET
    B8: Connected LED
    B12: Target Running LED

Important: this is a Keil MDK5 project, but a compiler version 5 (ARMCC) is needed.

---------------------------- following is from original author -------------------------

�����̴ӡ����¡���Դ��DAPLINK�޸�����
�޸� by��rush
1�������ԭ����ȱ�ļ��޷��������⡣����ʹ��MDK474����.����ĳ���ļ�RTL.h������keil��G�㣬����Ҫע�����keilע����RTOS�Ĺ��ܣ�
2��ԭ���̾�Ȼ�뵱Ȼȥ�޸����豸���֣������������˺ܶ�汾MDK�޷�ʶ�𣡣�
3��ԭ����ע�͵���������������֪���ǲ��Ǹ����豸���������ǵ�win7����֮�⵼������win10�¸����豸��ʶ��(����ֻ�д���û��HID)
4��ԭ����USBlibʹ��lib�������ṩ��һ��Դ�룬Ϊ����ȫ��Դ���Ǹ���Դ����룬���в���inline�����޷����룬��ȥ����
5���Ǹ�USBlib�ⲻ����GD�ȹ�����Ƭ��������ʵ��Ǯ��������STM32оƬ��
6����·ͼ���ǳ������ϹŶ�STLINK2.0������ˢJLINK OB�����֡��Ҿ�����12M����8M�����޸ġ�

�޸� by��hianiong
1���޸�SWDIO �� SWCLK ����Сϵͳ�����Ĭ��SWDIO��SWCLK���
2��ˢ��daplink�����Ҫͨ��SWD�ָ��������̼��������boot0 �� VCC����ͨ����������
3������8M���񣬲��Կ���ֱ��ʹ�ò����޸�