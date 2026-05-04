1.SELECT Paises.nombre, COUNT(Usuarios.id) AS total_usuarios FROM Usuarios JOIN Paises ON Usuarios.pais_id = Paises.id GROUP BY Paises.nombre;

<img width="920" height="254" alt="image" src="https://github.com/user-attachments/assets/1a2c1c99-c0be-4dc2-b391-fe386d38c7b2" />


2. SELECT Peliculas.titulo, COUNT(PeliculaActor.actor_id) AS total_actores FROM Peliculas JOIN PeliculaActor ON Peliculas.id = PeliculaActor.pelicula_id GROUP BY Peliculas.titulo;
<img width="1165" height="399" alt="image" src="https://github.com/user-attachments/assets/ed970d3b-2554-445e-9b98-441ea3246f5f" />
3. SELECT Peliculas.titulo FROM Peliculas JOIN PeliculaActor ON Peliculas.id = PeliculaActor.pelicula_id GROUP BY Peliculas.titulo HAVING COUNT(PeliculaActor.actor_id) >= 2;
<img width="305" height="183" alt="image" src="https://github.com/user-attachments/assets/8747b196-ef8b-4161-8b07-02db670b07c1" />
4.SELECT strftime('%Y', fecha_registro) AS año, COUNT(*) AS total FROM Usuarios GROUP BY año; 
<img width="857" height="275" alt="image" src="https://github.com/user-attachments/assets/2e3fdecf-106c-402c-9576-05021789698d" />
5.SELECT Paises.nombre, strftime('%Y', Usuarios.fecha_registro) AS año, COUNT(*) AS total FROM Usuarios JOIN Paises ON Usuarios.pais_id = Paises.id GROUP BY Paises.nombre, año;
<img width="940" height="319" alt="image" src="https://github.com/user-attachments/assets/3ac3b396-1436-413b-ba55-253f75650334" />

6. SELECT Actores.nombre, Peliculas.titulo FROM Actores JOIN PeliculaActor ON Actores.id = PeliculaActor.actor_id JOIN Peliculas ON PeliculaActor.pelicula_id = Peliculas.id;
<img width="937" height="524" alt="image" src="https://github.com/user-attachments/assets/fb191a7e-4d4a-4b31-bdad-44e9c1a73ded" />

7 SELECT Actores.nombre FROM Actores JOIN PeliculaActor ON Actores.id = PeliculaActor.actor_id JOIN Peliculas ON PeliculaActor.pelicula_id = Peliculas.id WHERE Peliculas.titulo = 'Los Juegos del Hambre';
<img width="518" height="268" alt="image" src="https://github.com/user-attachments/assets/54b9e32f-129a-4173-a28b-b8c2b915c152" />

8 SELECT Usuarios.nombre, SUM(Reproducciones.minutos_vistos) AS total_minutos FROM Usuarios JOIN Reproducciones ON Usuarios.id = Reproducciones.usuario_id GROUP BY Usuarios.nombre;
<img width="961" height="298" alt="image" src="https://github.com/user-attachments/assets/0ce0dc1b-ca6c-430a-85c8-de7c323cfaec" />

9 SELECT Peliculas.titulo FROM Peliculas LEFT JOIN Reproducciones ON Peliculas.id = Reproducciones.pelicula_id WHERE Reproducciones.id IS NULL;
<img width="963" height="287" alt="image" src="https://github.com/user-attachments/assets/8082ffb4-a3cb-44a2-97bc-a02b3f7e5ff7" />

10. SELECT DISTINCT Actores.nombre FROM Actores JOIN PeliculaActor ON Actores.id = PeliculaActor.actor_id JOIN Peliculas ON PeliculaActor.pelicula_id = Peliculas.id JOIN Reproducciones ON Peliculas.id = Reproducciones.pelicula_id JOIN Usuarios ON Reproducciones.usuario_id = Usuarios.id JOIN Paises ON Usuarios.pais_id = Paises.id WHERE Paises.nombre = 'España';
<img width="221" height="163" alt="image" src="https://github.com/user-attachments/assets/eef1f502-edd2-4022-a883-b9d07bd5f046" />


