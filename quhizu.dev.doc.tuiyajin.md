### 文档更新
    2020.3.24 退款状态：未退款、已导出、退款失败、退款成功

### 说明-退押金开发
     退押金开发说明
     【用户】通过电话向【客服】发起退押申请；
     【客服】通过 手机号/身份证，在“租后管理列表”中查询用户合同（客服有权限查询所有合同），
             查看合同列表时，人工判断是否能退押（合同已完成，付租完成，付租详情中没有逾期行为）
             点击“添加退押申请”，（点击时程序要判断能否退押金：付租完成，没有逾期行为）
             跳转到退押申请页面（携带参数：合同编码），
             通过合同编号自动填充数据字段（其中：金额，卡号，开户行，可改），
             确认提交，保存数据到“退押表”中。
     【财务】查看“退押申请列表”，可以根据时间，合同，状态，用户，筛选，导出，导出后自动设置状态为 已导出 。
	         
			 退款状态：未退款、已导出、退款失败、退款成功。
             退款状态=“未退款”可勾选导出，导出之后状态标记为“已导出”。
             退款状态=“退款失败”的记录，可编辑修改信息，修改后状态更新为"未退款"。
             退款状态=“已导出”的记录，可点击退款完成，将该记录状态修改为“退款成功”；可点击退款失败将记录状态更新为退款失败。
             退款状态=退款成功，只能查看详情。
###  新增“退押表”
      申请时间
      
      客户姓名
      
      身份证
      
      合同编号
      
      销售日期 
      
      申请金额 
      
      退款原因  
      
      开户行支行 
      
      银行卡号
      
      退款状态：未退款、已导出、退款失败、退款成功

### 时间评估-退押金开发 
    全职两个工作日，兼职一周，预定交付时间3.28上午。
    任务指派，M先生
    
### 图片

![Image text](img/queryLoanContractInfoList.png)    
![avatar](img/addD.png)  
![Alt text](img/listD.png)	 