### 说明-厂区信息管理 
     *文档与原型结合一起阅读，如果不一致，以文档为准，如果有问题请call me*
     厂区信息管理：
     厂区列表，名称和企业编码查询；
     厂区新增（企业编码唯一）；
     厂区详情；
     厂区修改（企业编码不能修改）；
     厂区删除（确认删除提示）；
     

###  新增“厂区信息表”
     企业编号  enterprise code
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
     
### 建表语句 DDL   
```sql

CREATE TABLE `industrial_zone` (
  `enterprise_code` varchar(64) NOT NULL COMMENT '企业编号',
  `enterprise_name` varchar(255) NOT NULL COMMENT '企业名称',
  `enterprise_address` varchar(255) DEFAULT NULL COMMENT '企业经营地址',
  `enterprise_website` varchar(255) DEFAULT NULL COMMENT '企业官网',
  `enterprise_phone` varchar(255) DEFAULT NULL COMMENT '企业电话',
  `lng` double(11,6) DEFAULT NULL COMMENT '经度lng  (6位小数)',
  `lat` double(11,6) DEFAULT NULL COMMENT '纬度lat  (6位小数)',
  `enterprise_profile` varchar(1000) DEFAULT NULL COMMENT '企业简介',
  `recruitment_info` varchar(255) DEFAULT NULL COMMENT '招聘信息 图片地址',
  `enterprise_photo` varchar(255) DEFAULT NULL COMMENT '厂区照片',
  `enterprise_map` varchar(255) DEFAULT NULL COMMENT '厂区地图',
  `note` varchar(255) DEFAULT NULL COMMENT '备注',
  `collector_name` varchar(20) DEFAULT NULL COMMENT '信息收集人员姓名',
  PRIMARY KEY (`enterprise_code`) USING BTREE
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COMMENT='工业园区';

```   
     

### 时间评估 
    全职两个工作日，兼职一周，预定交付时间3.28上午。
    任务指派，L先生
    
### 厂区统计 本次不做 

### 
