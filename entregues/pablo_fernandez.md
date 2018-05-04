
# VERSIÓ 1.0

Només agafarem els números que siguin majors de 2

```

create function dbo.mElsQuedo( @nJugador int, @punts int ) 
returns bit
as begin
	declare @quedarme as bit
	if @punts <=2
		set @quedarme=0
	else if @punts<=6
		set @quedarme=1
	return @quedarme
end

```
