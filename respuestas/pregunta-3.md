MATCH (p:Persona)-[:VIVE_EN]->(c:Ciudad) 
RETURN DISTINCT c.nombre
