《Java应用架构设计》源代码示例

[Chapter 9][Section 1][Code 3] - 非循环关系 - 下移
 - 抽离Customer中的getDiscountAmount()方法至独立的calculator.jar，并被Bill调用
 - customer.jar依赖于billing.jar，billing.jar依赖于calculator.jar
 
 
 --------------------------------------------------------------------------
 class - Customer ---------------            module - customer.jar ------
 -----------|1------------------|---------------------------|-----------|--
            |                   |                           |           |
            |                   |                           |           |
            |                   |                           |           |
            |                   |                           |           |
            |                   |                           |           |
 -----------^*------------------|---------------------------^-----------|--
 class - Bill                   |  	         module - billing.jar       |
 -------------------------------|---------------------------|-----------|--
            |                   |                           |           |
            |                   |                           |           |
            |                   |                           |           |
            |                   |                           |           |
            |                   |                           |           |
 -----------^-------------------|---------------------------^-----------|--
 class - DiscountCalculator <----            module - calculator.jar <---
 --------------------------------------------------------------------------