Este projeto é uma demonstração prática de como usar media queries no CSS para criar layouts que se adaptam a diferentes tipos de dispositivos, orientações (portrait/landscape), e até para impressão.

Impressão: Estilos específicos para quando o conteúdo for impresso.
Dispositivos diferentes: Adaptar o layout para smartphones, tablets e desktops.
Orientação da tela: Ajustar o design de acordo com a orientação do dispositivo (vertical ou horizontal).


Aqui estão algumas das media queries que foram aplicadas no projeto:

/* Para smartphones */
@media (max-width: 599px) {
    .gallery {
        grid-template-columns: repeat(1, 1fr);
    }
}

/* Para tablets */
@media (min-width: 600px) and (max-width: 1024px) {
    .gallery {
        grid-template-columns: repeat(2, 1fr);
    }
}

/* Para desktops */
@media (min-width: 1025px) {
    .gallery {
        grid-template-columns: repeat(4, 1fr);
    }
}

/* Modo landscape (horizontal) */
@media (orientation: landscape) {
    body {
        background-color: #f0f4f8;
    }
}

/* Modo portrait (vertical) */
@media (orientation: portrait) {
    body {
        background-color: #bcb8d4;
    }
}

/* Estilos para impressão */
@media print {
    header, nav {
        display: none;
    }
    .gallery img {
        width: 50%;
    }

    
}
