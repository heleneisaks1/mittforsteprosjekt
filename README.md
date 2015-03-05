# mittforsteprosjekt


select firstname, lastname
from person 
natural join (
	select filmtype
	from filmitem
	where filmtype like 'cast') 
natural join (
	select parttype
	from filmparticipation
	where parttype like 'C')

where gender like 'F'
group by firstname, lastname
