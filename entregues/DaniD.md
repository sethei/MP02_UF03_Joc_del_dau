# Bits en el ring. Contienda. Dau. Dani D
Aquesta funció fa que si el número es 4 o 2 no m'el quedo.
<br>
```
CCREATE FUNCTION dbo.mElsQuedo (@nJugador as int,@Dau as int)
returns integer
as BEGIN
	declare @mElQuedo bit;
	if @Dau IN (4,2)
		BEGIN
		SET mElQuedo=0
		END;
	else 
		BEGIN
		SET @mElQuedo=1
		END;
	return @mElQuedo
END;

```
