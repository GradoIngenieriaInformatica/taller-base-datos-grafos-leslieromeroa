MATCH (p:Persona)-[:AMIGO_DE]->(a)
WITH p, count(a) AS totalAmigos
WHERE totalAmigos >= 1
RETURN p.nombre, totalAmigos
