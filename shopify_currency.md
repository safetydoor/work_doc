# Catlog

|*Api Name*|*Api Url*|*Api Version*|*Developer*|*Remarks*|
|---|---|---|---|---|
|[queryShopInfo](#1)|shopify/app/work/currency/queryShopInfo|1.0|liao panpan||
|[queryAllCurrencies](#2)|shopify/app/work/currency/queryAllCurrencies |1.0|liao panpan||
|[queryShopConfiguration](#3)|shopify/app/work/currency/queryShopConfiguration |1.0|liao panpan||
|[saveShopConfiguration](#4)|shopify/app/work/currency/saveShopConfiguration |1.0|liao panpan||
|[disableShopConfiguration](#9)|shopify/app/work/currency/disableShopConfiguration |1.0|liao panpan||
|[enableShopConfiguration](#10)|shopify/app/work/currency/enableShopConfiguration |1.0|liao panpan||
|[exchangeRate](#5)|shopify/app/portal/currency/exchangeRate |1.0|liao panpan||
|[saveComplaint](#6)|shopify/app/work/currency/saveComplaint |1.0|liao panpan||
|[queryShopConfiguration](#7)|shopify/app/portal/currency/queryShopConfiguration |1.0|liao panpan||
|[logout](#8)|shopify/app/work/currency/logout |1.0|liao panpan||



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
|3.1.2|country|String|国家|N|暂无|
|3.1.3|currency|String|币种全称|Y||
|3.1.4|number|String|币种国际编号|N|部分币种不返回|
|3.1.5|currencySymbol|String|货币符号|N|部分币种不返回|


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
|3.0|enable|String|是否开启|Y|true/false|
|3.1|autoConversion|String|是否自动转换|Y|true/false|
|3.2|selectedCurrencies|List|已选择的货币列表|Y||
|3.2.1|currencyCode|String|货币代码|Y|USD|
|3.2.2|currencySymbol|String|货币符号|N|部分币种不返回|
|3.3|priceConfiguration|Object|价格设置|Y||
|3.3.1|decimalRounding|String|小数四舍五入设置|Y|参考DecimalRounding数据字典|
|3.3.2|currencyFormat|String|币种样式设置|Y|参考CurrencyFormat数据字典|
|3.3.3|customRoundingValue|String|自定义rounding|N| decimalRounding =04时有|
|3.3.4|customCurrencyRoundingValue|List|根据currency自定义rounding|N||
|3.3.4.1|currencyCode|String|币种|N||
|3.3.4.2|rounding|String|rounding的值|N|100，99，0.99等|
|3.4| cartPageNotification |Object|购物车页面提醒|Y||
|3.4.1| enabled |String|开关|Y|true/false|
|3.4.2| content |String|提醒内容|N||
|3.4.3| textColor |String|文本色值|N|#ff6600|
|3.4.4| backgroundColor |String|背景色值|N|#ff6600|
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
|3.7|showAllCurrencies|String|是否显示所有货币|Y|true/false|
|3.8|hideCurrencyBar|String|是否隐藏currency bar|N|true/false|
|3.9|showOriginalPrice|String|是否显示原金额|N|true/false|



<a name="4"> saveShopConfiguration </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/currency/saveShopConfiguration |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|3.0|enable|String|是否开启|Y|true/false|
|3.1|autoConversion|String|是否自动转换|Y|true/false|
|3.2|selectedCurrencies|List|已选择的货币列表|Y||
|3.2.1|currencyCode|String|货币代码|Y|USD|
|3.3|priceConfiguration|Object|价格设置|Y||
|3.3.1|decimalRounding|String|小数四舍五入设置|Y|参考DecimalRounding数据字典|
|3.3.2|currencyFormat|String|币种样式设置|Y|参考CurrencyFormat数据字典|
|3.3.3|customRoundingValue|String|自定义rounding|N| decimalRounding =04时有|
|3.3.4|customCurrencyRoundingValue|List|根据currency自定义rounding|N||
|3.3.4.1|currencyCode|String|币种|N||
|3.3.4.2|rounding|String|rounding的值|N|100，99，0.99等|
|3.4| cartPageNotification |Object|购物车页面提醒|Y||
|3.4.1| enabled |String|开关|Y|true/false|
|3.4.2| content |String|提醒内容|N||
|3.4.3| textColor |String|文本色值|N|#ff6600|
|3.4.4| backgroundColor |String|背景色值|N|#ff6600|
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
|3.7|showAllCurrencies|String|是否显示所有货币|Y|true/false|
|3.8|hideCurrencyBar|String|是否隐藏currency bar|N|true/false|
|3.9|showOriginalPrice|String|是否显示原金额|N|true/false|

**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||

<a name="9"> disableShopConfiguration </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/currency/disableShopConfiguration |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|

**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y||


<a name="10"> enableShopConfiguration </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/currency/enableShopConfiguration |
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|

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
|3.4|targetCurrencySymbol|String|货币符号|N|部分币种不返回|


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
|3|email|String|联系邮箱|N|传则用，不传则取用户邮箱|



**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||



<a name="7"> queryShopConfiguration </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/portal/currency/queryShopConfiguration|
|request method|POST|
|version|1|
|remarks|无|

**Params**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|domain|String|店铺域名:lapsdoor.myshopify.com|Y||

**Response**

| No | Field Name   | Field Type | Field Definition   | Mandatory | Remarks |
|---|---|---|---|---|---|
|1|code|String|返回码|Y|000000表示成功|
|2|msg|String|返回信息|Y||
|3|data|Object|返回数据|Y|enabled=false时不返回|
|3.0|enable|String|是否开启|Y|true/false|
|3.1|autoConversion|String|是否自动转换|Y|true/false|
|3.2|selectedCurrencies|List|已选择的货币列表|Y||
|3.2.1|currencyCode|String|货币代码|Y|USD|
|3.2.2|currencySymbol|String|货币符号|N|部分币种不返回|
|3.3|priceConfiguration|Object|价格设置|Y||
|3.3.1|decimalRounding|String|小数四舍五入设置|Y|参考DecimalRounding数据字典|
|3.3.2|currencyFormat|String|币种样式设置|Y|参考CurrencyFormat数据字典|
|3.3.3|customRoundingValue|String|自定义rounding|N| decimalRounding =04时有|
|3.3.4|customCurrencyRoundingValue|List|根据currency自定义rounding|N||
|3.3.4.1|currencyCode|String|币种|N||
|3.3.4.2|rounding|String|rounding的值|N|100，99，0.99等|
|3.4| cartPageNotification |Object|购物车页面提醒|Y||
|3.4.1| enabled |String|开关|Y|true/false|
|3.4.2| content |String|提醒内容|N||
|3.4.3| textColor |String|文本色值|N|#ff6600|
|3.4.4| backgroundColor |String|背景色值|N|#ff6600|
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
|3.7| ipGeolocation |Object|用户定位信息|N|autoConversion=true时返回|
|3.7.1| country |String|国家|Y||
|3.7.2| countryCode |String|国家编号|Y||
|3.7.3| countryFlag |String|国旗|Y||
|3.7.4| currency |String|币种|Y||
|3.7.5| currencyCode |String|币种编号|Y||
|3.7.6| currencySymbol |String|币种符号|Y||
|3.7.6| currencyRates |String|美元汇率|Y||
|3.8|showAllCurrencies|String|是否显示所有货币|Y|true/false|
|3.9|shopCurrencyCode|String|店铺默认货币|Y|USD|
|3.10|shopCurrencySymbol|String|店铺默认货币符号|Y|$|
|3.11|currencyRateList|Object|汇率列表|Y||
|3.11.1|baseCurrencyCode|String|基准汇率code|Y|EUR|
|3.11.2|baseRate|String|基准汇率|Y|1|
|3.11.3|currencyRates|Array|币种汇率|Y||
|3.11.3.1|currencyCode|String|币种|Y||
|3.11.3.2|rate|String|币种相比于baseCurrencyCode的汇率|Y||
|3.12|hideCurrencyBar|String|是否隐藏currency bar|N|true/false|
|3.13|showOriginalPrice|String|是否显示原金额|N|true/false|

<a name="8"> logout </a>

|*Attr*|*Desc*|
|---|---|
|uri|shopify/app/work/currency/logout |
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

