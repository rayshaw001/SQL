# SQL

select userid,deptid
from tab_users e1     
where      
   (  
    select count(1)     
    from tab_users e2     
    where e2.deptid = e1.deptid and e2.userid>=e1.userid  
   ) <=3 /*这里的数值表示你想取前几名*/  
order by deptid desc; 
