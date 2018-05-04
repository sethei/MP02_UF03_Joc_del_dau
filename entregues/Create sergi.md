# Function-pova
Aquest es un fitxer de proves
```
CREATE FUNCTION Mels_quedo
(
	@N_jugador as int, @Punts as int
)
RETURNS bit
AS BEGIN
	DECLARE @Total as int, @Totalrival as int
	SET @Total = (SELECT SUM(punts_anotats)
			FROM Marcador M
			WHERE n_jugador_anota=@N_jugador)
	SET @Totalrival = (SELECT SUM(punts_anotats)
				FROM Marcador M
				WHERE n_jugador_anota!=@N_jugador)
	IF (@Punts>=3)
		BEGIN
			RETURN 1
		END
	ELSE
		BEGIN
			IF (@Punts<3 AND @Totalrival-2>@Total)
				BEGIN
					RETURN 1
				END
			RETURN 0
		END
	RETURN 0
END
```
