# Catlog

|*Api Name*|*Api Url*|*Api Version*|*Developer*|*Remarks*|
|---|---|---|---|---|
|[queryShopInfo](#1)|shopify/app/work/reviews/sshop/query|1.0|liao panpan||
|[logout](#2)|shopify/app/work/reviews/logout |1.0|liao panpan||
|[queryEmailCfg](#3)|shopify/app/work/reviews/emailCfg/query |1.0|liao panpan||
|[saveEmailCfg](#4)|shopify/app/work/reviews/emailCfg/save |1.0|liao panpan||
|[queryEmailTemplate](#5)|shopify/app/work/reviews/emailTemplate/query |1.0|liao panpan||
|[saveEmailTemplate](#6)|shopify/app/work/reviews/emailTemplate/save |1.0|liao panpan||
|[queryBalcklist](#7)|shopify/app/work/reviews/balcklist/query |1.0|liao panpan||
|[saveBalcklist](#8)|shopify/app/work/reviews/balcklist/save |1.0|liao panpan||
|[queryEmailHistory](#9)|shopify/app/work/reviews/emailHistory/query |1.0|liao panpan||
|[queryDiscountCfg](#10)|shopify/app/work/reviews/discount/query |1.0|liao panpan||
|[saveDiscountCfg](#11)|shopify/app/work/reviews/discount/save |1.0|liao panpan||
|[queryReviews](#12)|shopify/app/work/reviews/query |1.0|liao panpan||
|[queryReviews](#13)|shopify/app/portal/reviews/query |1.0|liao panpan||
|[addReviews](#14)|shopify/app/portal/reviews/add |1.0|liao panpan||
|[approveReviews](#15)|shopify/app/work/reviews/approve |1.0|liao panpan||
|[deleteReviews](#16)|shopify/app/work/reviews/delete |1.0|liao panpan||
|[editReviews](#17)|shopify/app/work/reviews/edit |1.0|liao panpan||
|[pinReviews](#18)|shopify/app/work/reviews/pin |1.0|liao panpan||



# <a name="1">queryShopInfo</a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/queryShopInfo|
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|||||||

**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||
|3.1|<a href="https://shopify.dev/docs/admin-api/rest/reference/store-properties/shop">详见shopify官方文档</a>|String||Y|<a href="https://shopify.dev/docs/admin-api/rest/reference/store-properties/shop">shop</a>|

<a name="2"> logout </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/logout |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1||||Y||



**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||

<a name="3"> queryEmailCfg </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/emailCfg/query |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1||||Y||



**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||
|3.1|enabled|String|开关|Y|false/true|
|3.2|timingDomestic|String|国内多少天后发送|Y||
|3.3|timingConditionDomestic|String|国内timing条件|Y|timing条件，01:pruchase,02:fulfillment,03:delivery|
|3.4|timingInternational|String|国际多少天后发送|Y||
|3.5|timingConditionInternational|String|国际timing条件|Y|timing条件，01:pruchase,02:fulfillment,03:delivery|
|3.6|reminderTimes|String|提醒次数|Y||
|3.7|reminderAfterDaysDomestic|String|国内多少天后提醒|Y||
|3.8|reminderAfterDaysInternational|String|国际多少天后提醒|Y||
|3.9|senderName|String|邮箱中的发送人|N||
|3.10|senderEmail|String|发送邮箱|N||

<a name="4"> saveEmailCfg </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/emailCfg/save |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|enabled|String|开关|N|false/true|
|2|timingDomestic|String|国内多少天后发送|N||
|3|timingConditionDomestic|String|国内timing条件|N|timing条件，01:pruchase,02:fulfillment,03:delivery|
|4|timingInternational|String|国际多少天后发送|N||
|5|timingConditionInternational|String|国际timing条件|N|timing条件，01:pruchase,02:fulfillment,03:delivery|
|6|reminderTimes|String|提醒次数|N||
|7|reminderAfterDaysDomestic|String|国内多少天后提醒|N||
|8|reminderAfterDaysInternational|String|国际多少天后提醒|N||
|9|senderName|String|邮箱中的发送人|N||
|10|senderEmail|String|发送邮箱|N||

**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||



<a name="5"> queryEmailTemplate </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/emailTemplate/query |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1||||Y||

**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||
|3.1| templateNo |String|模板编号|Y|第一版本只有1个模板|
|3.2| subject |String|邮件主题|Y||
|3.3| banner |String|banner地址|Y||
|3.4| message |String|邮件内容|Y||
|3.5| footer |String|footer显示的文案|Y||
|3.6| purchaseTitle |String|订单标题|Y||
|3.7| buttonText |String|按钮文本|Y||
|3.8| productCount |String|显示一个订单里面多少个产品|Y|默认1|




<a name="6"> saveEmailTemplate </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/emailTemplate/save |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|3.1| templateNo |String|模板编号|Y|第一版本只有1个模板|
|3.2| subject |String|邮件主题|Y||
|3.3| banner |String|banner地址|Y||
|3.4| message |String|邮件内容|Y||
|3.5| footer |String|footer显示的文案|Y||
|3.6| purchaseTitle |String|订单标题|Y||
|3.7| buttonText |String|按钮文本|Y||
|3.8| productCount |String|显示一个订单里面多少个产品|Y|默认1|


**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||




<a name="7"> queryBalcklist </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/balcklist/query |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1| blacklistType |String|黑名单类型|Y|01:email，02：product,03:mobile number|
|2| pageNum |String|第几页|N|分页参数，从1开始，默认1|
|3| pageSize |String|页大小|N|默认10|

**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||
|3.1| blacklistType |String|黑名单类型|Y|01:email，02：product,03:mobile number|
|3.2| blacklistValue |String|黑名单值|Y||
|3.3| reason |String|加入的原因|N||



<a name="8"> saveBalcklist </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/balcklist/save |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|3.1| blacklistType |String|黑名单类型|Y|01:email，02：product,03:mobile number|
|3.2| blacklistValue |String|黑名单值|Y||
|3.3| reason |String|加入的原因|N||

**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||







<a name="9"> queryEmailHistory </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/emailHistory/query |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|emailSource|String|来源|Y|01：request email，02：reminder|
|2|emailAddress|String|邮箱|N||
|3|buyerName|String|购买人|N||
|4|sendStatus|String|状态|N|01:pending,02:finish,03:expired|
|6| pageNum |String|第几页|N|分页参数，从1开始，默认1|
|7| pageSize |String|页大小|N|默认10|
|8| startDateTime |String|时间开始范围|N|yyyy-mm-dd HH:mm:ss|
|9| endDateTime |String| 时间结束范围 |N|yyyy-mm-dd HH:mm:ss|


**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||
|3.1|emailSource|String|来源|Y|01：request email，02：reminder|
|3.2|emailAddress|String|邮箱|Y||
|3.3|buyerName|String|购买人|Y||
|3.4|sendStatus|String|状态|Y|01:pending,02:finish,03:expired|
|3.5|subject|String|主题|Y||
|3.6|createDate|String|主题|Y|yyyy-mm-dd HH:mm:ss|
|3.7|orderNo|String|订单号|Y||






<a name="10"> queryDiscountCfg </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/discount/query |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1||||Y||


**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||
|3.1|discountType|String|折扣类型|Y|01:百分比，02：固定|
|3.2|discountValue|String|折扣值|Y|百分比/固定金额|
|3.3|minimumRequirementType|String|最低使用要求|Y|01:none，02：minimum amount,03:minimum items|
|3.4|minimumRequirementValue|String|最小金额/最小订单商品数量|Y|amount/items count|
|3.5|usageLimit|String|使用次数限制|Y|默认：1|
|3.6|validity|String|多久后失效|Y|单位：天|






<a name="11"> saveDiscountCfg </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/discount/save |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|discountType|String|折扣类型|Y|01:百分比，02：固定|
|2|discountValue|String|折扣值|Y|百分比/固定金额|
|3|minimumRequirementType|String|最低使用要求|Y|01:none，02：minimum amount,03:minimum items|
|4|minimumRequirementValue|String|最小金额/最小订单商品数量|Y|amount/items count|
|5|usageLimit|String|使用次数限制|Y|默认：1|
|6|validity|String|多久后失效|Y|单位：天|


**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||



<a name="13"> queryReviews </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/query,shopify/app/portal/reviews/query |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|domain|String|店铺域名|N|front store访问时需要传|
|2|productNo|String|产品编号|N||
|3|reviewsSource|String|来源|N|01:storefront,02:email,03:sms,04:self|
|4|reviewStatus|String|状态|N|01:waiting,02:approved,03:rejected|
|5|rating|String|星|N|1-5|
|6| pageNum |String|第几页|N|分页参数，从1开始，默认1|
|7| pageSize |String|页大小|N|默认10|
|8| startDateTime |String|时间开始范围|N|yyyy-mm-dd HH:mm:ss|
|9| endDateTime |String| 时间结束范围 |N|yyyy-mm-dd HH:mm:ss|
|10|withPhoto|String|是否有图片|N|false/true|
|11|customerName|String|客户姓名|N|模糊匹配|
|12|countryCode|String|国家|N||
|13|content|String|内容|N|模糊匹配|
|14|email|String|email|N|模糊匹配|


**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||
|3.1|productNo|String|产品编号|Y||
|3.2|reviewsSource|String|来源|Y|01:storefront,02:email,03:sms,04:self|
|3.3|reviewStatus|String|状态|Y|01:waiting,02:approved,03:rejected|
|3.4|rating|String|星|Y|1-5|
|3.6| createDateTime |String|创建时间|Y|yyyy-mm-dd HH:mm:ss|
|3.8|photos|List|图片url列表|N|数组|
|3.9|customerName|String|客户姓名|Y||
|3.10|countryCode|String|国家|Y||
|3.11|content|String|内容|Y||
|3.12|customerEmail|String|email|Y||
|3.13|idReviewsTab|String|reviewId|Y||






<a name="14"> addReviews </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/add|
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|3.1|productNo|String|产品编号|Y||
|3.2|reviewsSource|String|来源|Y|01:storefront,02:email,03:sms,04:self|
|3.3|reviewStatus|String|状态|Y|01:waiting,02:approved,03:rejected|
|3.4|rating|String|星|Y|1-5|
|3.6| createDateTime |String|创建时间|Y|yyyy-mm-dd HH:mm:ss|
|3.8|photos|List|图片url列表|N|数组|
|3.9|customerName|String|客户姓名|Y||
|3.10|countryCode|String|国家|Y||
|3.11|content|String|内容|Y||
|3.12|customerEmail|String|email|Y||


**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||
|3.1|idReviewsTab|String|reviewId|Y||




<a name="15"> approveReviews </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/approve|
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|3.1|idReviewsTab|String|reviewId|Y||



**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||




<a name="16"> deleteReviews </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/delete|
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|3.1|idReviewsTab|String|reviewId|Y||



**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||







<a name="17"> editReviews </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/edit|
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|rating|String|星|N|1-5|
|2| createDateTime |String|创建时间|N|yyyy-mm-dd HH:mm:ss|
|3|photos|List|图片url列表|N|数组|
|4|countryCode|String|国家|N||
|5|content|String|内容|N||
|6|customerEmail|String|email|N||
|7|idReviewsTab|String|reviewId|N||
|8|customerName|String|客户姓名|N||



**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||




<a name="18"> pinReviews </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/reviews/pin|
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|3.1|idReviewsTab|String|reviewId|Y||



**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||


## 数据字典

| 字典类型 | 值   | 备注 |
|---|---|---|
| ReviewStatus |01| waiting |
| ReviewStatus |02| approved |
| ReviewStatus |03| rejected |
|---|---|---|
| TimingCondition |01| pruchase |
| TimingCondition |02| fulfillment |
| TimingCondition |03| delivery |
|---|---|---|
| BlacklistType |01| email |
| BlacklistType |02| product |
| BlacklistType |03| mobile number|
|---|---|---|
| SendStatus |01| pending |
| SendStatus |02| finish |
| SendStatus |03| expired |
|---|---|---|
| EmailSource |01| request email |
| EmailSource |02| reminder |
|---|---|---|
| ReviewsSource |01| storefront |
| ReviewsSource |02| email |
| ReviewsSource |03| sms |
| ReviewsSource |04| self |
