# Versió de prova

La funció retorna si t'els quedes o no.

```

create function mElsQuedo (@Num_Jugador as int, @punts as int)
returns bit 
as begin
		declare @quedar as bit;
		-- del 1 al 3 els dones --
		if (@punts <=3)
		begin
			set @quedar = 0;
		end
		-- del 4 al 6 t'el quedes --
		else
		begin
			set @quedar = 1;
		end

		return @quedar
end

```
