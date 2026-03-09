import numpy as np
import pandas as pd
import pandas as pd

sales_df = pd.read_csv("sales_data.csv")
print(sales)
                       order_id  order_date     product     category  quantity  unit_price  \
0       1001  2024-01-05      Laptop  Electronics       2.0       750.0   
1       1002  2024-01-07  Smartphone  Electronics       1.0       500.0   
2       1003  2024-01-15  Headphones  Accessories       3.0        50.0   
3       1004  2024-02-02      Laptop  Electronics       NaN       750.0   
4       1005  2024-02-05  Desk Chair    Furniture       2.0       120.0   
5       1006  2024-02-18  Smartphone  Electronics       2.0       500.0   
6       1007  2024-03-01     Monitor  Electronics       1.0       300.0   
7       1008  2024-03-03  Headphones  Accessories       4.0        50.0   
8       1009  2024-03-12  Desk Chair    Furniture       1.0         NaN   
9       1010  2024-03-20      Laptop  Electronics       1.0       750.0   
10      1011  2024-04-05     Monitor  Electronics       2.0       300.0   
11      1012  2024-04-10  Smartphone  Electronics       1.0       500.0   
12      1013  2024-04-18  Headphones  Accessories       NaN        50.0   
13      1014  2024-04-25  Desk Chair    Furniture       3.0       120.0   
14      1015  2024-05-02      Laptop  Electronics       2.0       750.0   

    revenue  
0       NaN  
1     500.0  
2     150.0  
3       NaN  
4     240.0  
5    1000.0  
6     300.0  
...
11      NaN  
12    100.0  
13    360.0  
14   1500.0  

sales_df.head(18)

order_id	order_date	product	category	quantity	unit_price	revenue
0	1001	2024-01-05	Laptop	Electronics	2.0	750.0	NaN
1	1002	2024-01-07	Smartphone	Electronics	1.0	500.0	500.0
2	1003	2024-01-15	Headphones	Accessories	3.0	50.0	150.0
3	1004	2024-02-02	Laptop	Electronics	NaN	750.0	NaN
4	1005	2024-02-05	Desk Chair	Furniture	2.0	120.0	240.0
5	1006	2024-02-18	Smartphone	Electronics	2.0	500.0	1000.0
6	1007	2024-03-01	Monitor	Electronics	1.0	300.0	300.0
7	1008	2024-03-03	Headphones	Accessories	4.0	50.0	NaN
8	1009	2024-03-12	Desk Chair	Furniture	1.0	NaN	120.0
9	1010	2024-03-20	Laptop	Electronics	1.0	750.0	750.0
10	1011	2024-04-05	Monitor	Electronics	2.0	300.0	600.0
11	1012	2024-04-10	Smartphone	Electronics	1.0	500.0	NaN
12	1013	2024-04-18	Headphones	Accessories	NaN	50.0	100.0
13	1014	2024-04-25	Desk Chair	Furniture	3.0	120.0	360.0
14	1015	2024-05-02	Laptop	Electronics	2.0	750.0	1500.0

saless =sales_df.fillna(0)
print(saless)

revenue  
0       0.0  
1     500.0  
2     150.0  
3       0.0  
4     240.0  
5    1000.0  
6     300.0  
...
11      0.0  
12    100.0  
13    360.0  
14   1500.0  
Output is truncated. View as a scrollable element or ope

sales_df.info ()
<class 'pandas.DataFrame'>
RangeIndex: 15 entries, 0 to 14
Data columns (total 7 columns):
 #   Column      Non-Null Count  Dtype  
---  ------      --------------  -----  
 0   order_id    15 non-null     int64  
 1   order_date  15 non-null     str    
 2   product     15 non-null     str    
 3   category    15 non-null     str    
 4   quantity    13 non-null     float64
 5   unit_price  14 non-null     float64
 6   revenue     11 non-null     float64
dtypes: float64(3), int64(1), str(3)
memory usage: 972.0 bytes


order_id= sales["order_id"]
print ([order_id])
[0     1001
1     1002
2     1003
3     1004
4     1005
5     1006
6     1007
7     1008
8     1009
9     1010
10    1011
11    1012
12    1013
13    1014
14    1015
Name: order_id, dtype: int64]


order_date = sales["order_date"]
print (order_date)

0     2024-01-05
1     2024-01-07
2     2024-01-15
3     2024-02-02
4     2024-02-05
5     2024-02-18
6     2024-03-01
7     2024-03-03
8     2024-03-12
9     2024-03-20
10    2024-04-05
11    2024-04-10
12    2024-04-18
13    2024-04-25
14    2024-05-02
Name: order_date, dtype: str


product = sales["product"]
print([product])

[0         Laptop
1     Smartphone
2     Headphones
3         Laptop
4     Desk Chair
5     Smartphone
6        Monitor
7     Headphones
8     Desk Chair
9         Laptop
10       Monitor
11    Smartphone
12    Headphones
13    Desk Chair
14        Laptop
Name: product, dtype: str]

category = sales ["category"]
print (category)

0     Electronics
1     Electronics
2     Accessories
3     Electronics
4       Furniture
5     Electronics
6     Electronics
7     Accessories
8       Furniture
9     Electronics
10    Electronics
11    Electronics
12    Accessories
13      Furniture
14    Electronics
Name: category, dtype: str

quantity = sales["quantity"]
print(quantity)

0     2.0
1     1.0
2     3.0
3     NaN
4     2.0
5     2.0
6     1.0
7     4.0
8     1.0
9     1.0
10    2.0
11    1.0
12    NaN
13    3.0
14    2.0
Name: quantity, dtype: float64

unit_price= sales["unit_price"]
print(unit_price)

0     750.0
1     500.0
2      50.0
3     750.0
4     120.0
5     500.0
6     300.0
7      50.0
8       NaN
9     750.0
10    300.0
11    500.0
12     50.0
13    120.0
14    750.0
Name: unit_price, dtype: float64

revenue= sales["revenue"]
print(revenue)
    order_id  order_date     product     category  quantity  unit_price  \
0       1001  2024-01-05      Laptop  Electronics       2.0       750.0   
1       1002  2024-01-07  Smartphone  Electronics       1.0       500.0   
2       1003  2024-01-15  Headphones  Accessories       3.0        50.0   
3       1004  2024-02-02      Laptop  Electronics       NaN       750.0   
4       1005  2024-02-05  Desk Chair    Furniture       2.0       120.0   
5       1006  2024-02-18  Smartphone  Electronics       2.0       500.0   
6       1007  2024-03-01     Monitor  Electronics       1.0       300.0   
7       1008  2024-03-03  Headphones  Accessories       4.0        50.0   
8       1009  2024-03-12  Desk Chair    Furniture       1.0         NaN   
9       1010  2024-03-20      Laptop  Electronics       1.0       750.0   
10      1011  2024-04-05     Monitor  Electronics       2.0       300.0   
11      1012  2024-04-10  Smartphone  Electronics       1.0       500.0   
12      1013  2024-04-18  Headphones  Accessories       NaN        50.0   
13      1014  2024-04-25  Desk Chair    Furniture       3.0       120.0   
14      1015  2024-05-02      Laptop  Electronics       2.0       750.0   

    revenue  
0       NaN  
1     500.0  
2     150.0  
3       NaN  
4     240.0  
5    1000.0  
6     300.0  
...
11      NaN  
12    100.0  
13    360.0  
14   1500.0  
Output is truncated. View as a scrollable element or open in a text editor. Adjust cell output settings...
order_id	order_date	product	category	quantity	unit_price	revenue
0	1001	2024-01-05	Laptop	Electronics	2.0	750.0	NaN
1	1002	2024-01-07	Smartphone	Electronics	1.0	500.0	500.0
2	1003	2024-01-15	Headphones	Accessories	3.0	50.0	150.0
3	1004	2024-02-02	Laptop	Electronics	NaN	750.0	NaN
4	1005	2024-02-05	Desk Chair	Furniture	2.0	120.0	240.0
5	1006	2024-02-18	Smartphone	Electronics	2.0	500.0	1000.0
6	1007	2024-03-01	Monitor	Electronics	1.0	300.0	300.0
7	1008	2024-03-03	Headphones	Accessories	4.0	50.0	NaN
8	1009	2024-03-12	Desk Chair	Furniture	1.0	NaN	120.0
9	1010	2024-03-20	Laptop	Electronics	1.0	750.0	750.0
10	1011	2024-04-05	Monitor	Electronics	2.0	300.0	600.0
11	1012	2024-04-10	Smartphone	Electronics	1.0	500.0	NaN
12	1013	2024-04-18	Headphones	Accessories	NaN	50.0	100.0
13	1014	2024-04-25	Desk Chair	Furniture	3.0	120.0	360.0
14	1015	2024-05-02	Laptop	Electronics	2.0	750.0	1500.0
    order_id  order_date     product     category  quantity  unit_price  \
0       1001  2024-01-05      Laptop  Electronics       2.0       750.0   
1       1002  2024-01-07  Smartphone  Electronics       1.0       500.0   
2       1003  2024-01-15  Headphones  Accessories       3.0        50.0   
3       1004  2024-02-02      Laptop  Electronics       0.0       750.0   
4       1005  2024-02-05  Desk Chair    Furniture       2.0       120.0   
5       1006  2024-02-18  Smartphone  Electronics       2.0       500.0   
6       1007  2024-03-01     Monitor  Electronics       1.0       300.0   
7       1008  2024-03-03  Headphones  Accessories       4.0        50.0   
8       1009  2024-03-12  Desk Chair    Furniture       1.0         0.0   
9       1010  2024-03-20      Laptop  Electronics       1.0       750.0   
10      1011  2024-04-05     Monitor  Electronics       2.0       300.0   
11      1012  2024-04-10  Smartphone  Electronics       1.0       500.0   
12      1013  2024-04-18  Headphones  Accessories       0.0        50.0   
13      1014  2024-04-25  Desk Chair    Furniture       3.0       120.0   
14      1015  2024-05-02      Laptop  Electronics       2.0       750.0   

    revenue  
0       0.0  
1     500.0  
2     150.0  
3       0.0  
4     240.0  
5    1000.0  
6     300.0  
...
11      0.0  
12    100.0  
13    360.0  
14   1500.0  
Output is truncated. View as a scrollable element or open in a text editor. Adjust cell output settings...
<class 'pandas.DataFrame'>
RangeIndex: 15 entries, 0 to 14
Data columns (total 7 columns):
 #   Column      Non-Null Count  Dtype  
---  ------      --------------  -----  
 0   order_id    15 non-null     int64  
 1   order_date  15 non-null     str    
 2   product     15 non-null     str    
 3   category    15 non-null     str    
 4   quantity    13 non-null     float64
 5   unit_price  14 non-null     float64
 6   revenue     11 non-null     float64
dtypes: float64(3), int64(1), str(3)
memory usage: 972.0 bytes
[0     1001
1     1002
2     1003
3     1004
4     1005
5     1006
6     1007
7     1008
8     1009
9     1010
10    1011
11    1012
12    1013
13    1014
14    1015
Name: order_id, dtype: int64]
0     2024-01-05
1     2024-01-07
2     2024-01-15
3     2024-02-02
4     2024-02-05
5     2024-02-18
6     2024-03-01
7     2024-03-03
8     2024-03-12
9     2024-03-20
10    2024-04-05
11    2024-04-10
12    2024-04-18
13    2024-04-25
14    2024-05-02
Name: order_date, dtype: str
[0         Laptop
1     Smartphone
2     Headphones
3         Laptop
4     Desk Chair
5     Smartphone
6        Monitor
7     Headphones
8     Desk Chair
9         Laptop
10       Monitor
11    Smartphone
12    Headphones
13    Desk Chair
14        Laptop
Name: product, dtype: str]
0     Electronics
1     Electronics
2     Accessories
3     Electronics
4       Furniture
5     Electronics
6     Electronics
7     Accessories
8       Furniture
9     Electronics
10    Electronics
11    Electronics
12    Accessories
13      Furniture
14    Electronics
Name: category, dtype: str
0     2.0
1     1.0
2     3.0
3     NaN
4     2.0
5     2.0
6     1.0
7     4.0
8     1.0
9     1.0
10    2.0
11    1.0
12    NaN
13    3.0
14    2.0
Name: quantity, dtype: float64
0     750.0
1     500.0
2      50.0
3     750.0
4     120.0
5     500.0
6     300.0
7      50.0
8       NaN
9     750.0
10    300.0
11    500.0
12     50.0
13    120.0
14    750.0
Name: unit_price, dtype: float64
0        NaN
1      500.0
2      150.0
3        NaN
4      240.0
5     1000.0
6      300.0
7        NaN
8      120.0
9      750.0
10     600.0
11       NaN
12     100.0
13     360.0
14    1500.0
Name: revenue, dtype: float64


sales_df.describe ()

order_id	quantity	unit_price	revenue
count	15.000000	13.000000	14.000000	11.000000
mean	1008.000000	1.923077	392.142857	510.909091
std	4.472136	0.954074	286.011796	433.046292
min	1001.000000	1.000000	50.000000	100.000000
25%	1004.500000	1.000000	120.000000	195.000000
50%	1008.000000	2.000000	400.000000	360.000000
75%	1011.500000	2.000000	687.500000	675.000000
max	1015.000000	4.000000	750.000000	1500.000000


import pandas as pd
import numpy as np
import matplotlib.pyplot as plt


saless.head (16)


order_id	order_date	product	category	quantity	unit_price	revenue
0	1001	2024-01-05	Laptop	Electronics	2.0	750.0	0.0
1	1002	2024-01-07	Smartphone	Electronics	1.0	500.0	500.0
2	1003	2024-01-15	Headphones	Accessories	3.0	50.0	150.0
3	1004	2024-02-02	Laptop	Electronics	0.0	750.0	0.0
4	1005	2024-02-05	Desk Chair	Furniture	2.0	120.0	240.0
5	1006	2024-02-18	Smartphone	Electronics	2.0	500.0	1000.0
6	1007	2024-03-01	Monitor	Electronics	1.0	300.0	300.0
7	1008	2024-03-03	Headphones	Accessories	4.0	50.0	0.0
8	1009	2024-03-12	Desk Chair	Furniture	1.0	0.0	120.0
9	1010	2024-03-20	Laptop	Electronics	1.0	750.0	750.0
10	1011	2024-04-05	Monitor	Electronics	2.0	300.0	600.0
11	1012	2024-04-10	Smartphone	Electronics	1.0	500.0	0.0
12	1013	2024-04-18	Headphones	Accessories	0.0	50.0	100.0
13	1014	2024-04-25	Desk Chair	Furniture	3.0	120.0	360.0
14	1015	2024-05-02	Laptop	Electronics	2.0	750.0	1500.0


x = sales_df["quantity"]
y = sales_df["product"]


plt.bar(x,y)
plt.show()

plt.scatter(x,y)
plt.show()


best_selling = sales_df.groupby("product")["quantity"].sum().sort_values(ascending=False)

print(best_selling)

product
Headphones    7.0
Desk Chair    6.0
Laptop        5.0
Smartphone    4.0
Monitor       3.0
Name: quantity, dtype: float64












