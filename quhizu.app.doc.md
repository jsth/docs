### 说明
    临时开放接口文档 主要便于沟通 和存档
	host 依然使用原来的
### 【客户经理】
### 申请管理-合同概要信息
    原接口地址 http://127.0.0.1:40090/app/contractInfoQueryApp.json?contractId=2020031347675553
### 现接口地址 同；返回内容新增 商铺门店信息字段: store
    "store":{"companyName":"熊超测试门店","storeId":19,"storeCode":"648810001"}
### 查看返回内容 [app.contractInfoQueryApp.json](app.contractInfoQueryApp.json)


### 业绩查询 
    原接口地址 http://127.0.0.1:40090/app/querySalesCommissionYWY.json  入参数：pageSize、pageNumber
### 现接口地址 同；返回内容说明 ；原型中 “成交单数”暂不支持，取消掉。sales_commission
    增加 date 字段：当月日期 如2020-03
    salesCommissionList 数组元素中增加字段 ；字段意义与之前一致。
    {"date":"2020-02","oldLoanAmount":"83.33","newLoanAmount":"17000.00","newLoanCount":17,"newOverdueCount":5,"oldLoanCount":1,"salesCommissionAmount":"0.00","newOverdueAmount":"17000.00","oldOverdueCount":1,"oldOverdueAmount":"0.00"}
    
    新增订单：newLoanAmount  newLoanCount
    成交订单：审核通过	暂不支持，取消
    新增逾期：newOverdueAmount  newOverdueCount
    存量订单：oldLoanAmount  oldLoanCount
    存量逾期	：oldOverdueAmount oldOverdueCount
### 查看返回内容 [app.querySalesCommissionYWY.json](app.querySalesCommissionYWY.json)
    