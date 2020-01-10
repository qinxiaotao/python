# 1.连接数库
```
db = MySQLdb.connect("localhost","root","nihao","cdn",unix_socket='/tmp/mysql.sock')
```

# 2.查询语句
```
cursor = db.cursor()
    cursor.execute('select sum(size)/1000/1000 from t where d like "u%%%%.n" and time like "%s%%%%"  and c="%s"'%(q,c))
```
    查询语句中最重要的是对百分号的处理.python 将用四个百分号来输出一个原始百分号
     
