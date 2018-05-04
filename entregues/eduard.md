#Jocs de daus
Hem quedo els punts a partir de igual o més gran de 3.
```
create function meLoquedo(@jugador as int, @punts as int)
returns bit
as begin
        declare @quedat as bit;
        if @punts>=3
                set @quedat=1;
        else
                set @quedat=0;
        return @quedat
end
```
