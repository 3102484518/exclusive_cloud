##��Ϣ����

###ҵ������

��Ϣ������Ҫ�û������û����飬�����û�ˢ��ҳ��ӷ���������ȡ���ݡ������ʼ����ѣ���Ҫ֪ͨ�ܼ�ʱ���͸��û�������û����顣

###����˵��

iuap-message����ṩ�����ֻ����Ͷ��š����͵����ʼ�����APP������Ϣ�Ĺ��ܡ�

1.�ṩ�����ֻ����Ͷ���
2.�ṩ�˷��͵����ʼ�
3.�����ʼ�֧�ֳ��͡�����
4.�����ʼ�֧�ָ�������
5.�ṩ����APP������Ϣ�Ĺ���
6.����չ����Ϣ���ͷ�ʽ��

##�������

###��������

�������Maven���б���ʹ��������������ṩ��������ʽ���£�

1
<dependency>
2
  <groupId>com.yonyou.iuap</groupId>
3
  <artifactId>iuap-message</artifactId>
4
  <version>${iuap.modules.version}</version>
5
</dependency>

${iuap.modules.version} Ϊƽ̨��maven˽���Ϸ����������version��

###����˵��

iuap-message����ṩ�����ֻ����Ͷ��š����͵����ʼ�����APP������Ϣ�Ĺ��ܡ�

1.��Ϣ���� 

�ڹ�˾���е���Ϣ����ƽ̨�Ļ����ϣ����ô�ƽ̨��REST���񣬽�ҵ�����ݰ�װ�ɷ���Ҫ��ĸ�ʽ�����͵�ƽ̨�ϣ����APP�����͡����û����ƶ���Ҳ��Ҫ��װƽ̨�ṩ��SDK��

2.���Ͷ��� 

���Ͷ��ŵĹ����ǻ��ڹ�˾�Ķ�������ƽ̨��ͨ����ƽ̨���ṩ��REST���񣬰���ƽ̨��Ҫ�󣬽����ݷ�װ�ύ��ƽ̨����ɶ��ŷ�������Ŀǰ֧�ֹ��ڵ��ƶ�����ͨ�͵����������硣

3.�����ʼ� 

�����ʼ������ǻ���JavaMailʵ�ֵ��ʼ����ͷ���ʹ��JDKԭ����javax.mail�������ɷ����ʼ��ķ���

��Ҫ�����������£�

1.��֤��¼Ȩ��Authenticator

2.�������õ�Properties��Authenticator����һ��Session

3.����һ��MimeMessageʵ�����������message�������ˡ����⡢���ݵ�

4.�����ʼ�Transport.send(message);

##ʹ��˵��

###�����˵��

iuap-message����ṩ�����ֻ����Ͷ��š����͵����ʼ�����APP������Ϣ�Ĺ��ܡ�

###�������

�������ļ�message-senderInfo.xml(��������ʾ�������õ�)�ŵ����̵�classpath�£������maven���̣�����src/main/resourcesĿ¼�¼���

###��������

��Ϣ��������ṩ��ʾ������iuap-message-example���û��ɴ�maven�������أ�ʾ���������н�Ϊ�����Ķ�iuap-message�����ʹ��ʾ�����롣

###��������

��ֱ�Ӳο�����ʾ�����̣�

1.��������ļ���

�������ļ�message-senderInfo.xml(��������ʾ�������õ�)�ŵ����̵�classpath�£������maven���̣�����src/main/resourcesĿ¼�¼���

2.������Ϣ����Ľӿڷ�����������Ϣ:

1
// ������Ϣ������
2
MessageReceiver emailReceivers = new EmailReceiver("username1@domain.com,username2@domain.com");
3
 
4
// ������Ϣ����
5
MessageContent emailContent = new EmailContent("���Ǳ���1", "��������1");
6
 
7
// ������Ϣ
8
List<MessageResponse> responseList = new MessageSend(emailReceivers, emailContent).send(); 


###���ýӿ�

####���� 

���š��ʼ���APP��Ϣ���ͽӿ�

####���󷽷� 

new MessageSend(msgReceivers, msgContent).send();

�������˵��

<table>
   <tr>
      <td>�����ֶ�</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>��ѡ</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>����</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>����</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>˵��</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>msgReceivers</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>True</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>MessageReceiver</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>��Ϣ�Ľ����ߣ��ж����ʱ�򣬰���Ӣ�ġ�,���ָ�</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>msgContent</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>True</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>MessageContent</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>��Ϣ���ݣ�������Ϣ���⣬��Ϣ���ݣ�����ʱ�䡣������Ϣ����ͷ���ʱ��Ǳ���</td>
   </tr>
   <tr>
      <td></td>
   </tr>
</table>

1.msgReceivers��Ϣ�����ߡ��������ʼ���ַ�������ǵ绰���룬������APP ID��

2.msgContent��Ϣ���ݣ�����������Ϣ���⡢�ı����ݡ�

####����

���š��ʼ���APPͨ����Ϣͨ�����ͽӿ�

####���󷽷�

new MessageSend(msgReceivers, msgContent, channel).send();

####�������˵��

<table>
   <tr>
      <td>�����ֶ�</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>��ѡ</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>����</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>����</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>˵��</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>msgReceivers</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>True</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>MessageReceiver</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>��Ϣ�Ľ����ߣ��ж����ʱ�򣬰���Ӣ�ġ�,���ָ�</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>msgContent</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>True</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>MessageContent</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>��Ϣ���ݣ�������Ϣ���⣬��Ϣ���ݣ�����ʱ�䡣������Ϣ����ͷ���ʱ��Ǳ���</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>channel</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>false</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>String</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>��Ϣͨ������</td>
   </tr>
   <tr>
      <td></td>
   </tr>
</table>


1.msgReceivers ��Ϣ�����ߡ��������ʼ���ַ�������ǵ绰���룬������APP ID��

2.msgContent ��Ϣ���ݣ�����������Ϣ���⡢�ı����ݡ�

3.channel ��Ϣͨ�����룬��Ҫע����Ϣͨ��������ο���Ϣͨ������ĵ���

֧����Ϣͨ������չ����չ�������£� 

(1)Ĭ��֧��sms,messagepush,email���û�����չ�Լ�����Ϣͨ������Ҫ��չ��Ϣͨ�������������ļ�message-senderInfo.property�������Լ�����Ϣͨ��,���������ʾ�����ò���

<msconfig>
02
<!-- ���ŷ����������  START-->
03
  <sms>
04
    <corpId></corpId><!-- �˻�ID -->
05
    <secretKey></secretKey><!-- �ӿڵ�����Կ -->
06
    <url>http://umessage.yyuap.com/remote/sendSms.do</url><!-- ���ŷ�����URL -->
07
  </sms>
08
<!-- ���ŷ����������  END-->
09
 
10
<!-- ��Ϣ���Ͳ�������  START-->
11
  <messagepush>
12
    <userName></userName><!-- �˻���(������̨��¼��) -->
13
    <userKey></userKey><!-- Զ�̽ӿ���Կ -->
14
    <url>http://upush.yyuap.com/remote/req.do</url><!-- ��Ϣ���ͷ�����URL -->
15
  </messagepush>
16
<!-- ��Ϣ���Ͳ�������  END-->
17
 
18
<!-- �ʼ������Ͳ�������  START-->
19
  <mail>
20
    <userName></userName><!-- �˻���(�����������˻����˺�) -->
21
    <password></password><!-- ����(�����������˻�������) -->
22
    <hostName>mail.yonyou.com</hostName><!-- �ʼ����ͷ�����SMTP��ַURL -->
23
    <port>25</port><!-- �ʼ����ͷ�����SMTP�˿ں� -->
24
  </mail>
25
<!-- �ʼ������������  END-->
26
 
27
</msconfig>


��2�������Ϣͨ����ʵ���࣬ʵ�ֽӿ�com.yonyou.uap.service.IMessageSendChannelExt�������õ��ļ�message-channelExt.xml�С�

view sourceprint?
1
<MessageSendChannelExt>
2
    <mail>com.yonyou.uap.service.impl.mail.EMailSend</mail>
3
    <sms>com.yonyou.uap.service.impl.sms.SMSSend</sms>
4
    <messagepush>com.yonyou.uap.service.impl.messagepush.MessagePush</messagepush>
5
</MessageSendChannelExt>


(3)��Ϣ����������ÿ���ͨ�����·�ʽ��ȡ��

1
ISenderInfoFetch getEmailSenderInfo = new SenderInfoFetchByXML();
2
Map<String, Object> channelInfoMap = getEmailSenderInfo.getSenderInfo(����Ϣͨ�����롱);

(4)��Ҫ�����������war��aplication.xmk��������������bean

1
<bean id="senderInfoFetch" class="com.yonyou.uap.message.service.impl.SenderInfoFetchByDB" />
2
<bean id="senderInfoFetcher" class="com.yonyou.uap.service.SenderInfoFetcher" />

###��չ����

1.����HTML���ݵĵ����ʼ��� 

�������ʼ���������ʱ������ֱ�ӱ�дHTML���룬���£�

1
StringBuffer htmlContent = new StringBuffer();
2
htmlContent.append("<h1>���Ǳ���</h1>");
3
htmlContent.append("<h3>��ҵ��������Ӫ֧��ƽ̨</h3>");
4
htmlContent.append("<div><img src='http://img4.3lian.com/sucai/img6/230/29.jpg'></div>");
5
htmlContent.append("<a href='http://iuap.yonyou.com/'>���ѿ���ƽ̨</a>");
6
MessageContent mailContent = new EmailContent("HTML Mail����", htmlContent.toString());

�����Ϳ��Է���HTML��ʽ���ʼ���

1.֧���ʼ����ͣ����ͣ����͸���

MessageContent mailContent = new EmailContent(title, content, copyReceivers, blindCopyReceivers, attachFiles);

<table>
   <tr>
      <td>�����ֶ�</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>��ѡ</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>����</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>����</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>˵��</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>title</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>True</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>String</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>�ʼ��ı���</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>content </td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>True</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>String</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>��Ϣ����</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>copyReceivers </td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>false</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>String</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>�����ˣ����������ʱ���ð��Ӣ�Ķ��ŷָ���</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>blindCopyReceivers </td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>false</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>String</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>�����ˣ����������ʱ���ð��Ӣ�Ķ��ŷָ���</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>attachFiles </td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>false</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>String[]</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>�����ı���·���� </td>
   </tr>
</table>

1
MessageContent mailContent = new EmailContent(title, content, copyReceivers, blindCopyReceivers, attachFileBytesMap)


<table>
   <tr>
      <td>�����ֶ�</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>��ѡ</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>����</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>����</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>˵��</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>title</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>True</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>String</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>�ʼ��ı���</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>content </td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>True</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>String</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>��Ϣ����</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>copyReceivers </td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>false</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>String</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>�����ˣ����������ʱ���ð��Ӣ�Ķ��ŷָ���</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>blindCopyReceivers </td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>false</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>String</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>�����ˣ����������ʱ���ð��Ӣ�Ķ��ŷָ���</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>attachFileBytesMap </td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>false</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>Map </td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>����֧�ֶ����Ʒ���,Map ��ʾ<�ļ���,��Ӧ���ļ���������> </td>
   </tr>
   <tr>
      <td></td>
   </tr>
</table>

1
MessageContent mailContent = new EmailContent(title, content, copyReceivers, blindCopyReceivers, attachFileUrls)


<table>
   <tr>
      <td>�����ֶ�</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>��ѡ</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>����</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>����</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>˵��</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>title</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>True</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>String</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>�ʼ��ı���</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>content </td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>True</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>String</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>��Ϣ����</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>copyReceivers </td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>false</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>String</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>�����ˣ����������ʱ���ð��Ӣ�Ķ��ŷָ���</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>blindCopyReceivers </td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>false</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>String</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>�����ˣ����������ʱ���ð��Ӣ�Ķ��ŷָ���</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>attachFileUrls </td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>false </td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>List </td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>-</td>
   </tr>
   <tr>
      <td></td>
   </tr>
   <tr>
      <td>ͨ��url��ַ�����Ʒ��͸��� </td>
   </tr>
   <tr>
      <td></td>
   </tr>
</table>