##������:��ʱ����
###���
iuap-dispatch-service������ܰ�����ӡ�ɾ������ͣ���������񡣲����ṩ���ⲿ���õ�Rest���񣬲��ұ���Ҳ���������������ý��棬
����������ȣ���־��ѯ�ȹ��ܡ�

###���ݿ���ϢԤ��
1.ִ�����ݿ�ű���Ԥ�����ݿ����Ϣ

����ִ��examples��Ŀ��sqlĿ¼�е�dll.sql��index.sql��dml.sql�������ݿⲢ��ʼ�����ݡ�
Ԥ�����ݿ��dispatch_taskway����Ϣ�����ű����û�Ҫִ��������嵥����Ҫ�û�Ԥ�ý�ȥ������url��ָ��Ҫִ�еĶ�ʱ����ͨ��HTTP�ķ�ʽ���ʡ�

###��������ṩ���ַ�ʽ����

1.
�½�����Rest�ӿ�

A������һ��������

(1)Rest����URL 

��http://localhost:8080/iuap-dispatch-service/dispatchserver/add.do�� 

(2)����,��ʽ����

{"replace":true,"recallConfig":{"data":{},"option":{"url":"http://localhost:8080/iuap-dispatch-service/dispatchserver/pause.do"},"recallType":"HTTP"},"taskConfig":{"triggerType":"SimpleTrigger","jobCode":"22b511e8-1b80-4f4d-b65e-48f52d8aa682","groupCode":"simpleTaskGroup","startDate":1463813876403,"endDate":null,"priority":0,"timeConfig":{"interval":2,"intervalType":"SECOND","isForever":false,"repeatCount":1}}};

B������һ��Cron���ʽ����

(1)Rest����URL 

http://localhost:8080/iuap-dispatch-service/dispatchserver/add.do��

(2)����,��ʽ����

{\"replace\":true, \"recallConfig\":{\"data\":{\"serverName\":\"Windows 2003\"},\"option\":{\"url\":\"http://localhost:8080/iuap-dispatch-service/dispatchserver/pause.do\"},\"recallType\":\"HTTP\"}, \"taskConfig\":{\"cronExpress\":\"* */1 * * * ?\",\"groupCode\":\"cronTaskGroup\",\"jobCode\":\"cronTask\",\"priority\":0,\"triggerType\":\"CronTrigger\"}}";

###ͨ����������������

�����war�����𵽷������Ϸ�����ҳhttp://IP:PORT/iuap-dispatch-service������������.

####�����б����

��������ͼ��ʾ��


![](/articles/application/7-/images/7-4-1.png)

����˵��

�����������顢�������񡢲鿴��־���������������������ͣ�á�

����˵������

���Ϊ�������
�Ҳ�Ϊ�����µ������б���棬��������״̬��ʾΪ��ͬ����ɫ����鿴���񡢲鿴������־��ɾ������Ȳ����������ͣʱ��δ����������ʾͣ�á����ò�����ť��

###�����������

��������ͼ��ʾ��



![](/articles/application/7-/images/7-4-2.png)

����˵�������������ϵ���������Ͻ��½����鰴ť���������棬��д�󱣴档

����˵�����£�

�������ƣ�����ı�ʶ

###��������

��������ͼ��ʾ


![](/articles/application/7-/images/7-4-3.png)

����˵�������������ϵ���������Ͻ��½�����ť����������༭���棬��д�󱣴档

����˵�����£�

1.������룺����ı�ʶ

2.�������ƣ�����ʶ����˼������

3.������飺ָ��������������

4.��Ϣ���գ���������ɹ�������Ϣ�Ľ����˺ͽ��շ�ʽ����Ҫ��չʵ����Ϣ�����߼�)

5.��ʱ�����������ִ��ʱ�䣬ÿ������ִ��һ�Σ���ָ����ʼʱ��

6.���ù���ָ��Ҫִ�е����񣬾�������������Ԥ������˵����

7.����������ִ��ʱ�������ָ���Ĳ���ֵ����ҵ�����

��ʱ�����������ͼ��ʾ��

![](/articles/application/7-/images/7-4-4.png)

����˵�����£�

1.֧��ָ������ʼ����ʱ��

2.֧��ָ��ÿ�졢ÿ�ܣ���ѡ���ܼ�����ÿ�µڼ���ִ������

3.֧��������ѡ�������һ���ڣ�ָ���������������ʱ�����ֹʱ��

###�鿴��������

��������ͼ��ʾ��


![](/articles/application/7-/images/7-4-5.png)

����˵��������������б���������Ҳ�鿴��������ͼ�ꡣ��������������档

����˵�����£�

1.�����ʾ��������ƺ�ִ�����

2.�Ҳ���ʾ�������ϸ��Ϣ

3.�༭����������༭����

4.��־��������־�鿴���棬��ʾ��ǰ�������־

###�޸�����

��������ͼ��ʾ��

![](/articles/application/7-/images/7-4-6.png)

����˵�������������б���������Ҳ����༭����ͼ�ꡣ��������༭���棬��д�󱣴档

����˵�����£�

1.������룺����ı�ʶ
2.�������ƣ�����ʶ����˼������
3.������飺ָ��������������
4.��Ϣ���գ���������ɹ�������Ϣ�Ľ����˺ͽ��շ�ʽ����Ҫ��չʵ����Ϣ�����߼�����
5.��ʱ�����������ִ��ʱ�䣬ÿ������ִ��һ�Σ���ָ����ʼʱ��
6.���ù���ָ��Ҫִ�е����񣬾�������������Ԥ������˵����
7.����������ִ��ʱ�������ָ���Ĳ���ֵ����ҵ�����

###ɾ������

����˵�������������б���������Ҳ���ɾ������ͼ�ꡣ

###��������

��������ͼ��ʾ��


![](/articles/application/7-/images/7-4-7.png)

����˵�������ѡ����ͣ�õ�����ʱ���б�����ʾ���ð�ť�������ť���ø�����

###ͣ������

��������ͼ��ʾ��


![](/articles/application/7-/images/7-4-8.png)

����˵�������ѡ�����������е�����ʱ���б�����ʾͣ�ð�ť�������ťͣ�ø�����

###������������

��������ͼ��ʾ��


![](/articles/application/7-/images/7-4-9.png)

����˵���������ѡ��ťʱ���Ử�����á�ͣ�á�ɾ����ť���б�����л�Ϊ��ѡ״̬��ѡ��������󣬵����ť���в����������ѡ�ص�ԭ��״̬��

###�鿴����ִ����־

��������ͼ��ʾ��

![](/articles/application/7-/images/7-4-10.png)

����˵����

1.������������Ͻǵġ���־����ť����ʾȫ��������־

2.��������������ġ���־����ť����ʾ��ǰ�������־

3.����־��������Ͻǿ���ѡ��Ҫ��ѯ������ѡ��󣬸���ָ���������ѯ����ʾ��־��Ϣ�����ͼ��

����������棺 

![](/articles/application/7-/images/7-4-11.png)

����˵����

1.ѡ�����������ʾ�����µ�����

2.ѡ���������󣬽���ᰴ��ѡ������������ʾ��

###�鿴��־����

��������ͼ��ʾ��

![](/articles/application/7-/images/7-4-12.png)

����˵�������������־�б������������Ҳ�ġ��鿴ԭ�򡱰�ť����ʾ��־���顣

������Ϣ��������ļ�����

###��������

1.��maven��������war����

2.����dispatch_dbinfo.properties �����ļ�������mysql���ݿ������Դ��Ϣ��

3.ִ��dispatch.sql ��tables_mysql.sql ��ʼ�����ݿ�Ľű���

4.Ԥ�����ݿ��dispatch_taskway����Ϣ�����ű����û�Ҫִ��������嵥����Ҫ�û�Ԥ�ý�ȥ������url��ָ��Ҫִ�еĶ�ʱ����ͨ��HTTP�ķ�ʽ���ʡ��������Ҫ�������������ȷ�����Ժ��Դ��

5.Rest������ýӿ��ṩ�������ɾ�ȹ��ܣ�������÷�ʽ�ο����������½ڡ�

6.��������������ϵͳ���ʷ�ʽ 

http://IP:PORT/iuap-dispatch-service

###Ԥ������˵��

��Ҫ�û������ݿ��dispatch_taskwayclass��dispatch_taskway��dispatch_taskparam��Ԥ�ƹ������ݣ�

1.dispatch_taskwayclas���������

2.dispatch_taskway��������Ҫ��url�ֶ�Ϊִ������ʱ�����õ�ҵ�����ĵ�ַ����Ҫ��������õ�Ҫ���ṩ��

3.dispatch_taskparam����������ò����б��ڵ���ҵ�����ʱ�����������ָ����������


###API�ӿ�

###ָ������Beanid��������Cron���ʽ�Ķ�ʱ����

####����

��ӻ򸲸ǻ���Cron���ʽ�Ķ�ʱ��������

####���󷽷�

/dispatchserver/add.do

####����ʽ

post

####�������˵��

<table>
   <tr>
      <td>�����ֶ�</td>
      <td>��ѡ</td>
      <td>����</td>
      <td>��������</td>
      <td>˵��</td>
   </tr>
   <tr>
      <td>recallConfig</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>�ص���Ϣ���ã�Json��ʽ������ο�����˵��</td>
   </tr>
   <tr>
      <td>taskConfig</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>����ִ�����ã�Json��ʽ������ο�����˵��</td>
   </tr>
   <tr>
      <td>replace</td>
      <td>True</td>
      <td>boolean</td>
      <td>��</td>
      <td>�Ƿ񸲸ǣ�Ϊtureʱ���Զ����ǣ�Ϊfalseʱ��������ڻ᷵�ش�����Ϣ</td>
   </tr>
</table>

recallConfig���ݸ�ʽ��

<table>
   <tr>
      <td>�����ֶ�</td>
      <td>��ѡ</td>
      <td>����</td>
      <td>��������</td>
      <td>˵��</td>
   </tr>
   <tr>
      <td>recallType</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>�ص���ʽ��SOCKET/HTTP</td>
   </tr>
   <tr>
      <td>option</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>�ص��ķ�ʽ��ַ��"recallType" = "HTTP"ʱ����ʽΪ{"url":"http://ip:port/XXX"} </td>
   </tr>
   <tr>
      <td>"recallType" = "SOCKET"ʱ����ʽΪ{"host":"ip","port"}</td>
   </tr>
   <tr>
      <td>data</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>���񸽼����ݣ�ִ��ʱ���ݸ����ýӿڣ�����Ϊjson��ʽ</td>
   </tr>
</table>

taskConfig���ݸ�ʽ��

<table>
   <tr>
      <td>�����ֶ�</td>
      <td>triggerType</td>
      <td>��ѡ</td>
      <td>����</td>
      <td>��������</td>
      <td>˵��</td>
   </tr>
   <tr>
      <td>triggerType</td>
      <td></td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>������ʽ��SimpleTrigger/CronTrigger����������������Ͳ�ͬ�仯�� </td>
   </tr>
   <tr>
      <td>�ɲο�sdk�е�CronTaskConfig/SimpleTaskConfig�������������</td>
   </tr>
   <tr>
      <td>jobCode</td>
      <td>SimpleTrigger/CronTrigger</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>��������</td>
   </tr>
   <tr>
      <td>groupCode</td>
      <td>SimpleTrigger/CronTrigger</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>������</td>
   </tr>
   <tr>
      <td>priority</td>
      <td>SimpleTrigger/CronTrigger</td>
      <td>True</td>
      <td>int</td>
      <td>��</td>
      <td>���ȼ������ִ������ִ��</td>
   </tr>
   <tr>
      <td>endDate</td>
      <td>SimpleTrigger/CronTrigger</td>
      <td>True</td>
      <td>Date</td>
      <td>��</td>
      <td>�������ʼʱ��</td>
   </tr>
   <tr>
      <td>cronExpress</td>
      <td>CronTrigger</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>���ʽ��</td>
   </tr>
   <tr>
      <td>startDate</td>
      <td>SimpleTrigger</td>
      <td>True</td>
      <td>Date</td>
      <td>��</td>
      <td>����ʼʱ��</td>
   </tr>
   <tr>
      <td>timeConfig</td>
      <td>SimpleTrigger</td>
      <td>True</td>
      <td>Json</td>
      <td>��</td>
      <td>ʱ�����ã�json��ʽ���ο�TimeConfig���ʽ����</td>
   </tr>
</table>

timeConfig���ݸ�ʽ��

<table>
   <tr>
      <td>�����ֶ�</td>
      <td>��ѡ</td>
      <td>����</td>
      <td>��������</td>
      <td>˵��</td>
   </tr>
   <tr>
      <td>interval</td>
      <td>True</td>
      <td>int</td>
      <td>��</td>
      <td>ִ�м��ʱ�䣬���嵥λ��intervalType</td>
   </tr>
   <tr>
      <td>intervalType</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>ִ�м��ʱ�䵥λ��NULL/MILLISECOND/SECOND/MINUTE/HOUR</td>
   </tr>
   <tr>
      <td>isForever</td>
      <td>True</td>
      <td>boolean</td>
      <td>��</td>
      <td>�Ƿ��ظ�ִ�У�Ϊtrueʱ��һֱ��ʱִ�У�ֱ����ͣ��ɾ������</td>
   </tr>
   <tr>
      <td>repeatCount</td>
      <td>True</td>
      <td>int</td>
      <td>��</td>
      <td>�ظ�������isForeverΪfalseʱ�������ִ��ָ���Ĵ���</td>
   </tr>
</table>

���ز���˵��

<table>
   <tr>
      <td>�����ֶ�</td>
      <td>����</td>
      <td>˵��</td>
   </tr>
   <tr>
      <td>success</td>
      <td>boolean</td>
      <td>true/false</td>
   </tr>
   <tr>
      <td>error</td>
      <td>String</td>
      <td>������Ϣ</td>
   </tr>
   <tr>
      <td>resultValue</td>
      <td>String</td>
      <td>����ֵ��һ��Ϊnull</td>
   </tr>
</table>

###��ͣ����

####����

�����������ƺ���������ͣ����

####���󷽷�

/dispatchserver/pause.do

####����ʽ

post

####�������˵��

<table>
   <tr>
      <td>�����ֶ�</td>
      <td>��ѡ</td>
      <td>����</td>
      <td>��������</td>
      <td>˵��</td>
   </tr>
   <tr>
      <td>jobName</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>��������</td>
   </tr>
   <tr>
      <td>groupName</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>������</td>
   </tr>
</table>

���ز���˵��

<table>
   <tr>
      <td>�����ֶ�</td>
      <td>����</td>
      <td>˵��</td>
   </tr>
   <tr>
      <td>success</td>
      <td>boolean</td>
      <td>true/false</td>
   </tr>
   <tr>
      <td>error</td>
      <td>String</td>
      <td>������Ϣ</td>
   </tr>
   <tr>
      <td>resultValue</td>
      <td>String</td>
      <td>����ֵ��һ��Ϊnull</td>
   </tr>
</table>

###�ָ�����

####����

�����������ƺ������ƻָ�����

####���󷽷�

/dispatchserver/resumeTask.do

####����ʽ

post

�������˵��

<table>
   <tr>
      <td>�����ֶ�</td>
      <td>��ѡ</td>
      <td>����</td>
      <td>��������</td>
      <td>˵��</td>
   </tr>
   <tr>
      <td>jobName</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>��������</td>
   </tr>
   <tr>
      <td>groupName</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>������</td>
   </tr>
</table>

���ز���˵��

<table>
   <tr>
      <td>�����ֶ�</td>
      <td>����</td>
      <td>˵��</td>
   </tr>
   <tr>
      <td>success</td>
      <td>boolean</td>
      <td>true/false</td>
   </tr>
   <tr>
      <td>error</td>
      <td>String</td>
      <td>������Ϣ</td>
   </tr>
   <tr>
      <td>resultValue</td>
      <td>String</td>
      <td>����ֵ��һ��Ϊnull</td>
   </tr>
</table>

###ɾ������

####����

�����������ƺ�������ɾ������

####���󷽷�

/dispatchserver/delete.do

####����ʽ

post

####�������˵��

<table>
   <tr>
      <td>�����ֶ�</td>
      <td>��ѡ</td>
      <td>����</td>
      <td>��������</td>
      <td>˵��</td>
   </tr>
   <tr>
      <td>jobName</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>��������</td>
   </tr>
   <tr>
      <td>groupName</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>������</td>
   </tr>
</table>

���ز���˵��

<table>
   <tr>
      <td>�����ֶ�</td>
      <td>����</td>
      <td>˵��</td>
   </tr>
   <tr>
      <td>success</td>
      <td>boolean</td>
      <td>true/false</td>
   </tr>
   <tr>
      <td>error</td>
      <td>String</td>
      <td>������Ϣ</td>
   </tr>
   <tr>
      <td>resultValue</td>
      <td>String</td>
      <td>����ֵ��һ��Ϊnull</td>
   </tr>
</table>

###����ִ������

####����

�����������ƺ�����������ִ������

####���󷽷�

/dispatchserver/trigger.do

####����ʽ

post

####�������˵��

<table>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>�����ֶ�</td>
      <td>��ѡ</td>
      <td>����</td>
      <td>��������</td>
      <td>˵��</td>
   </tr>
   <tr>
      <td>jobName</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>��������</td>
   </tr>
   <tr>
      <td>groupName</td>
      <td>True</td>
      <td>String</td>
      <td>��</td>
      <td>������</td>
   </tr>
</table>


####���ز���˵��

<table>
   <tr>
      <td>�����ֶ�</td>
      <td>����</td>
      <td>˵��</td>
   </tr>
   <tr>
      <td>success</td>
      <td>boolean</td>
      <td>true/false</td>
   </tr>
   <tr>
      <td>error</td>
      <td>String</td>
      <td>������Ϣ</td>
   </tr>
   <tr>
      <td>resultValue</td>
      <td>String</td>
      <td>����ֵ��һ��Ϊnull</td>
   </tr>
</table>