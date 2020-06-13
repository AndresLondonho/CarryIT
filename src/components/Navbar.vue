
<template>


  <nav class="menu" id="menu"> 
		<div class="contenedor contenedor-botones-menu">
			<button id="btn-menu-barras" class="btn-menu-barras"><i class="fas fa-bars"></i></button>
			<button id="btn-menu-cerrar" class="btn-menu-cerrar"><i class="fas fa-times"></i></button>
		</div>
       
		<div class="contenedor contenedor-enlaces-nav">
			<div class="btn-departamentos" id="btn-departamentos"  @mouseover="drawer=true" @mouseout="drawer=false">
				<p>Todas las <span>Categorias</span></p>
				<i class="fas fa-caret-down"></i>
			</div>

			<div class="enlaces">
				<router-link to="/Registry"> Registrate  </router-link>
                <router-link to="/Login"> Iniciar sesion  </router-link>
			</div>
		</div>

		<div class="contenedor contenedor-grid">
			<div class="grid" :class="{'grid activo' : drawer}" id="grid" @mouseover="drawer=true" @mouseout="drawer=false">
				<div class="categorias">
					<button class="btn-regresar"><i class="fas fa-arrow-left"></i> Regresar</button>
					<h3 class="subtitulo">Categorias</h3>

					<a href="#" data-categoria="tecnologia-y-computadoras" @mouseover="computadores=true" @mouseout="computadores=false">Tecnología y Computadoras <i class="fas fa-angle-right"></i></a>
					<a href="#" data-categoria="libros" @mouseover="libros=true" @mouseout="libros=false">Libros <i class="fas fa-angle-right"></i></a>
					<a href="#" data-categoria="ropa-y-accesorios" @mouseover="ropa=true" @mouseout="ropa=false">Ropa y Accesorios <i class="fas fa-angle-right"></i></a>
					<a href="#" data-categoria="hogar-y-cocina" @mouseover="hogar=true" @mouseout="hogar=false">Hogar y Cocina <i class="fas fa-angle-right"></i></a>
					<a href="#" data-categoria="juegos-y-juguetes" @mouseover="juegos=true" @mouseout="juegos=false">Juegos y Juguetes <i class="fas fa-angle-right"></i></a>
					<a href="#" data-categoria="salud-y-belleza" @mouseover="salud=true" @mouseout="salud=false">Salud y Belleza <i class="fas fa-angle-right"></i></a>
					<a href="#" data-categoria="alimentos-y-bebidas" @mouseover="alimentos=true" @mouseout="alimentos=false">Alimentos y Bebidas <i class="fas fa-angle-right"></i></a>
				</div>

				<div class="contenedor-subcategorias" >
					<div class="subcategoria" :class="{'subcategoria activo' : computadores}" data-categoria="tecnologia-y-computadoras" @mouseover="computadores=true" @mouseout="computadores=false">
						<div class="enlaces-subcategoria">
							<button class="btn-regresar"><i class="fas fa-arrow-left"></i>Regresar</button>
							<h3 class="subtitulo" >Tecnología y Computadoras</h3>
							<a href="#">Laptops</a>
							<a href="#">Tablets</a>
							<a href="#">Computadoras de Escritorio</a>
							<a href="#">Monitores</a>
							<a href="#">Componentes</a>
						</div>

						<div class="banner-subcategoria">
							<a href="#">
								<img src="@/assets/tecnologia-banner-1.png" alt="">
							</a>
						</div>

						<div class="galeria-subcategoria">
							<a href="#">
								<img src="@/assets/tecnologia-galeria-1.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/tecnologia-galeria-2.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/tecnologia-galeria-3.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/tecnologia-galeria-4.png" alt="">
							</a>
						</div>
					</div>

					<div class="subcategoria" :class="{'subcategoria activo' : libros }" data-categoria="libros" @mouseover="libros=true" @mouseout="libros=false">
						<div class="enlaces-subcategoria">
							<button class="btn-regresar"><i class="fas fa-arrow-left"></i>Regresar</button>
							<h3 class="subtitulo"  >Libros</h3>
							<a href="#">Top Sellers</a>
							<a href="#">Ciencia Ficcion</a>
							<a href="#">Fantasia</a>
							<a href="#">Miedo</a>
						</div>

						<div class="banner-subcategoria">
							<a href="#">
								<img src="@/assets/libros-banner-1.png" alt="">
							</a>
						</div>

						<div class="galeria-subcategoria">
							<a href="#">
								<img src="@/assets/libros-galeria-1.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/libros-galeria-2.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/libros-galeria-3.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/libros-galeria-4.png" alt="">
							</a>
						</div>
					</div>

					<div class="subcategoria" :class="{'subcategoria activo' : ropa }" data-categoria="ropa-y-accesorios" @mouseover="ropa=true" @mouseout="ropa=false">
						<div class="enlaces-subcategoria">
							<button class="btn-regresar"><i class="fas fa-arrow-left"></i>Regresar</button>
							<h3 class="subtitulo">Ropa y Accesorios</h3>
							<a href="#">Ropa</a>
							<a href="#">Zapatos</a>
							<a href="#">Accesorios</a>
							<a href="#">Relojes</a>
						</div>

						<div class="banner-subcategoria">
							<a href="#">
								<img src="@/assets/ropa-banner-1.png" alt="">
							</a>
						</div>

						<div class="galeria-subcategoria">
							<a href="#">
								<img src="@/assets/ropa-galeria-1.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/ropa-galeria-2.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/ropa-galeria-3.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/ropa-galeria-4.png" alt="">
							</a>
						</div>
					</div>

					<div class="subcategoria" :class="{'subcategoria activo' : hogar }" data-categoria="hogar-y-cocina" @mouseover="hogar=true" @mouseout="hogar=false">
						<div class="enlaces-subcategoria">
							<button class="btn-regresar"><i class="fas fa-arrow-left"></i>Regresar</button>
							<h3 class="subtitulo">Hogar y Cocina</h3>
							<a href="#">Cocina</a>
							<a href="#">Electrodomesticos</a>
							<a href="#">Limpieza</a>
							<a href="#">Baño</a>
							<a href="#">Decoracion</a>
							<a href="#">Arte</a>
							<a href="#">Manualidades</a>
							<a href="#">Jardin</a>
						</div>

						<div class="banner-subcategoria">
							<a href="#">
								<img src="@/assets/hogar-banner-1.png" alt="">
							</a>
						</div>

						<div class="galeria-subcategoria">
							<a href="#">
								<img src="@/assets/hogar-galeria-1.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/hogar-galeria-2.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/hogar-galeria-3.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/hogar-galeria-4.png" alt="">
							</a>
						</div>
					</div>

					<div class="subcategoria" :class="{'subcategoria activo' : juegos }" data-categoria="juegos-y-juguetes" @mouseover="juegos=true" @mouseout="juegos=false">
						<div class="enlaces-subcategoria">
							<button class="btn-regresar"><i class="fas fa-arrow-left"></i>Regresar</button>
							<h3 class="subtitulo">Juegos y Juguetes</h3>
							<a href="#">Juguetes</a>
							<a href="#">Juegos de Mesa</a>
							<a href="#">Aire Libre</a>
							<a href="#">Muñecas</a>
						</div>

						<div class="banner-subcategoria">
							<a href="#">
								<img src="@/assets/juegos-banner-1.png" alt="">
							</a>
						</div>

						<div class="galeria-subcategoria">
							<a href="#">
								<img src="@/assets/juegos-galeria-1.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/juegos-galeria-2.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/juegos-galeria-3.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/juegos-galeria-4.png" alt="">
							</a>
						</div>
					</div>

					<div class="subcategoria" :class="{'subcategoria activo' : salud }" data-categoria="salud-y-belleza" @mouseover="salud=true" @mouseout="salud=false">
						<div class="enlaces-subcategoria">
							<button class="btn-regresar"><i class="fas fa-arrow-left"></i>Regresar</button>
							<h3 class="subtitulo">Salud y Belleza</h3>
							<a href="#">Cuidado de la Piel</a>
							<a href="#">Maquillaje</a>
							<a href="#">Lociones</a>
							<a href="#">Shampoo</a>
						</div>

						<div class="banner-subcategoria">
							<a href="#">
								<img src="@/assets/belleza-banner-1.png" alt="">
							</a>
						</div>

						<div class="galeria-subcategoria">
							<a href="#">
								<img src="@/assets/belleza-galeria-1.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/belleza-galeria-2.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/belleza-galeria-3.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/belleza-galeria-4.png" alt="">
							</a>
						</div>
					</div>

					<div class="subcategoria" :class="{'subcategoria activo' : alimentos }" data-categoria="alimentos-y-bebidas" @mouseover="alimentos=true" @mouseout="alimentos=false">
						<div class="enlaces-subcategoria">
							<button class="btn-regresar"><i class="fas fa-arrow-left"></i>Regresar</button>
							<h3 class="subtitulo">Alimentos y Bebidas</h3>
							<a href="#">Alimentos</a>
							<a href="#">Bebidas</a>
						</div>

						<div class="banner-subcategoria">
							<a href="#">
								<img src="@/assets/comida-banner-1.png" alt="">
							</a>
						</div>

						<div class="galeria-subcategoria">
							<a href="#">
								<img src="@/assets/comida-galeria-1.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/comida-galeria-2.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/comida-galeria-3.png" alt="">
							</a>
							<a href="#">
								<img src="@/assets/comida-galeria-4.png" alt="">
							</a>
						</div>
					</div>
				</div>
			</div>
		</div>
	</nav>
    

</template>
<script>

export default {
    name: 'Navbar',
    data(){
        return {
            drawer : false,
            fondo: "activo",
            computadores: false,
            libros: false,
            ropa: false,
            hogar: false,
            juegos: false,
            salud: false,
            alimentos: false

            

        }
   
    },
    computed: {
        dentro ()
        {
         if(drawer)
         {
             return drawer
         }
        }
    },    
    }




</script>

<style scoped>


a {
	text-decoration: none;
}

.contenedor {
	margin: auto;
	width: 90%;
	max-width: 1200px;
}

main article {
	background: #fff;
	margin: 20px 0;
	padding: 20px;
	height: 1000px;
}

/* ------------------------- */
/* Enlaces del NAV */
/* ------------------------- */
.menu {
	background: #B31E1E;
	padding: 5px 0;
	margin-bottom: 20px;
}

.menu .contenedor-botones-menu {
	/* display: flex; */
	display: none;
	justify-content: space-between;
}

.menu .contenedor-botones-menu button {
	font-size: 20px;
	color: #fff;
	padding: 10px 20px;
	border: 1px solid transparent;
	display: inline-block;
	cursor: pointer;
	background: none;
}

.menu .contenedor-botones-menu button:hover {
	border: 1px solid rgba(255,255,255, .4);
}

.menu .contenedor-botones-menu .btn-menu-cerrar {
	display: none;
}

.menu .contenedor-botones-menu .btn-menu-cerrar.activo {
	display: inline-block;
}

.menu .contenedor-enlaces-nav {
	display: flex;
	justify-content: space-between;
	align-items: center;
}

.menu .btn-departamentos {
	color: #fff;
	padding: 7px;
	border-radius: 3px;
	display: flex;
	align-items: flex-end;
	border: 1px solid transparent;
	font-size: 12px;
	cursor: default;
}

.menu .btn-departamentos i {
	margin-left: 20px;
	position: relative;
	bottom: 4px;
}

.menu .btn-departamentos:hover {
	border: 1px solid rgba(255,255,255, .4);
}

.menu .btn-departamentos span {
	display: block;
	font-size: 14px;
	font-weight: bold;
}

.menu .btn-departamentos p{
    margin:0px;
}

.menu .contenedor-enlaces-nav .enlaces a {
	color: #ccc;
	border: 1px solid transparent;
	padding: 7px;
	border-radius: 3px;
	font-size: 14px;
}

.menu .contenedor-enlaces-nav .enlaces a:hover {
	border: 1px solid rgba(255,255,255,.4);
}

/* ------------------------- */
/* GRID */
/* ------------------------- */
.contenedor-grid {
	position: relative;
}

.grid {
	width: 100%;
	display: none;
	position: absolute;
	top: 5px;
	z-index: 1000;
	grid-template-columns: repeat(4, 1fr);
	grid-template-rows: 1fr;
	grid-template-areas: "categorias subcategorias subcategorias subcategorias";
}

.grid.activo {
	display: grid;
}

.grid::before {
	content: "⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀";
	display: block;
	background: transparent;
	border-left: solid transparent;
	border-right: 10px solid transparent;
	border-bottom: 5px solid #ffffff;
	position: absolute;
	top: -5px;
	left: 10px;
}

.grid > div {
	background: #fff;
	box-shadow: 0px 3px 6px rgba(0,0,0,.10);
}

/* ------------------------- */
/* Categorias */
/* ------------------------- */

.grid .btn-regresar {
	background: #232F3E;
	color: #fff;
	border: none;
	padding: 10px;
	border-radius: 3px;
	margin: 20px;
	font-size: 16px;
	cursor: pointer;
	display: none;
}

.grid .btn-regresar i {
	margin-right: 10px;
}

.grid .categorias {
	grid-area: categorias;
	padding-top: 10px;
	min-height: 300px;
	overflow: auto;
}

.grid .categorias .subtitulo {
	display: none;
}

.grid .categorias a {
	color: #000;
	font-size: 14px;
	display: flex;
	justify-content: space-between;
	padding: 10px 20px;
}

.grid .categorias a i {
	display: none;
}

.grid .categorias a:hover {
	color: #E47911;
	font-weight: bold;
}

.grid .categorias a:hover i {
	display: inline-block;
}

/* ------------------------- */
/* Subcategorias */
/* ------------------------- */

.grid .contenedor-subcategorias {
	grid-area: subcategorias;
}

.grid .subcategoria {
	display: none;
	grid-template-columns: 1fr 1fr 1fr;
	grid-template-rows: 1fr;
	height: 100%;
}

.grid .subcategoria.activo {
	display: grid;
}

.grid .subcategoria img {
	width: 100%;
	vertical-align: top;
	height: 100%;
	object-fit: cover;
}

.grid .enlaces-subcategoria {
	padding-top: 10px;
	height: 100%;
	max-height: 300px;
	overflow: auto;
}

.grid .enlaces-subcategoria a {
	color: #000;
	display: block;
	font-size: 14px;
	padding: 10px 20px;
}

.grid .enlaces-subcategoria a:hover {
	color: #E47911;
}

.grid .subtitulo {
	font-size: 18px;
	font-weight: normal;
	color: #E47911;
	padding: 10px 20px;
}

.grid .banner-subcategoria a {
	display: block;
	height: 100%;
}

.grid .galeria-subcategoria {
	display: flex;
	flex-wrap: wrap;
	align-content: start;
}

.grid .galeria-subcategoria a {
	width: 50%;
	height: 50%;
}

/* ------------------------- */
/* Mediaqueies */
/* ------------------------- */
@media screen and (max-width: 1000px) {
	.menu .contenedor-enlaces-nav {
		padding: 0 2px;
	}

	.menu .contenedor {
		width: 100%;
	}
}

@media screen and (max-width: 800px) {
	.menu .contenedor {
		width: 90%;
	}

	.menu .contenedor-botones-menu {
		display: flex;
	}

	.menu .contenedor-enlaces-nav {
		padding: 20px;
		flex-direction: column;
		align-items: flex-start;
		justify-content: flex-start;
		position: fixed;
		left: 0;
		background: #232F3F;
		height: 100vh;
		width: 80%;
		z-index: 2000;
		transition: .3s ease all;
		transform: translate(-100%);
	}

	.menu .contenedor-enlaces-nav.activo {
		transform: translate(0%);
	}

	.menu .btn-departamentos {
		width: 100%;
		align-items: center;
		justify-content: space-between;
		cursor: pointer;
	}

	.menu .btn-departamentos i {
		position: static;
		margin-left: 20px;
		transform: rotate(-90deg);
	}

	.menu .enlaces {
		width: 100%;
	}

	.menu .enlaces a {
		display: block;
		margin: 10px 0;
		padding: 10px;
	}

	.grid {
		display: grid;
		transition: .3s ease all;
		transform: translateX(-100%);
		z-index: 3000;
		width: 80%;
		position: fixed;
		top: 0;
		left: 0;
		height: 100vh;
		grid-template-areas: "categorias categorias categorias categorias";
	}

	.grid.activo {
		transform: translateX(0%);
	}

	.grid::before {
		display: none;
	}

	.grid .btn-regresar {
		display: inline-block;
	}

	.grid .categorias .subtitulo {
		display: block;
	}

	.grid .contenedor-subcategorias {
		position: absolute;
		top: 0;
		width: 100%;
		height: 100%;
		transition: .3s ease all;
		transform: translateX(-100%);
		overflow: auto;
	}

	.grid .contenedor-subcategorias.activo {
		transform: translateX(0%);
	}

	.grid .contenedor-subcategorias .subcategoria {
		grid-template-columns: 1fr;
	}

	.grid .contenedor-subcategorias .banner-subcategoria {
		width: 100%;
		min-height: 250px;
		max-height: 350px;
	}

	.grid .enlaces-subcategoria {
		min-height: 50vh;
		overflow: auto;
	}

	.grid .contenedor-subcategorias .galeria-subcategoria a {
		width: 25%;
		height: 100%;
	}
}
</style>