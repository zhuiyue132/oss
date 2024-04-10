

## Claude AI 文件分析当前存在的限制：

1. 官方没有提供文件分析接口，需要将文件转为文本或 json 数据后调用文本补全接口进行统计分析。这样会导致 input tokens 暴增。
	> 按照这种方式调用了几次，花掉了 $9，账号已欠费。

2. output tokens 最大为 4096，可能存在输出不完整的情况。![image-20240409172540772](https://cdn.jsdelivr.net/gh/zhuiyue132/oss/2024-04-09/image-20240409172540772.png)

3. Rate Limit 速率限制。

   截至目前最高级别付费账号的 TPM(tokens per minute)为 40w。![image-20240409174941282](https://cdn.jsdelivr.net/gh/zhuiyue132/oss/2024-04-09/image-20240409174941282.png)

   因为第1 点的原因，单账号的 TPM 和 TPD 无法满足短时间内多次分析文件。

   以下是一个660 条数据的报表使用文本补全接口分析的用量：

   ![image-20240409175535927](https://cdn.jsdelivr.net/gh/zhuiyue132/oss/2024-04-09/image-20240409175535927.png)

4. Usage Limit 用量限制。

   账号存在每月最大消费金额用量的限制，超过限制后需要等下一个自然月开始后，限制重置后才能使用。![image-20240409180139619](https://cdn.jsdelivr.net/gh/zhuiyue132/oss/2024-04-09/image-20240409180139619.png)
