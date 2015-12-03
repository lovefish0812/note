# SQL 冒號後帶參數
## case → 因字串包含":D"字樣，但不是代表要帶入參數，而只是一般的字串而已，<br/>但SQL誤會無帶入值給此參數，故爆錯．
## errorMsg　→ Not all named parameters have been set
``` java
ArrayList employee = new ArrayList();
Query query=em.createQuery("select u from Role as r left join r.users as u where u.sapid=:sapid and u.pass=:pass and r.roledesc=:roledesc")
query.setString("sapid", user.getSapid());
query.setString("pass", user.getPass());
query.setString("roledesc", role.getRoledesc());            
employee =query.list();
```
