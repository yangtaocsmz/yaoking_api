
# yaoking门店医生问诊接口
## 登录接口


接口名称: | app用户密码登录
---|---
method:	 | POST
接口地址:	 |https://www.yaoking.cn/openapi/emc_passport/login

### 请求字段：


字段	 | Type | 必传	  | 描述 | 测试值
---|---|---|---|---
uname	 | 	string  |是	|手机号|13992880225
password	 | 	string  |是	|密码|leven123
device_app	 | 	string  |否	|APP机械码 服务器返回存储在缓存中不随注销登录和app自身清除缓存被删除	|
device_mobile	 | 	string  |否	|手机机械码 手机的唯一序列号 苹果uidevice 安卓根据情况取序列	|
mobile_version	 | 	string  |否	|手机版本 如ios 10.1或android 4.3 等|
app_version	 | 	string  |否	|	APP版本 v2.3.0|
### 返回数据

```
{
    "result": "success",
    "msg_code": "0x000",
    "msg": "调用接口成功",
    "time": 1517987660,
    "session": "mobile-366948a1c614bfc956c88af726d638ba",
    "info": {
        "session": "mobile-366948a1c614bfc956c88af726d638ba",
        "member": {
            "id": "342727",
            "yikangcrd_currency": 0,
            "mobile": null,
            "sex": "M",
            "experience": 2880,
            "point": 0,
            "currency": "￥",
            "cur": "CNY",
            "name": "杨志文new",
            "uname": "leven",
            "email": null,
            "headPic": "http://img1.yaoking.cn//dd/19/83/cb885be8c267c13d1c71c508eedc6b6e541.png",
            "advance": "131.24",
            "levelID": "4",
            "levelName": "普通会员",
            "doctorTotal": 0,
            "facTotal": 0,
            "couponTotal": 0,
            "quantityOfOrder": 0,
            "quantityOfMessage": 0,
            "quantityOfCartItems": "",
            "tls_identifier": "64607a50bff3a93fd450ba1c684a5b49"
        },
        "device_info": {
            "device_app": "1802071514202840000342727",
            "flag": "0",
            "msg": "这是一个新设备,欢迎使用"
        }
    }
}
```


---

## 医生列表信息接口


接口名称: | 医生列表信息接口
---|---
method:	 | POST
接口地址:	 |https://www.yaoking.cn/openapi/emc_hospindex/department_find_doctors

### 请求字段：


null
### 返回数据

```
{
    "result": "success",
    "msg_code": "0x000",
    "msg": "调用接口成功",
    "time": 1517981133,
    "session": "mobile-a217e9fc905c5c7b1fde6fedb7b08037",
    "info": {
        "pageInfo": null,
        "doctors": [
            {
                "doc_id": "7",
                "doc_headpic": "http://img1.yaoking.cn//6d/98/c9/0bc1fee05f17a678cc54b4f69d94f2584e8.jpg",
                "doc_name": "王璐",
                "doc_Pharmacist_lv": "执业药师",
                "doc_department": "内科",
                "doc_diagnosis_quantity": null,
                "doc_remark": "药学专业本科毕业，从事医药工作数年，熟悉药品质量管理规范和常见病基本用药情况",
                "doc_impression": [
                    "4",
                    "6",
                    "8"
                ],
                "hosp_id": "1",
                "good_rate": "86.67",
                "hosp_name": "西安莲湖怡康长安康泰医院",
                "doc_impression_arr": [
                    "业内专家",
                    "妙手回春",
                    "对症下药"
                ],
                "doc_online": 2
            },         
        ]
    }
}
```

#### 返回值说明








 字段	| 说明 |
---|---
doc_id	| 医生ID |
doc_headpic | 医生头像|
doc_name | 医生姓名
doc_Pharmacist_lv |医生职业等级
doc_department | 医生科室
doc_remark | 医生简介
good_rate |医生评分
doc_impression_arr | 医生标签















---


## 医生个人资料详情


接口名称: | 医生个人资料详情
---|---
method:	 | POST
接口地址:	 |https://www.yaoking.cn/openapi/emc_hospinner/detail_doctor

### 请求字段：


字段	 | Type | 必传	  | 描述 | 测试值
---|---|---|---|---
doc_id	 | 	string  |是	|医生ID|8
member_id	 | 	string  |是	|用户ID|342727

### 返回数据

```
{
    "result": "success",
    "msg_code": "0x000",
    "msg": "调用接口成功",
    "time": 1517982090,
    "session": "mobile-e68d56b7f71266933d977269adb0928e",
    "info": {
        "doctor_info": {
            "doc_id": "8",
            "doc_headpic": "http://img1.yaoking.cn//f6/6f/23/a6db93d4be521da264c1184963dfb19b12f.jpg",
            "doc_name": "王瑾",
            "doc_Pharmacist_lv": "执业药师",
            "hosp_id": "1",
            "doc_diagnosis_quantity": 449,
            "doc_prescription_quantity": "500",
            "doc_superiority": "西药执业药师，10多年医药行业从业经验，熟悉常见疾病与用药。在疾病预防、用药指导、促进健康等方面提供专业服务，擅长亚健康症状预防治疗。",
            "doc_remark": "西药执业药师，10多年医药行业从业经验，熟悉常见疾病与用药。在疾病预防、用药指导、促进健康等方面提供专业服务，擅长亚健康症状预防治疗。",
            "doc_favorite_quantity": 5,
            "hosp_name": "西安莲湖怡康长安康泰医院",
            "department_name": "内科",
            "good_rate": "86.67",
            "impression": [
                "药到病除",
                "加急问诊",
                "妙手回春",
                "手到病除"
            ],
            "doctor_fee": "",
            "favorite": "1"
        },
        "discuss_list": []
    }
}
```








---

## 查询医生在线状态接口


接口名称: | 查询医生在线状态接口
---|---
method:	 | POST
接口地址:	 |http://doctorpc.yaoking.cn:9555/Services/VisitorService.svc/GetOnlineDoctorList


---
---
---

## 查询问诊人信息接口


接口名称: | 查询问诊人信息接口
---|---
method:	 | POST
接口地址:	 |https://www.yaoking.cn/openapi/emc_hospinner/health_list

### 请求字段：

字段	 | Type | 必传	  | 描述 | 测试值
---|---|---|---|---
session	 | 	string  |是	|从登录接口获取的session值|

### 返回数据

```
{
    "result": "success",
    "msg_code": "0x000",
    "msg": "调用接口成功",
    "time": 1517982834,
    "session": "mobile-a217e9fc905c5c7b1fde6fedb7b08037",
    "info": [
        {
            "health_id": "1195",
            "description": "",
            "patient_name": "郑婧",
            "sex": "2",
            "age": "33",
            "relation": "女",
            "is_default": "0"
        },
        {
            "health_id": "1269",
            "description": "",
            "patient_name": "徐彪",
            "sex": "1",
            "age": "53",
            "relation": "男",
            "is_default": "1"
        }
    ]
}
```

#### 返回值说明








 字段	| 说明 |
---|---
description |病情描述
patient_name | 问诊人姓名
---

## 新增问诊人接口

接口名称: | 新增问诊人接口
---|---
method:	 | POST
接口地址:	 |https://www.yaoking.cn/openapi/emc_hospinner/health_add

### 请求字段：

字段	 | Type | 必传	  | 描述 | 测试值
---|---|---|---|---
session		 | 	string  |是	||36
patient_name		 | 	string  |是	|  患者姓名|邓小小
patient_mobile		 | 	string  |否	|患者手机号|
sex		 | 	string  |是	|性别|1
age		 | 	string  |否	|年龄|88
height	 | 	string  |否	|身高|
weight		 | 	string  |否	|体重|
smoke		 | 	string  |否	|抽烟|
smoke_desc		 | 	string  |否	|抽烟描述|俺抽了一辈子了
drink		 | 	string  |否	|喝酒|1
allergy		 | 	string  |是	|过敏|
id_number		 | 	string  |否	|身份证号|641023698855562543
description		 | 	string  |是	|病情描述|喝酒
relation		 | 	string  |是	|关系|3
is_default		 | 	string  |是	|是否默认|1
casebook_img	 | 	string  |否	|病例图片|111
birthday		 | 	string  |是	|出生年月日|111111


### 返回数据

```
{
    "result": "success",
    "msg_code": "0x000",
    "msg": "调用接口成功",
    "time": 1517989967,
    "session": "36",
    "info": {
        "msg": "保存成功"
    }
}
```


---
## 查询云信账号信息



接口名称: | 查询云信账号信息
---|---
method:	 | POST
接口地址:	 |https://www.yaoking.cn/openapi/emc_hospvideoserver/register

### 请求字段：

字段	 | Type | 必传	  | 描述 | 测试值
---|---|---|---|---
user_id		 | 	string  |是	||1647160
type		 | 	string  |是	|用户为member，医生为doctor|member
name		 | 	string  |否	||王云帆




### 返回数据

```
{
    "result": "success",
    "msg_code": "0x000",
    "msg": "调用接口成功",
    "time": 1517986232,
    "session": "mobile-3acc90aeac1799c3e5bdaa5c66f4445a",
    "info": {
        "desc": "already register",
        "code": 414,
        "token": "9d96a541e09b7d061ea086dcbea46db1",
        "accid": "ykuser_1647160"
    }
}
```

#### 返回值说明


 字段	| 说明 |
---|---
token | 云信注册返回用户token
---

## 请求视频接口



接口名称: | 请求视频接口
---|---
method:	 | POST
接口地址:	 |http://doctorpc.yaoking.cn:9555/Services/VisitorService.svc/RequestVideo

### 请求字段：

字段	 | Type | 必传	  | 描述 | 测试值
---|---|---|---|---
yunxin_accid		 | 	string  |是	|云信用户ID|ykuser_1647160





### 返回数据

```
{"Message":"成功设置医生为正在视频(忙碌)状态！","Status":"success"}
```
---

---
## 处方详情接口



接口名称: | 处方详情接口
---|---
method:	 | POST
接口地址:	 |https://www.yaoking.cn/openapi/emc_hospinner/prescription_detail

### 请求字段：

字段	 | Type | 必传	  | 描述 | 测试值
---|---|---|---|---
prescription_id		 | 	string  |是	|处方ID|2018020613298255
doc_id		 | 	string  |是	|医生ID|15





### 返回数据

```
{
    "result": "success",
    "msg_code": "0x000",
    "msg": "调用接口成功",
    "time": 1518158103,
    "session": "mobile-14230efe98889c420a027e4ea6b4b20f",
    "info": {
        "prescription_record": {
            "prescription_id": "2018020613298255",
            "create_time": "2018-02-06 13:26:43",
            "health_id": "45"
        },
        "doctor_info": {
            "doc_name": "杨恒",
            "doc_Pharmacist_lv": "执业中医师"
        },
        "member_info": {
            "patient_name": "紫铭",
            "sex": "2",
            "birthday": "2000",
            "age": 18
        },
        "prescription_info": {
            "id": "2018020613298255",
            "doctor_id": "15",
            "member_id": "1542205",
            "member_age": "0",
            "member_sex": "0",
            "department": "怡康问诊",
            "health_id": "0",
            "prescription_type": "xiyi",
            "statement": "感冒，发烧",
            "diagnose_result": "发生扁桃体",
            "drugs": null,
            "pharmacist_id": "0",
            "status": "1",
            "open_time": "1517894951",
            "updatetime": "1517894951",
            "remarks": "ABC",
            "prescription_type_txt": "西医",
            "items": [
                {
                    "price": "7.708",
                    "goods_id": "6047",
                    "product_id": "8792",
                    "name": "阿莫西林胶囊  ",
                    "directions": "一日三次",
                    "nums": "2",
                    "approval_no": "国药准字H23020932",
                    "mfrs": "哈尔滨哈药制药总厂",
                    "exp_date": "",
                    "spec": "0.25克*50粒"
                },
                {
                    "price": "20.700",
                    "goods_id": "5882",
                    "product_id": "6548",
                    "name": "感冒清热颗粒",
                    "directions": "",
                    "nums": "3",
                    "approval_no": "国药准字Z45022098",
                    "mfrs": "南宁市维威制药有限公司",
                    "drug_form": "颗粒剂",
                    "exp_date": "",
                    "spec": "12g*15袋"
                }
            ]
        }
    }
}
```




---

## 通过问诊人手机号查询问诊记录



接口名称: | 通过问诊人手机号查询问诊记录
---|---
method:	 | POST
接口地址:	 |https://www.yaoking.cn/openapi/emc_hospinner/prescription_person

### 请求字段：

字段	 | Type | 必传	  | 描述 | 测试值
---|---|---|---|---
mobile		 | 	string  |是	|问诊人手机号|18602994971





### 返回数据

```
{
    "result": "success",
    "msg_code": "0x000",
    "msg": "调用接口成功",
    "time": 1518159683,
    "session": "mobile-e6f076c3e842f8e44524870c8231462f",
    "info": {
        "page_info": null,
        "records": [
            {
                "id": "2123",
                "service_type": "video",
                "prescription_id": "2018020613298255",
                "create_time": "2018-02-06 13:26:43",
                "doctor_id": "15",
                "doctor_info": {
                    "doc_id": "15",
                    "doc_headpic": "http://img1.yaoking.cn//5d/7a/0f/066fd0da7c27795f92eb8b6963dd14c3e67.jpg",
                    "doc_name": "杨恒",
                    "doc_Pharmacist_lv": "执业中医师",
                    "hosp_id": "1",
                    "doc_department": "内科",
                    "doc_remark": "擅长各种慢性病的诊治及干预方案的制定",
                    "hosp_name": "西安莲湖怡康长安康泰医院",
                    "department_name": "内科"
                }
            }
        ]
    }
}
 
```






 



















