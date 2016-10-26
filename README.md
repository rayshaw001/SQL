# SQL
# 各部门收入排名前三的人
select name,deptid
from Employee e1     
where      
   (  
    select count(1)     
    from Employee e2     
    where e2.deptid = e1.deptid and e2.salary>=e1.salary  
   ) <=3 /*这里的数值表示你想取前几名*/  
order by deptid desc; 



SELECT username ,deptid ,sum(deptid) FROM tab_users GROUP BY deptid having sum(deptid)>5
