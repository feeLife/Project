# Statement

- Backgroud
  * Partner is an important part to reach customers. Help distribute products to the area well. And help reduce investment in setting up a store. The partner who comes as a partnership will receive a profit in many forms, such as operating fees, commission or extra reward when hit the target, with such benefits, there are some partners focus on selling out in large quantities. But low quality of customers for example customer not pay for the invoice, Customers who only use freebies, when they run out, come back to buy again.This type of customer causes the company to lose income.

  * Partner grading s therefore a part that allows to help team to monitor and troubleshoot problem in a time.


- Problem Statement
  * The partner's grade arrangement is a manual operation and relies on data. Now they use unpaid bill in 1 month previous . And is working on Microsoft Excel.
  * The current Commission process cannot be used to determine Commission tier because it is a manual process. Lack of reliability.
  * Evaluation of efficiency and quality of Partner slowness.
  * The company loses revenue from customers that is not quality.

- Business Benefit:
  * Help the team can solve or judge partner that has a risk.
  * Helps company reduce excessive expense.
  * Limited some offer that partner get example reduce giving discount offer to customer, limited quantity of products has allocate to partner

> Cost : expense per partner = 15,000 ฿

>Gain/Loss price = 600฿ * 4 mth = 2,400 ฿ per subs

- Limitation:
  * data churn has a lot of zero value (it's good), make quantile mistake

- The process of making a project
  * backgroup & problem statement
  * query data
  * eda
  * RMF by using value of recency, sales, churn (for basic)
    - but from limitation, will add gridsearch cv to find the best quantile for RFM
  * model
    - classification : to create partner grade/group
    - ARIMA : for predict sales performance (Addon)


- Data Dict

| field | description | Type |
|-------|-------------|------|
| partner_code | staff code all sales channel | string |
| sales_date | date of subscriber start | datetime |
| total | number of new subscriber | int |
| revenue | total of revenue | int |
| churn | total of subscriber leave | int |
