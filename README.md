Here is my Code that i used in Pizza sales dashboard:
To calculate average pizza sale--> Avg_pizza_per_order = DIVIDE(SUM(pizza_sales[quantity]), DISTINCTCOUNT(pizza_sales[order_id])) 

To calculate average Orders --> avg_order = ROUND(DIVIDE(SUM(pizza_sales[total_price]), DISTINCTCOUNT(pizza_sales[order_id])), 2)

Calculate ranking of pizza--->Rank = if(pizza_sales[ranking] <= 10, [ranking], BLANK())

Calculate ranking of pizza on basis of sales---->ranking = RANKX(all(pizza_sales[pizza_name]), [revenue], ,DESC)

Calculate revenue generated-->revenue = "$"& FORMAT(sum(pizza_sales[total_price]), "#,##0.00")

Calculate total sales of pizza ----> total selling = ROUND(SUM(pizza_sales[quantity]), 0)

week_day_num = WEEKDAY(pizza_sales[order_date], 1)

week_day = FORMAT(pizza_sales[order_date], "dddd")
