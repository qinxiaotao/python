# 1.连接数库
```
db = MySQLdb.connect("localhost","root","nihao","cdn",unix_socket='/tmp/mysql.sock')
```

# 2.查询语句
```
    cursor = db.cursor()
    cursor.execute('select sum(s)/1000/1000 from t where d like "u%%%%.n" and time like "%s%%%%"  and c="%s"'%(q,c))
    data = cursor.fetchone()
```
    查询语句中最重要的是对百分号的处理.在sql语句中将用四个百分号来输出一个原始百分号
 
# 3.insert 语句
```
cursor = db.cursor()
cursor.execute('insert into c(cd,cn,dn,ps) values("%s","%s","uu","%s")'%(c,d,s))
db.commit()
```

# 4关闭语句
```
db.close()
```

     
