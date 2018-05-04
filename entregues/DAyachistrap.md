# Bits en el ring. Contienda. Dado.David Ayachi
Ens en demanaven que féssim una funció de si ens quedem el número obtingut o no.Jo el que he fet és si el número obtingut és entre 0 i 3 li donem a la altra persona. En el cas que sigui més gran de 3 mels quedo jo. 
<br>He fet el joc amb si, si el voleu, està adjuntat al meu perfil.
```
create function dbo.melsquedo (@njugador as int,@punts as int)
returns bit
as begin
	declare @siono bit;
	if @punts between 0 and 3
		begin
		set @siono=0
		end;
	else 
		begin
		set @siono=1
		end;
		return @siono
end;
GO;
```
