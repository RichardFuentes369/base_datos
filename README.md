# base_datos
-- actualiza un consecutivo, ejemplo id <br><br>
   UPDATE users as a, (SELECT @numeroConsecutivo:= (SELECT max(id) FROM users)) as tabla SET a.id=@numeroConsecutivo:=@numeroConsecutivo+1; <br>
   pongo un id en 0 <br><br>
   UPDATE users as a, (SELECT @numeroConsecutivo:= (SELECT min(id) FROM users)) as tabla SET a.id=@numeroConsecutivo:=@numeroConsecutivo+1; <br><br>
-- actualiza un consecutivo, de llave foránea <br><br>
  UPDATE company AS c, (SELECT @myId:= 0) AS tabla SET c.user_id = @myId := @myId + 1 ; 
