MATCH (p:Persona)-[:AMIGO_DE]->(amigo:Persona)-[:PARTICIPA_EN]->(proy:Proyecto)
WITH p, amigo, count(proy) AS cantidadProyectos
WHERE cantidadProyectos > 1
RETURN DISTINCT p.nombre AS Persona
