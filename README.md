<!DOCTYPE html>


<!-- Animación SVG: fotógrafo tomando fotos + balón en movimiento -->
<div class="svg-anim" aria-hidden="true" style="display:flex; justify-content:center; margin-top:20px;">
<svg width="320" height="120" viewBox="0 0 320 120" fill="none" xmlns="http://www.w3.org/2000/svg">
<defs>
<linearGradient id="g1" x1="0" x2="1">
<stop offset="0%" stop-color="#ff7f00" />
<stop offset="100%" stop-color="#ffb36b" />
</linearGradient>
</defs>


<!-- fotógrafo: cabeza -->
<circle cx="60" cy="35" r="12" fill="#ffffff" opacity="0.95" />
<!-- cuerpo -->
<rect x="48" y="50" width="24" height="28" rx="6" fill="#ffffff" opacity="0.95" />


<!-- cámara -->
<g class="camera" transform="translate(100,24)">
<rect x="0" y="6" width="70" height="40" rx="6" fill="#111" />
<rect x="6" y="12" width="18" height="12" rx="3" fill="#ff7f00" />
<circle cx="46" cy="26" r="12" fill="#fff" />
<circle cx="46" cy="26" r="7" fill="#111" />
<!-- flash light -->
<rect class="flash" x="74" y="12" width="18" height="20" rx="3" fill="url(#g1)" opacity="0" />
</g>


<!-- balón que se desplaza -->
<g class="ball" transform="translate(240,80)">
<circle cx="0" cy="0" r="10" fill="#ffffff" />
<path d="M-6,-2 L0,0 L-2,5" stroke="#111" stroke-width="1.2" fill="none" />
</g>


<!-- texto de soporte (oculto para accesibilidad) -->
<text x="160" y="112" font-size="11" fill="#aaa" text-anchor="middle">Animación: fotógrafo tomando fotos • CuchoGT</text>
</svg>
</div>


<h2>Sobre mí</h2>
<section class="about animate-section">
Soy un fotógrafo deportivo amante del deporte, capturando emociones, momentos únicos y la pasión que se vive en cada cancha, estadio y escenario deportivo.
</section>


<h2 id="deporte" class="sport-anim">Fotografía Deportiva</h2>
<section class="gallery">
<div class="photo-item"><img src="https://via.placeholder.com/800x600" alt="Deporte 1"></div>
<div class="photo-item"><img src="https://via.placeholder.com/800x600" alt="Deporte 2"></div>
<div class="photo-item"><img src="https://via.placeholder.com/800x600" alt="Deporte 3"></div>
</section>


<h2 id="eventos" class="sport-anim">Eventos (Cumpleaños, Graduaciones, etc.)</h2>
<section class="gallery">
<div class="photo-item"><img src="https://via.placeholder.com/800x600" alt="Evento 1"></div>
<div class="photo-item"><img src="https://via.placeholder.com/800x600" alt="Evento 2"></div>
<div class="photo-item"><img src="https://via.placeholder.com/800x600" alt="Evento 3"></div>
</section>


<a class="whatsapp-btn" href="https://wa.me/50244865199" target="_blank">📱</a>


<footer>
© 2025 CuchoGT — Fotografía Profesional Deportiva y de Eventos
</footer>


<script>
// Activar/desactivar animación en el contenedor para controlar rendimiento
(function(){
const svgWrap = document.querySelector('.svg-anim');
if(!svgWrap) return;
// Añadimos la clase por defecto para que arranque la animación
svgWrap.classList.add('animating');


// alternativa: pulso de cámara más marcado cada vez que el usuario pase el mouse
svgWrap.addEventListener('mouseenter', ()=> svgWrap.classList.add('animating'));
svgWrap.addEventListener('mouseleave', ()=> svgWrap.classList.remove('animating'));


// en móvil activamos animación al tocar
svgWrap.addEventListener('touchstart', ()=> svgWrap.classList.add('animating'));
})();
</script>
</body>
</html>
