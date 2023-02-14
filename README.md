---
title: material-test v1.0.0
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
code_clipboard: true
highlight_theme: darkula
headingLevel: 2
generator: "@tarslib/widdershins v4.0.15"


---

#### 框架

springboot2.5

mybatisplus

lombok

#### 开发工具

idea

#### 环境

jdk11

maven3.6

git

# 材料

DDL

```sql
CREATE TABLE `t_goods_material` (
  `id` varchar(50) CHARACTER SET utf8mb4 COLLATE utf8mb4_bin NOT NULL COMMENT '主键',
  `material_name` varchar(50) CHARACTER SET utf8mb4 COLLATE utf8mb4_bin DEFAULT NULL COMMENT '材料名称',
  `material_code` varchar(50) CHARACTER SET utf8mb4 COLLATE utf8mb4_bin DEFAULT NULL COMMENT '材料编码',
  `stock_num` int DEFAULT NULL COMMENT '库存数量',
  `unit_value` char(2) CHARACTER SET utf8mb4 COLLATE utf8mb4_bin DEFAULT NULL COMMENT '单位(1-张，2-盒，3-条，4-卷)',
  `remark` varchar(500) CHARACTER SET utf8mb4 COLLATE utf8mb4_bin DEFAULT NULL COMMENT '备注',
  `create_user_id` varchar(50) CHARACTER SET utf8mb4 COLLATE utf8mb4_bin DEFAULT NULL COMMENT '创建人',
  `create_time` datetime DEFAULT NULL COMMENT '创建时间',
  `update_user_id` varchar(50) CHARACTER SET utf8mb4 COLLATE utf8mb4_bin DEFAULT NULL COMMENT '更新人',
  `update_time` datetime DEFAULT NULL COMMENT '更新时间',
  `tenant_id` varchar(50) CHARACTER SET utf8mb4 COLLATE utf8mb4_bin DEFAULT NULL COMMENT '租户id',
  `request_id` varchar(50) CHARACTER SET utf8mb4 COLLATE utf8mb4_bin DEFAULT NULL,
  `del_flag` tinyint(1) DEFAULT NULL,
  PRIMARY KEY (`id`) USING BTREE
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_bin ROW_FORMAT=DYNAMIC COMMENT='材料管理表';
```



> v1.0.0

# 材料管理

<a id="opIdgetAllMaterialUsingGET"></a>

## GET 查询材料

GET /materialList

按条件模糊查询材料

### 请求参数

| 名称                 | 位置  | 类型    | 必选 | 说明 |
| -------------------- | ----- | ------- | ---- | ---- |
| certMaterialCode     | query | string  | 否   | none |
| certMaterialName     | query | string  | 否   | none |
| certMaterialStockNum | query | integer | 否   | none |
| certMaterialUnit     | query | string  | 否   | none |
| certMaterialUnitName | query | string  | 否   | none |
| configTime           | query | string  | 否   | none |
| createTime           | query | string  | 否   | none |
| createUserId         | query | string  | 否   | none |
| dataScope            | query | string  | 否   | none |
| delFlag              | query | string  | 否   | none |
| id                   | query | string  | 是   | none |
| num                  | query | integer | 否   | none |
| params               | query | string  | 否   | none |
| projectId            | query | string  | 否   | none |
| remark               | query | string  | 否   | none |
| requestId            | query | string  | 否   | none |
| templateMaterialId   | query | string  | 否   | none |
| tenantId             | query | string  | 否   | none |
| updateTime           | query | string  | 否   | none |
| updateUserId         | query | string  | 否   | none |

> 返回示例

### 返回结果

| 状态码 | 状态码含义                                                   | 说明         | 数据模型                              |
| ------ | ------------------------------------------------------------ | ------------ | ------------------------------------- |
| 200    | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)      | OK           | [TableDataInfo](#schematabledatainfo) |
| 401    | [Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1) | Unauthorized | Inline                                |
| 403    | [Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3) | Forbidden    | Inline                                |
| 404    | [Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4) | Not Found    | Inline                                |

### 返回数据结构

<a id="opIddelMaterialUsingGET"></a>

## DELETE 删除材料

DELETE /delMaterial

按条件模糊查询材料

### 请求参数

| 名称                 | 位置  | 类型    | 必选 | 说明 |
| -------------------- | ----- | ------- | ---- | ---- |
| certMaterialCode     | query | string  | 否   | none |
| certMaterialName     | query | string  | 否   | none |
| certMaterialStockNum | query | integer | 否   | none |
| certMaterialUnit     | query | string  | 否   | none |
| certMaterialUnitName | query | string  | 否   | none |
| configTime           | query | string  | 否   | none |
| createTime           | query | string  | 否   | none |
| createUserId         | query | string  | 否   | none |
| dataScope            | query | string  | 否   | none |
| delFlag              | query | string  | 否   | none |
| id                   | query | string  | 否   | none |
| num                  | query | integer | 否   | none |
| params               | query | string  | 否   | none |
| projectId            | query | string  | 否   | none |
| remark               | query | string  | 否   | none |
| requestId            | query | string  | 否   | none |
| templateMaterialId   | query | string  | 否   | none |
| tenantId             | query | string  | 否   | none |
| updateTime           | query | string  | 否   | none |
| updateUserId         | query | string  | 否   | none |

> 返回示例

### 返回结果

| 状态码 | 状态码含义                                                   | 说明         | 数据模型 |
| ------ | ------------------------------------------------------------ | ------------ | -------- |
| 200    | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)      | OK           | Inline   |
| 401    | [Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1) | Unauthorized | Inline   |
| 403    | [Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3) | Forbidden    | Inline   |
| 404    | [Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4) | Not Found    | Inline   |

### 返回数据结构

状态码 **200**

| 名称                       | 类型   | 必选  | 约束 | 中文名 | 说明 |
| -------------------------- | ------ | ----- | ---- | ------ | ---- |
| » **additionalProperties** | object | false | none |        | none |

## GET 查询全部材料

GET /getMaterialList

查询全部材料

> 返回示例

### 返回结果

| 状态码 | 状态码含义                                                   | 说明         | 数据模型 |
| ------ | ------------------------------------------------------------ | ------------ | -------- |
| 200    | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)      | OK           | Inline   |
| 401    | [Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1) | Unauthorized | Inline   |
| 403    | [Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3) | Forbidden    | Inline   |
| 404    | [Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4) | Not Found    | Inline   |

### 返回数据结构

状态码 **200**

| 名称                    | 类型                          | 必选  | 约束 | 中文名   | 说明 |
| ----------------------- | ----------------------------- | ----- | ---- | -------- | ---- |
| *anonymous*             | [[Material](#schemamaterial)] | false | none |          | none |
| » Material              | [Material](#schemamaterial)   | false | none | Material | none |
| »» certMaterialCode     | string                        | false | none |          | none |
| »» certMaterialName     | string                        | false | none |          | none |
| »» certMaterialStockNum | integer(int32)                | false | none |          | none |
| »» certMaterialUnit     | string                        | false | none |          | none |
| »» certMaterialUnitName | string                        | false | none |          | none |
| »» configTime           | string(date-time)             | false | none |          | none |
| »» createTime           | string(date-time)             | false | none |          | none |
| »» createUserId         | string                        | false | none |          | none |
| »» dataScope            | string                        | false | none |          | none |
| »» delFlag              | boolean                       | false | none |          | none |
| »» id                   | string                        | false | none |          | none |
| »» num                  | integer(int32)                | false | none |          | none |
| »» params               | object                        | false | none |          | none |
| »» projectId            | string                        | false | none |          | none |
| »» remark               | string                        | false | none |          | none |
| »» requestId            | string                        | false | none |          | none |
| »» templateMaterialId   | string                        | false | none |          | none |
| »» tenantId             | string                        | false | none |          | none |
| »» updateTime           | string(date-time)             | false | none |          | none |
| »» updateUserId         | string                        | false | none |          | none |

<a id="opIdaddMaterialUsingGET"></a>

## POST 编辑材料

POST /updateMaterial

编辑材料

### 请求参数

| 名称                 | 位置  | 类型    | 必选 | 说明 |
| -------------------- | ----- | ------- | ---- | ---- |
| certMaterialCode     | query | string  | 否   | none |
| certMaterialName     | query | string  | 否   | none |
| certMaterialStockNum | query | integer | 否   | none |
| certMaterialUnit     | query | string  | 否   | none |
| certMaterialUnitName | query | string  | 否   | none |
| configTime           | query | string  | 否   | none |
| createTime           | query | string  | 否   | none |
| createUserId         | query | string  | 否   | none |
| dataScope            | query | string  | 否   | none |
| delFlag              | query | string  | 否   | none |
| id                   | query | string  | 否   | none |
| num                  | query | integer | 否   | none |
| params               | query | string  | 否   | none |
| projectId            | query | string  | 否   | none |
| remark               | query | string  | 否   | none |
| requestId            | query | string  | 否   | none |
| templateMaterialId   | query | string  | 否   | none |
| tenantId             | query | string  | 否   | none |
| updateTime           | query | string  | 否   | none |
| updateUserId         | query | string  | 否   | none |

> 返回示例

### 返回结果

| 状态码 | 状态码含义                                                   | 说明         | 数据模型 |
| ------ | ------------------------------------------------------------ | ------------ | -------- |
| 200    | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)      | OK           | Inline   |
| 401    | [Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1) | Unauthorized | Inline   |
| 403    | [Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3) | Forbidden    | Inline   |
| 404    | [Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4) | Not Found    | Inline   |

### 返回数据结构

状态码 **200**

| 名称         | 类型   | 必选  | 约束 | 中文名 | 说明 |
| ------------ | ------ | ----- | ---- | ------ | ---- |
| » **Result** | object | false | none |        | none |



<a id="opIdaddMaterialUsingGET"></a>

## POST 新增材料

POST /createMaterial

编辑材料

### 请求参数

| 名称                 | 位置  | 类型    | 必选 | 说明 |
| -------------------- | ----- | ------- | ---- | ---- |
| certMaterialCode     | query | string  | 否   | none |
| certMaterialName     | query | string  | 否   | none |
| certMaterialStockNum | query | integer | 否   | none |
| certMaterialUnit     | query | string  | 否   | none |
| certMaterialUnitName | query | string  | 否   | none |
| configTime           | query | string  | 否   | none |
| createTime           | query | string  | 否   | none |
| createUserId         | query | string  | 否   | none |
| dataScope            | query | string  | 否   | none |
| delFlag              | query | string  | 否   | none |
| id                   | query | string  | 否   | none |
| num                  | query | integer | 否   | none |
| params               | query | string  | 否   | none |
| projectId            | query | string  | 否   | none |
| remark               | query | string  | 否   | none |
| requestId            | query | string  | 否   | none |
| templateMaterialId   | query | string  | 否   | none |
| tenantId             | query | string  | 否   | none |
| updateTime           | query | string  | 否   | none |
| updateUserId         | query | string  | 否   | none |

> 返回示例

### 返回结果

| 状态码 | 状态码含义                                                   | 说明         | 数据模型 |
| ------ | ------------------------------------------------------------ | ------------ | -------- |
| 200    | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)      | OK           | Inline   |
| 401    | [Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1) | Unauthorized | Inline   |
| 403    | [Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3) | Forbidden    | Inline   |
| 404    | [Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4) | Not Found    | Inline   |

### 返回数据结构

状态码 **200**

| 名称         | 类型   | 必选  | 约束 | 中文名 | 说明 |
| ------------ | ------ | ----- | ---- | ------ | ---- |
| » **Result** | object | false | none |        | none |

# 

# 数据模型

<h2 id="tocS_Material">Material</h2>

<a id="schemamaterial"></a>
<a id="schema_Material"></a>
<a id="tocSmaterial"></a>
<a id="tocsmaterial"></a>

```json
{
  "certMaterialCode": "string",
  "certMaterialName": "string",
  "certMaterialStockNum": 0,
  "certMaterialUnit": "string",
  "certMaterialUnitName": "string",
  "configTime": "2019-08-24T14:15:22Z",
  "createTime": "2019-08-24T14:15:22Z",
  "createUserId": "string",
  "dataScope": "string",
  "delFlag": true,
  "id": "string",
  "num": 0,
  "params": {},
  "projectId": "string",
  "remark": "string",
  "requestId": "string",
  "templateMaterialId": "string",
  "tenantId": "string",
  "updateTime": "2019-08-24T14:15:22Z",
  "updateUserId": "string"
}

```

Material

### 属性

| 名称                 | 类型              | 必选  | 约束 | 中文名 | 说明 |
| -------------------- | ----------------- | ----- | ---- | ------ | ---- |
| certMaterialCode     | string            | false | none |        | none |
| certMaterialName     | string            | false | none |        | none |
| certMaterialStockNum | integer(int32)    | false | none |        | none |
| certMaterialUnit     | string            | false | none |        | none |
| certMaterialUnitName | string            | false | none |        | none |
| configTime           | string(date-time) | false | none |        | none |
| createTime           | string(date-time) | false | none |        | none |
| createUserId         | string            | false | none |        | none |
| dataScope            | string            | false | none |        | none |
| delFlag              | boolean           | false | none |        | none |
| id                   | string            | false | none |        | none |
| num                  | integer(int32)    | false | none |        | none |
| params               | object            | false | none |        | none |
| projectId            | string            | false | none |        | none |
| remark               | string            | false | none |        | none |
| requestId            | string            | false | none |        | non  |
| tenantId             | string            | false | none |        | none |
| updateTime           | string(date-time) | false | none |        | none |
| updateUserId         | string            | false | none |        | none |
|                      |                   |       |      |        |      |

<h2 id="tocS_TableDataInfo">TableDataInfo</h2>

<a id="schematabledatainfo"></a>
<a id="schema_TableDataInfo"></a>
<a id="tocStabledatainfo"></a>
<a id="tocstabledatainfo"></a>

```json
{
  "code": 0,
  "msg": "string",
  "rows": [
    {}
  ],
  "total": 0
}

```

TableDataInfo

### 属性

| 名称  | 类型           | 必选  | 约束 | 中文名 | 说明 |
| ----- | -------------- | ----- | ---- | ------ | ---- |
| code  | integer(int32) | false | none |        | none |
| msg   | string         | false | none |        | none |
| rows  | [object]       | false | none |        | none |
| total | integer(int64) | false | none |        | none |

## 通用返回结果

```
{
  "code": 0,
  "msg": "string",
}

```

