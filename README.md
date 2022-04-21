# GBO-Aku - monitoring of the load control

Only in Czech ...


GBO-Aku popis viz. http://www.yorix.cz/cz/greenbono/gbo-aku.htm

Zařízení disponuje rozhraním RS485 s protokolem MODBUS RTU. Na stránkách výrobce je uvedeno připojení k počítaači přes sériovou linku, tak i přes ethernet. Zařízení se konfiguruje za pomocí aplikace GreenBonO_HMI.exe. Aplikace GreenBonO_HMI neumí pracovat s protokolem Modbus TCP, ale pouze se sériovou linkou přes TCP. Lokálně pak komunikuje RS485 s protokolem MODBUS RTU. 

Pro monitoring je výhodnější používat Modbus TCP, ale zároveň se hodí pro občasnou konfigurací mít k dispozici sériovou linku přes TCP. Jako vhodný se jeví např. převodník Waveshare k instalci na DIN lištu s oběma režimy provozu. 

Link na wiki převodníku:  https://www.waveshare.com/wiki/RS485_TO_ETH_(B)


# Flow
![flow](/img/flow.png)

# Dashboard
![dashboard](/img/board.png)


# NodeRed modules
node-red-contrib-ui-led
node-red-contrib-modbus

# Waveshare - Modbus TCP (NodeRed and other)
In the configuration, change the Device IP, port and gateway. In this example, the address 192.168.2.12 is given.

![flow](/img/wavesahre-modbus.png)

# Waveshare - serial over TPC (GreenBonO_HMI)

![flow](/img/waveshare-serial.png)
![flow](/img/hmi.png)



