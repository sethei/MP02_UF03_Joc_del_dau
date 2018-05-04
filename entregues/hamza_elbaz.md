# Joc
Esta función mira si el número dado es menor que 3 entonces es para él o para mi
```
create function dbo.mElsQuedo (
@n_jugador as int,
@punts as int)
returns integer
as begin
	declare @paraMi int --Si es para mi será 1 (true), sino será 0 (false)
	if @punts<3
		begin
			set @paraMi=0
		end;
	else 
		begin
			set @paraMi=1
		end;
	return @paraMi
end;
```
