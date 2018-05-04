# Prova

Aquesta funció és queda tots aquells numeros que siguin més grans que 2.

```
create function dbo.quedo (@numjugador as int,@punts as int)
returns integer
as begin
	declare @sino int;
	if @punts between 0 and 2
		begin
			set @sino=0
			Print @punts;
			Print ‘no el vull’;
		end;
	else 
		begin
			set @sino=1
			Print @punts;
			Print ‘el vull’;
		end;
	return @sino
end;
```
