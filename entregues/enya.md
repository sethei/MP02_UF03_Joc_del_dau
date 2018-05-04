# AhoraSiQueSi

DadosDaditos
La funcio, retorna, depenent dels punts, un bit, per si el jugador s'els queda o el dona al oponent.

```

go
create function dbo.mElsQuedo(@nJugador int, @punts int)
 returns bit
 as begin
	declare @peraqui as bit
	if(@punts <=3)
	begin
		set @peraqui = 0;
	end
	else
	begin
		set @peraqui = 1;
	end
	return @peraqui
end

```
