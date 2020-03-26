### 说明-厂区信息管理 基于 工作单位管理 加字段
     * 文档与原型结合一起阅读，如果不一致，以文档为准，如果有问题请call me*
     * 需求原型地址 http://zbox.quhizu.com/zentao/story-view-16.html *
	 
	 厂区信息管理基于工作单位管理加字段（commonAddressManage）；
	 
     厂区信息管理：
     厂区列表，；
     厂区新增（）；
     厂区详情；
     厂区修改（）；
     厂区删除（确认删除提示）；
     

###  新增“厂区信息”
     
     企业名称  
     企业经营地址 
     企业官网 
     企业电话 
     经度lng  (6位小数)
     纬度lat  (6位小数)
     企业简介及生产产品 (最多1000字)
     招聘信息图片  (上传图片保存地址)
     厂区照片      (上传图片保存地址)
     厂区地图      (上传图片保存地址)
     备注
     信息收集人员姓名
	 状态 (1.待完善,2.已完善：所有字段全部填完不为空，不为空白;默认1;)
     
### 建表语句 DDL   
```sql

	ALTER TABLE  `common_address`    
	ADD COLUMN  `status` tinyint(4) NOT NULL DEFAULT 1 COMMENT '状态 (1.待完善,2.已完善：所有字段全部填完不为空，不为空白;默认1;)',
	#ADD COLUMN  `enterprise_name` varchar(255) NOT NULL COMMENT '企业名称',
	ADD COLUMN  `enterprise_address` varchar(255) DEFAULT NULL COMMENT '企业经营地址',
	ADD COLUMN  `enterprise_website` varchar(255) DEFAULT NULL COMMENT '企业官网',
	ADD COLUMN  `enterprise_phone` varchar(255) DEFAULT NULL COMMENT '企业电话',
	ADD COLUMN  `lng` double(11,6) DEFAULT NULL COMMENT '经度lng  (6位小数)',
	ADD COLUMN  `lat` double(11,6) DEFAULT NULL COMMENT '纬度lat  (6位小数)',
	ADD COLUMN  `enterprise_profile` varchar(1000) DEFAULT NULL COMMENT '企业简介',
	ADD COLUMN  `recruitment_info` varchar(255) DEFAULT NULL COMMENT '招聘信息 图片地址',
	ADD COLUMN  `enterprise_photo` varchar(255) DEFAULT NULL COMMENT '厂区照片',
	ADD COLUMN  `enterprise_map` varchar(255) DEFAULT NULL COMMENT '厂区地图',
	ADD COLUMN  `work_card_photo` varchar(255) DEFAULT NULL COMMENT '工牌照片',
	ADD COLUMN  `note` varchar(255) DEFAULT NULL COMMENT '备注',
	ADD COLUMN  `collector_name` varchar(20) DEFAULT NULL COMMENT '信息收集人员姓名';
  
  
```   
  
  

### 时间评估 
    全职两个工作日，兼职一周，预定交付时间3.28上午。
    任务指派，L先生
    
### 厂区统计 本次不做 

### 改善需求 查询条件去空白
    预计完成时间  3.31
    http://zbox.quhizu.com/zentao/story-view-17.html
	
	申请管理&&合同管理&&租后管理：所有状态下的查询条件中的“合同编号”、“身份证号”两个输入框，自动去除收尾空格。 
    客户管理&&风控管理：所有状态下的查询条件中的“身份证号”这个输入框，自动去除收尾空格。 
    注释：实际应用中，用户习惯复制粘贴合同编号或身份证号进行查询，因收尾空格原因导致查询失败，因此要求技术层面自动去除收尾空格。


