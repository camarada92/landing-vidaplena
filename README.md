# landing-vidaplena
Evaluacion 1 - Frontend

prompts:

Como puedo centrar el texto de la columna central?

/* Ajuste para que el formulario también se vea centrado y equilibrado */
form {
    display: flex;
    flex-direction: column;
    width: 100%;       /* Ocupa el ancho disponible */
    max-width: 500px;  /* Limita el ancho para que no sea gigante */
    margin: 0 auto;    /* Centra el formulario dentro del contenedor */
    gap: 15px;
}

Como puedo aplicarle un efecto hover a mis tarjetas?

.card {
    background: #f4f4f4;
    padding: 1.5rem;
    border-radius: 8px;
    text-align: center;
    flex: 1;
    
    /* Efecto inicial de transición */
    transition: transform 0.3s ease, background-color 0.3s ease, box-shadow 0.3s ease;
}

/* Efecto al pasar el mouse */
.card:hover {
    background-color: #5D4037; /* Cambia a tu color café corporativo */
    color: white;              /* El texto se vuelve blanco para contrastar */
    transform: translateY(-10px); /* La tarjeta sube un poco */
    box-shadow: 0 10px 20px rgba(0,0,0,0.2); /* Sombra para dar efecto de elevación */
    cursor: pointer;
}

Como puedo alinear todas mis tarjetas horizontalmente?

.contenedor-tarjetas {
    display: flex;
    justify-content: space-around;
    gap: 20px;
    width: 100%;
    margin-top: 1.5rem; /* Separación entre el título y las tarjetas */
}

Quiero agregarle imagenes al lado de los testimonios, como puedo hacer para que la imagen tenga forma circular y a continuacion aparezca el testimonio?

<!-- TESTIMONIOS -->
<section id="testimonios" class="Testimonios">
    <h2>Lo que dicen nuestros clientes</h2>
    
    <article class="testimonial">
        <img src="img/cliente1.jpg" alt="María G." class="foto-testimonio">
        <div class="texto-testimonio">
            <p>"Excelente servicio. Me ayudaron a encontrar el equilibrio que necesitaba."</p>
            <cite>- María G.</cite>
        </div>
    </article>

    <article class="testimonial">
        <img src="img/cliente2.jpg" alt="Juan P." class="foto-testimonio">
        <div class="texto-testimonio">
            <p>"El equipo es muy profesional y comprensivo. Recomiendo sus servicios."</p>
            <cite>- Juan P.</cite>
        </div>
    </article>
</section>

/* Contenedor del testimonio para alinear imagen y texto */
.testimonial {
    display: flex; /* Alinea imagen y texto horizontalmente */
    align-items: center; /* Centra verticalmente */
    gap: 20px; /* Espacio entre la foto y el texto */
    margin: 20px 0;
    text-align: left; /* Alineamos a la izquierda dentro del bloque central */
}

/* Estilo de la imagen circular */
.foto-testimonio {
    width: 80px; /* Tamaño de la foto */
    height: 80px;
    border-radius: 50%; /* Esto crea el círculo perfecto */
    object-fit: cover; /* Evita que la imagen se deforme */
    border: 3px solid #5D4037; /* Borde café para combinar con el estilo */
}

/* Opcional: Para que el bloque central no se vea desalineado */
.Testimonios {
    display: flex;
    flex-direction: column;
    align-items: flex-start; /* Alinea los testimonios al inicio del contenedor */
    width: 100%;
}