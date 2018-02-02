## ��ο���widget


### ����widget��߱���֪ʶ

Widget ������Ա��Ҫ��Ϥjs��react��uui��comonjs������ǰ�˿�����������д����ʱҪ��ѭAMD�ȴ��ڹ淶����������д�ο�
Google JavaScript ����淶ָ�ϣ�<http://alloyteam.github.io/JX/doc/specification/google-javascript.xml>

 һ��widget xml����ṹ���£�

	<?xml version="1.0" encoding="UTF-8"?>
	<Module><ModulePrefs title="����-����"></ModulePrefs>
	<Content type="html">
	<![CDATA[
	          Css����  
	          Js����
	          Js��д
	          Css��д
	          Html��д
	         ϵͳ����
	]]>
	</Content>
	</Module>

### ��������������

1��Css���� 

	require('css!./indexlink.css'); 
	require('css!../../font/mehecofont/iconfont.css');
    
   ͨ��require���غô�������һ�Σ�������������

2��Js ����

	require(["/portal/widget/CommonLink6/linkTask.js"],function(task){
	    var hei = getWidgetAttr(��height��);
	    task.init(hei);
	});

3��Js��д

	define(function(require, exports, module ){
	    var styles = require('css!./indexvision.css');
	    var icon = require('css!../../font/mehecofont/iconfont.css');
	    var viewModel={
	        pageInit:function(){
	
	        }
	    };
	    return {
	        init: function(){
	            viewModel.pageInit();
	        }
	    }
	});


4��Css��д

ģ�壺

	.���class  widgetƤ��class  ҵ��class{
	     ��.
	}

ʾ����

	.commonlink .u-panel-heading{
	    background: #eeeeef;
	    border-radius: 10px;
	    height: 40px;
	    line-height: 40px;
	} 

˵����

	1�����class����ҳ�������л�ʱ����
    2��widget Ƥ��class ���ڲ��ָ��Ի�ʱ�༭С����Ƥ��ʱ��������
    3��ҵ��class������widgetҵ����

5��Html��д

Html��дҪ��ѭuui �ؼ�Ҫ��html���ݰ󶨡��¼���

ʾ����

	<html>
	    <head>
	        <title></title>
	    </head>
	    <body>
	        <div class="oa-task width-full oaApprove">
	            <div class="u-panel">
	                <div class="u-panel-heading clearfix">
	                    <span class="pull-left"><strong>OA��������</strong></span>
	                    <ul class="pull-right height-full OAsc">
	                        <li class="pull-left title">
	                            <a href="javaScript:void(0)" searchtype="unread" data-bind="click:$root.search">��������</a>
	                        </li>
	                        <li class="pull-left title">
	                            <a href="javaScript:void(0)" searchtype="incoming" data-bind="click:$root.search">��������</a>
	                        </li>
	                    </ul>
	                </div>
	                <div class="u-panel-body">
	                    <div u-meta='{"id":"oaGrid","data":"dataTable","type":"grid","onBeforeClickFun":"onClickFun"}'>
	                        <div options='{"field":"title","dataType":"String","editType":"string","sortable":true,"canSwap":true}'></div>
	                        <div options='{"field":"sender","dataType":"String","editType":"string" ,"renderType":"timeRender","sortable":true}'></div>
	                        <div options='{"field":"senddate","dataType":"String","editType":"string","sumCol":true}'></div>
	                    </div>
	                </div>
	            </div>
	        </div>
	    </body>
	</html>


6��ϵͳ����

�ڿ���widget�����У����漰��ϵͳ�������Ļ�ȡ���磺context(/portal��/integration)��widgetid�ȡ�
ϵͳĿǰ�ṩ����ϵͳ������ע�룺

(1).${context}��Ӧ��������
ʹ��ʾ�����£�

![](/articles/portal/6-/images/4-1.png)
<p align="center">ͼ 1</p>
 
(2).${widgetId}, С������ʶ
ʹ��ʾ�����£�

![](/articles/portal/6-/images/4-2.png)
<p align="center">ͼ 2</p>


### Widgetʵս

�ֲ�ͼ����

1��autoplay.xml����

	<?xml version="1.0" encoding="UTF-8"?>
	<Module>
	    <ModulePrefs title="��ҳ�ֲ�ͼ" description="autoplay">
	    </ModulePrefs>
	    <UserPref status="1" name="height" display_name="�߶�" datatype="string" default_value="240" required="true" />
	    <UserPref status="1" name="number" display_name="ͼƬ����" datatype="string" default_value="3" required="true" />
	    <Content type="html" inline="true">
	        <![CDATA[
	        <div class="swiper-container width-full"  id="${widgetId}">
	            <div class="swiper-wrapper">
	
	            </div>
	        </div>
	            <script type="text/javascript">
	                require(["./widget/autoplay/autoplay.js"],function(task){
	                    var count=getWidgetAttr("${widgetId}",'number');
	                    var height=getWidgetAttr("${widgetId}",'height');
	                    task.init("${widgetId}",count,height);
	                })
	            </script>
	        ]]>
	    </Content>
	</Module>

2��autoplay.js����

	define(function(require, exports, module ){
	    var html = require('text!./index.html');
	    var styles = require('css!./index.css');
	    var viewModel={
	        pageInit:function(widgetId,count,height){
	            $('#'+widgetId).css('height',height);
	            for(var i=1;i<=count;i++){
	                var str='<div class="swiper-slide swiper-no-swiping" ><img src="./widget/autoplay/images/'+i+'.jpg" class="img-responsive"> </div>';
	                $('#'+widgetId).children().append(str);
	            }
	            var mySwiper = new Swiper ('#'+widgetId, {
	                loop:'true',
	                autoplay:3000,
	                speed:1000,
	                direction:'horizontal',
	                autoplayDisableOnInteraction:'false'
	            })
	        }
	    };
	    return {
	        init: function(widgetId,count,height){
	            viewModel.pageInit(widgetId,count,height);
	        }
	    }
	});

3��Ч��ͼ����


![](/articles/portal/6-/images/4-3.png)
<p align="center">ͼ 3</p>