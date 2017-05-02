# SQL Server Notes

### Temp Tables
```sql
select 
    au.kcid,
    au.program,
    au.status_code,
    au.start_date,
    au.expire_date
into #auths_2017
from au_master as au
where
    year(au.start_date) = 2017

;

select *
from #auths_2017 as a17
where 
    a17.program in ('3A1','3B1','2X1')

;

drop table #auths_2017;

```
