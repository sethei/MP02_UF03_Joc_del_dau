# Versió definitiva
La meva funció retorna  un boleà, si no es queda amb els punts retorna un 0, i si es queda els punts retorna un 1.

```

create function mElsQuedo (@num_jugador as int, @punts as int)
returns int
as begin
	declare @donar as bit
	if(@punts <=3)
	begin
		set @donar = 0;
	end
	else
	begin
		set @donar = 1;
	end
	return @donar
end

```
