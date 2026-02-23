Total Sales = SUM('Sales_Data'[Total Sales])

Total Orders = COUNT('Sales_Data'[Order ID])

Total Quantity = SUM('Sales_Data'[Quantity])

Average Order Value = DIVIDE([Total Sales], [Total Orders])

Total Customers = DISTINCTCOUNT('Sales_Data'[Customer Name])

Net Revenue =
SUMX(
    'Sales_Data',
    'Sales_Data'[Total Sales] -
    ('Sales_Data'[Total Sales] * 'Sales_Data'[Discount %])
)
