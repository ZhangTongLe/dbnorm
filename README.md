# dbnorm
一个通用的数据库字段设计规范（实体表）

# 字符编码
- 数据库、数据表、字段编码全部应为utf-8。

# 数据表名称（table）
- 以英文单词命名，全部小写。多个英文单词以下划线间隔。
- 不要使用单词复数，也不要使用数字，除下划线外不要使用其他特殊字符。
- 尽量不要使用英文缩写，ip/url等常见的除外。

# 字段名称（name）
- 以英文单词命名，全部使用小写英文字母，多个英文单词以下划线间隔。
- 不要使用单词复数，也不要使用数字，除下划线外不要使用其他特殊字符。
- 尽量不要使用英文缩写，ip/url等常见的除外。
- 数据表中建议含有id字段，string类型，128长度，主键。
- 数据表中建议含有insert_timestamp/update_timestamp字段，timestamp类型。
- 外键或引用外部数据表的字段时，命名方式为：外部数据表名+下划线+外部字段名，如：user_id/order_price。

# 字段类型（type）
- integer 整数型
- decimal 小数型
- string 字符串
- text 文本
- timestamp 时间戳

# 字段长度（size）
- 数字型字段1-11
- 字符串型字段1-1024

# 禁止空值
- 除text类型、timestamp类型字段外，其他类型字段禁止null值，需设置为not null。

# 字段默认值（default）
- 数字型字段默认为：0
- 字符型字段默认为：''
- 时间型字段默认为：null

# 字段备注（comment）
- 除主键id外，其他字段建议添加中文备注。

# 禁止无符号数（unsigned）
- 整数型字段均为有符号数。

# 小数点后位数（scale）
- 此为小数型字段所特有，小数型字段必须添加。

# 字段排序
- 常用的字段排在前面，不常用的字段排在后面。
