����js hcharts���� ��������sar ����־��

�ο�������http://www.hcharts.cn/



cpu,�ڴ棬Ӳ��io��Ϣ��ɾ���˵�1-3�к����һ�У�����������js����

shell �ű����£�

``` shell 
#!/bin/bash
if (( $# != 1))
then
    echo "please input sum time:"
    exit 1
fi
sar -u 1 $1 | sed '1,3d'|sed '$d' > sar_cpu_1.txt
sar -r 1 $1 |sed '1,3d'|sed '$d' > sar_men_1.txt
sar -b 1 $1 |sed '1,3d'|sed '$d' > sar_io_1.txt
```


![CPUͳ��ͼ](cpu.png  "CPUͳ��ͼ")

![�ڴ�ͳ��ͼ](men.png  "�ڴ�ͳ��ͼ")

![IOͳ��ͼ](io.png  "ioͳ��ͼ")

sar����˵����

http://github.com/284772894/sar_Highcharts/raw/master/txt/sar.txt)