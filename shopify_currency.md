# Catlog

|*Api Name*|*Api Url*|*Api Version*|*Developer*|*Remarks*|
|---|---|---|---|---|
|[queryShopInfo](#1)|shopify/app/work/currency/queryShopInfo|1.0|liao panpan||
|[queryAllCurrencies](#2)|shopify/app/work/currency/queryAllCurrencies |1.0|liao panpan||
|[queryShopConfiguration](#3)|shopify/app/work/currency/queryShopConfiguration |1.0|liao panpan||
|[saveShopConfiguration](#4)|shopify/app/work/currency/saveShopConfiguration |1.0|liao panpan||
|[exchangeRate](#5)|shopify/app/work/currency/exchangeRate |1.0|liao panpan||
|[exchangeRate](#6)|shopify/app/work/currency/saveComplaint |1.0|liao panpan||




<a name="1">queryShopInfo</a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/currency/queryShopInfo|
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


<a name="2"> queryAllCurrencies </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/currency/queryAllCurrencies|
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
|3.1|currencies|List|货币列表|Y||
|3.1.1|currencyCode|String|货币代码|Y|USD|
|3.1.2|countryCode|String|国家代码|Y|US|

<a name="3"> queryShopConfiguration </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/currency/queryShopConfiguration|
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
|3.1|autoConversion|String|是否自动转换|Y|true/false|
|3.2|selectedCurrencies|List|已选择的货币列表|Y||
|3.2.1|code|String|货币代码|Y|USD|
|3.3|priceConfiguration|Object|价格设置|Y||
|3.3.1|decimalRounding|String|小数四舍五入设置|Y|参考DecimalRounding数据字典|
|3.3.2|currencyFormat|String|币种样式设置|Y|参考CurrencyFormat数据字典|
|3.3.3|customRoundingValue|String|自定义rounding|N| decimalRounding =04时有|
|3.4| cartPageNotification |Object|购物车页面提醒|Y||
|3.4.1| enabled |String|开关|Y|true/false|
|3.4.2| content |String|提醒内容|Y||
|3.5| currencyBarDesign |Object|币种选择框样式设置|Y||
|3.5.1| currencyBarLayout |String|币种选择框样式|Y|见CurrencyBarLayout数据字典|
|3.5.2| background |String|背景色值|Y|#ff6600|
|3.5.3| hoverColor |String|悬停色值|Y|#ff6600|
|3.5.4| textColor |String|文本色值|Y|#ff6600|
|3.5.5| font |String|字体|Y|字体的值，字体列表前端写在代码里，后端不提供|
|3.5.6| shadowDisplay |String|是否显示阴影|Y|true/false|
|3.6| deviceSetting |Object|设备样式设置|Y||
|3.6.1| desktopPlacement |String|货币选择器在电脑上的位置|Y|见Placement数据字典|
|3.6.2| mobilePlacement |String|货币选择器在手机上的位置|Y|见Placement数据字典|
|3.6.3| desktopPadding |String|货币选择器在电脑上的padding|Y|按css规则|
|3.6.4| mobilePadding |String|货币选择器在手机上的padding|Y|按css规则|
|3.6.5| showStyle |String|货币选择器显示样式|Y|见ShowStyle数据字典|

<a name="3"> saveShopConfiguration </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/currency/saveShopConfiguration |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|3.1|autoConversion|String|是否自动转换|Y|true/false|
|3.2|selectedCurrencies|List|已选择的货币列表|Y||
|3.2.1|code|String|货币代码|Y|USD|
|3.3|priceConfiguration|Object|价格设置|Y||
|3.3.1|decimalRounding|String|小数四舍五入设置|Y|参考DecimalRounding数据字典|
|3.3.2|currencyFormat|String|币种样式设置|Y|参考CurrencyFormat数据字典|
|3.3.3|customRoundingValue|String|自定义rounding|N| decimalRounding =04时有|
|3.4| cartPageNotification |Object|购物车页面提醒|Y||
|3.4.1| enabled |String|开关|Y|true/false|
|3.4.2| content |String|提醒内容|Y||
|3.5| currencyBarDesign |Object|币种选择框样式设置|Y||
|3.5.1| currencyBarLayout |String|币种选择框样式|Y|见CurrencyBarLayout数据字典|
|3.5.2| background |String|背景色值|Y|#ff6600|
|3.5.3| hoverColor |String|悬停色值|Y|#ff6600|
|3.5.4| textColor |String|文本色值|Y|#ff6600|
|3.5.5| font |String|字体|Y|字体的值，字体列表前端写在代码里，后端不提供|
|3.5.6| shadowDisplay |String|是否显示阴影|Y|true/false|
|3.6| deviceSetting |Object|设备样式设置|Y||
|3.6.1| desktopPlacement |String|货币选择器在电脑上的位置|Y|见Placement数据字典|
|3.6.2| mobilePlacement |String|货币选择器在手机上的位置|Y|见Placement数据字典|
|3.6.3| desktopPadding |String|货币选择器在电脑上的padding|Y|按css规则|
|3.6.4| mobilePadding |String|货币选择器在手机上的padding|Y|按css规则|
|3.6.5| showStyle |String|货币选择器显示样式|Y|见ShowStyle数据字典|

**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||


<a name="5"> exchangeRate </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/currency/exchangeRate |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|amountList|List|金额列表|Y||
|1.1| sourceAmount |String|源金额|Y||
|2|sourceCurrency|String|源币种|Y||
|3|targetCurrency|String|目标币种|Y||
|4|domain|String|店铺域名:lapsdoor.myshopify.com|Y||



**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||
|3.1|amountList|List|金额列表|Y||
|3.1.1|sourceAmount|String|源金额|Y||
|3.1.2|targetAmount|String|汇率换算后的金额|Y||
|3.2|sourceCurrency|String|源币种|Y||
|3.3|targetCurrency|String|目标币种|Y||


<a name="6"> saveComplaint </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/currency/saveComplaint |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|score|String|分数1-5|Y||
|2| content |String|评论内容|Y||
|3|email|String|联系邮箱|Y||



**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||


## 数据字典

| 字典类型 | 值   | 备注 |
|---|---|---|
| DecimalRounding |01|Show original|
| DecimalRounding |02|Round up|
| DecimalRounding |03|Round down|
| DecimalRounding |04|Customer Roubding|
| CurrencyFormat |01|Symbol only|
| CurrencyFormat |02|Symbol & Code|
|CurrencyBarLayout|01|对应UI上第1种样式|
|CurrencyBarLayout|02|对应UI上第2种样式|
|CurrencyBarLayout|03|对应UI上第3种样式|
|Placement|01|top left|
|Placement|02|top right|
|Placement|03|bottom left|
|Placement|04|bottom right|
|ShowStyle|01|show flag and currency|
|ShowStyle|02|show currency only|
