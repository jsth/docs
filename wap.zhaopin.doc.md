# 简介

**标题**：demo

**简介**：请先阅读 Terms of service 

**HOST**:localhost:28003

**联系人**:

**接口路径**：/v2/api-docs


# wap-controller
    
## getAllEntity

**接口说明**:


**接口地址**:`/p/RecruitInfo`


**请求方式**：`get`


**consumes**:``


**produces**:`["*/*"]`

**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|user_id| user_id  | query | false |integer  |    |
                

**响应数据**:

```json
[
    {
        "add_time": "",
        "age_max": 0,
        "age_min": 0,
        "apply": 0,
        "city": "",
        "company_name": "",
        "district": "",
        "education": 0,
        "label": "",
        "lat": 0,
        "lng": 0,
        "money_str": "",
        "num": 0,
        "province": "",
        "recruit_id": 0,
        "sex": 0,
        "status": 0,
        "street": "",
        "up_sort": 0,
        "up_time": ""
    }
]
```
**响应参数说明**:

| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|add_time|   |string  |    |
|age_max| 最高年龄:45  |integer  |    |
|age_min| 最低年龄:18  |integer  |    |
|apply| 申请状态:0未申请，1已申请  |integer  |    |
|city| 地市  |string  |    |
|company_name| 公司名称  |string  |    |
|district| 区县  |string  |    |
|education| 最低学历:0不限，1初中， 2中专/高中，3大专，4本科，5硕士  |integer  |    |
|label| 标签：岗位标签最多5个:普工|车间|搬运|叉车|电工|焊工|维修|木工|组装|电器  |string  |    |
|lat| 维度  |number  |    |
|lng| 精度  |number  |    |
|money_str| 薪资预算文本：3000-5000/月,100-200/天,10-20/小时  |string  |    |
|num| 招聘人数  |integer  |    |
|province| 省/直辖市  |string  |    |
|recruit_id| 招聘主键  |integer  |    |
|sex| 性别要求:0.不限，1.男性，2.女性  |integer  |    |
|status| 状态：200.发布上架,0.下架  |integer  |    |
|street| 详细地址：仅街道楼栋门牌  |string  |    |
|up_sort| 首页置顶排序  |integer  |    |
|up_time|   |string  |    |


**响应状态码说明**:

| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |RecruitInfo对象|
                | 401 | Unauthorized  ||
                | 403 | Forbidden  ||
                | 404 | Not Found  ||
                

        
    
## visit

**接口说明**:


**接口地址**:`/p/RecruitInfo/{id}`


**请求方式**：`get`


**consumes**:``


**produces**:`["*/*"]`

**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|id| id  | path | true |string  |    |
                |user_id| user_id  | query | false |integer  |    |
                

**响应数据**:

```json
{
    "apply": {},
    "detail": {
        "id": 0,
        "img1": "",
        "img2": "",
        "img3": "",
        "img4": "",
        "img5": "",
        "img6": "",
        "img7": "",
        "img8": "",
        "img9": "",
        "text1": "",
        "text2": "",
        "text3": "",
        "text4": ""
    },
    "info": {
        "add_time": "",
        "age_max": 0,
        "age_min": 0,
        "apply": 0,
        "city": "",
        "company_name": "",
        "district": "",
        "education": 0,
        "label": "",
        "lat": 0,
        "lng": 0,
        "money_str": "",
        "num": 0,
        "province": "",
        "recruit_id": 0,
        "sex": 0,
        "status": 0,
        "street": "",
        "up_sort": 0,
        "up_time": ""
    }
}
```
**响应参数说明**:

| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|apply|   |object  |    |
|detail|   |string  | RecruitDetail对象   |
|info|   |string  | RecruitInfo对象   |


**schema属性说明**

**RecruitDetail对象**

| 参数名称         |  说明          |   类型  |  schema |
| ------------ | ------------------|--------|----------- |
|id | 招聘主键   |integer  |    |
                |img1 | 照片地址1-9：最多9张   |string  |    |
                |img2 | 照片地址1-9：最多9张   |string  |    |
                |img3 | 照片地址1-9：最多9张   |string  |    |
                |img4 | 照片地址1-9：最多9张   |string  |    |
                |img5 | 照片地址1-9：最多9张   |string  |    |
                |img6 | 照片地址1-9：最多9张   |string  |    |
                |img7 | 照片地址1-9：最多9张   |string  |    |
                |img8 | 照片地址1-9：最多9张   |string  |    |
                |img9 | 照片地址1-9：最多9张   |string  |    |
                |text1 | 详情第一段文本：薪资说明   |string  |    |
                |text2 | 详情第二段文本：福利待遇   |string  |    |
                |text3 | 详情第三段文本：公司简介   |string  |    |
                |text4 | 详情第三段文本：其他说明   |string  |    |
                

**RecruitInfo对象**

| 参数名称         |  说明          |   类型  |  schema |
| ------------ | ------------------|--------|----------- |
|add_time |    |string  |    |
                |age_max | 最高年龄:45   |integer  |    |
                |age_min | 最低年龄:18   |integer  |    |
                |apply | 申请状态:0未申请，1已申请   |integer  |    |
                |city | 地市   |string  |    |
                |company_name | 公司名称   |string  |    |
                |district | 区县   |string  |    |
                |education | 最低学历:0不限，1初中， 2中专/高中，3大专，4本科，5硕士   |integer  |    |
                |label | 标签：岗位标签最多5个:普工|车间|搬运|叉车|电工|焊工|维修|木工|组装|电器   |string  |    |
                |lat | 维度   |number  |    |
                |lng | 精度   |number  |    |
                |money_str | 薪资预算文本：3000-5000/月,100-200/天,10-20/小时   |string  |    |
                |num | 招聘人数   |integer  |    |
                |province | 省/直辖市   |string  |    |
                |recruit_id | 招聘主键   |integer  |    |
                |sex | 性别要求:0.不限，1.男性，2.女性   |integer  |    |
                |status | 状态：200.发布上架,0.下架   |integer  |    |
                |street | 详细地址：仅街道楼栋门牌   |string  |    |
                |up_sort | 首页置顶排序   |integer  |    |
                |up_time |    |string  |    |
                

**响应状态码说明**:

| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |招聘详情对象|
                | 401 | Unauthorized  ||
                | 403 | Forbidden  ||
                | 404 | Not Found  ||
                

        
    
## apply

**接口说明**:


**接口地址**:`/p/RecruitInfo/{id}/apply`


**请求方式**：`put`


**consumes**:`["application/json"]`


**produces**:`["*/*"]`

**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|id| id  | path | true |string  |    |
                |user_id| user_id  | query | true |integer  |    |
                

**响应数据**:

```json

```
**响应参数说明**:

暂无


**响应状态码说明**:


| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  ||
                | 201 | Created  ||
                | 401 | Unauthorized  ||
                | 403 | Forbidden  ||
                | 404 | Not Found  ||
                

        
    
## UserIdByPhone

**接口说明**:


**接口地址**:`/p/UserIdByPhone/{phone}`


**请求方式**：`get`


**consumes**:``


**produces**:`["*/*"]`

**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|phone| phone  | path | true |string  |    |
                

**响应数据**:

```json

```
**响应参数说明**:

暂无


**响应状态码说明**:

| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  ||
                | 401 | Unauthorized  ||
                | 403 | Forbidden  ||
                | 404 | Not Found  ||
                

        
    
## saveOrUpdateEntityUserResume

**接口说明**:


**接口地址**:`/p/UserResume`


**请求方式**：`post`


**consumes**:`["application/json"]`


**produces**:`["*/*"]`

**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|arrival_time| 到岗时间:随时到岗，一周到岗(默认)，两周到岗，月内到岗  | query | false |string  |    |
                |career_company1| 工作经历单位1：标1为最近一份工作;可以不填，  | query | false |string  |    |
                |career_company2| 工作经历单位2：可以不填如果要填必须先填1  | query | false |string  |    |
                |career_hiredate1| 工作经历入职日期1  | query | false |string  |    |
                |career_hiredate2| 工作经历入职日期2  | query | false |string  |    |
                |career_leavedate1| 工作经历离职日期1  | query | false |string  |    |
                |career_leavedate2| 工作经历离职日期2  | query | false |string  |    |
                |college| 毕业学校  | query | false |string  |    |
                |domicile| 户籍地:默认 重庆  | query | false |string  |    |
                |education| 学历:0无，1初中， 2中专/高中，3大专，4本科，5硕士及以上;默认2  | query | false |integer  |    |
                |id_no| 身份证号码  | query | false |string  |    |
                |job_objective| 求职意向：填写 默认 岗位不限  | query | false |string  |    |
                |major| 专业技能  | query | false |string  |    |
                |phone| 注册手机号/登录凭证  | query | false |string  |    |
                |sex| 性别：1男，2女;默认1  | query | false |integer  |    |
                |user_id| 用户主键  | query | false |integer  |    |
                

**响应数据**:

```json
{
    "arrival_time": "",
    "career_company1": "",
    "career_company2": "",
    "career_hiredate1": "",
    "career_hiredate2": "",
    "career_leavedate1": "",
    "career_leavedate2": "",
    "college": "",
    "domicile": "",
    "education": 0,
    "id_no": "",
    "job_objective": "",
    "major": "",
    "phone": "",
    "sex": 0,
    "user_id": 0
}
```
**响应参数说明**:

| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|arrival_time| 到岗时间:随时到岗，一周到岗(默认)，两周到岗，月内到岗  |string  |    |
|career_company1| 工作经历单位1：标1为最近一份工作;可以不填，  |string  |    |
|career_company2| 工作经历单位2：可以不填如果要填必须先填1  |string  |    |
|career_hiredate1| 工作经历入职日期1  |string  |    |
|career_hiredate2| 工作经历入职日期2  |string  |    |
|career_leavedate1| 工作经历离职日期1  |string  |    |
|career_leavedate2| 工作经历离职日期2  |string  |    |
|college| 毕业学校  |string  |    |
|domicile| 户籍地:默认 重庆  |string  |    |
|education| 学历:0无，1初中， 2中专/高中，3大专，4本科，5硕士及以上;默认2  |integer  |    |
|id_no| 身份证号码  |string  |    |
|job_objective| 求职意向：填写 默认 岗位不限  |string  |    |
|major| 专业技能  |string  |    |
|phone| 注册手机号/登录凭证  |string  |    |
|sex| 性别：1男，2女;默认1  |integer  |    |
|user_id| 用户主键  |integer  |    |


**响应状态码说明**:

| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |UserResume对象|
                | 201 | Created  ||
                | 401 | Unauthorized  ||
                | 403 | Forbidden  ||
                | 404 | Not Found  ||
                

        
    
## getEntityByIdUserResume

**接口说明**:


**接口地址**:`/p/UserResume/{id}`


**请求方式**：`get`


**consumes**:``


**produces**:`["*/*"]`

**请求参数**：

| 参数名称         | 说明     |     in |  是否必须      |  类型   |  schema  |
| ------------ | -------------------------------- |-----------|--------|----|--- |
|id| id  | path | true |string  |    |
                

**响应数据**:

```json
{
    "arrival_time": "",
    "career_company1": "",
    "career_company2": "",
    "career_hiredate1": "",
    "career_hiredate2": "",
    "career_leavedate1": "",
    "career_leavedate2": "",
    "college": "",
    "domicile": "",
    "education": 0,
    "id_no": "",
    "job_objective": "",
    "major": "",
    "phone": "",
    "sex": 0,
    "user_id": 0
}
```
**响应参数说明**:

| 参数名称         | 说明                             |    类型 |  schema |
| ------------ | -------------------|-------|----------- |
|arrival_time| 到岗时间:随时到岗，一周到岗(默认)，两周到岗，月内到岗  |string  |    |
|career_company1| 工作经历单位1：标1为最近一份工作;可以不填，  |string  |    |
|career_company2| 工作经历单位2：可以不填如果要填必须先填1  |string  |    |
|career_hiredate1| 工作经历入职日期1  |string  |    |
|career_hiredate2| 工作经历入职日期2  |string  |    |
|career_leavedate1| 工作经历离职日期1  |string  |    |
|career_leavedate2| 工作经历离职日期2  |string  |    |
|college| 毕业学校  |string  |    |
|domicile| 户籍地:默认 重庆  |string  |    |
|education| 学历:0无，1初中， 2中专/高中，3大专，4本科，5硕士及以上;默认2  |integer  |    |
|id_no| 身份证号码  |string  |    |
|job_objective| 求职意向：填写 默认 岗位不限  |string  |    |
|major| 专业技能  |string  |    |
|phone| 注册手机号/登录凭证  |string  |    |
|sex| 性别：1男，2女;默认1  |integer  |    |
|user_id| 用户主键  |integer  |    |


**响应状态码说明**:

| 状态码         | 说明                             |    schema                         |
| ------------ | -------------------------------- |---------------------- |
| 200 | OK  |UserResume对象|
                | 401 | Unauthorized  ||
                | 403 | Forbidden  ||
                | 404 | Not Found  ||
                

        
    





            