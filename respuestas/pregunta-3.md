MATCH (p:Persona)-[:ESTUDIO_EN]->(u:Universidad)
RETURN p.nombre AS Persona, u.nombre AS Universidad;
