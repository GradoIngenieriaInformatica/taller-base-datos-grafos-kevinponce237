MATCH (p:Persona)-[:TRABAJA_EN]->(e:Empresa)<-[:TRABAJA_EN]-(empleado)-[:VIVE_EN]->(c:Ciudad)
WITH e, COLLECT(DISTINCT p.nombre) AS personas, COUNT(DISTINCT c) AS ciudades
WHERE ciudades = 1
UNWIND personas AS persona
RETURN persona;
