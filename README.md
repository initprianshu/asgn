# asgn
--Q1
Select count(Snum) from SalesPeople where sname like 'a%' or sname like 'A%'


--Q2
Select snum, sum(amt) from Orders group by Snum having sum(amt) > 2000


--Q3
Select count(*) as SalesPeople_from_NY from SalesPeople where city='New York'


--Q4
Select count(*) as Number_of_SalesPeople, city from SalesPeople group by city having city='London' or city='Paris'


--Q5
 
Select snum, count(*) as Orders_Taken, odate from Orders group by snum, odate


--Q6
Select count(*) as Number_of_SalesPersons, odate from Orders group by odate


--Q7
Select * from Customers where cname like 'G%' and RowNum <2 order by cname
-- RowNum checks for Row number and we need first entry only so we set rownum<2


--Q8
Select * from Orders where (snum, amt) in (select snum, max(amt) from Orders group by snum having snum=1002 or snum=1007)


--Q9


--Q10
select count(*), city, comm from SalesPeople group by city, comm
