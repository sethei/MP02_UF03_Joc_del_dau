# Bits en el ring. Contienda. Dado.David Ayachi
Ens en demanaven que féssim una funció de si ens quedem el número obtingut o no.Jo el que he fet és si el número obtingut és entre 0 i 3 li donem a la altra persona. En el cas que sigui més gran de 3 mels quedo jo. 
<br>He fet el joc amb si, si el voleu, està adjuntat al meu perfil.
```
CREATE FUNCTION dbo.Melsquedo (@njugador AS INT, 
                               @punts    AS INT) 
returns BIT 
AS 
  BEGIN 
      DECLARE @siono BIT; 

      IF @punts BETWEEN 0 AND 3 
        BEGIN 
            SET @siono=0 
        END; 
      ELSE 
        BEGIN 
            SET @siono=1 
        END; 

      RETURN @siono 
  END; 

go 
```
