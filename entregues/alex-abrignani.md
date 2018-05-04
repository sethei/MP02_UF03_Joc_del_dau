# hola
Aquesta funcio retorna TRUE si la puntuacio de la tirada és més gran que 3, i sino retorna FALSE.

```
create function dbo.mElsQuedo(@numeroJugador int,@puntuacioTirada int)
returns bit
as begin
	declare @bit as bit
		if @puntuacioTirada >3
			begin
				set @bit=1
			end
		else
			begin
				set @bit=0
			end
	return @bit
end
```
