<p align="center"><img width="250px" src="https://i.postimg.cc/G3sys4sS/logo-studiove.png" alt="logo de Studio Ve Style"></p>

---
<h1 align="center">Studio Ve Style</h1>

## Repositorio / Repository
Proyecto final del curso de Desarrollo Web de Coderhouse.

Final proyect of the Web Development course by Coderhouse.

## Introducción / Introduction
Studio Ve Style®, marca destinada a impulsar y promover una manicuría más consciente y amigable con el medioambiente, por medio de cursos y asesorías tanto online como presenciales.

Studio Ve Style®, brand designed to boost and promote a more conscious and environmentally friendly manicure, through courses and coaching sessions both online and face-to-face.

## Autor / Author
Alexandra Ludmila Maimo

## Desarrollo / Development

**Menú hamburguesa hecho enteramente con html y css.**
**Hamburger menu done entirely with html and css.**

```html
            <div class="menu-mobile">
                <input type="checkbox" id="check">
                <label for="check" class="check-btn">
                    <img src="assets/img/menu-hamburguesa.png" alt="menu hamburguesa" class="icono-menu">
                </label>
                <ul class="mobile-navbar">
                    <li><a href="pages/sobre-mi.html">SOBRE MI</a></li>
                    <li><a href="pages/servicios.html">SERVICIOS</a></li>
                    <li><a href="pages/para-vos.html">PARA VOS</a></li>
                    <li><a href="pages/galeria.html">GALERIA</a></li>
                    <li><a href="pages/contacto.html">CONTACTO</a></li>
                </ul>
                <div class="logo-marca">
                    <a href="index.html"><img src="assets/img/logonavbar.png" alt="logo de Studio Ve Style en negro" class="logo-mobile"></a>
                </div>
            </div>
```
```sass
        .menu-mobile {
            width: 100vw;
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            background-color: $color-principal;
            position: fixed;
            top: 0;
            z-index: 1;
            #check {
                display: none;
                &:checked ~ ul{
                    left: 0;
                }
            }
            .check-btn {
                @include flex (unset, flex-start, center);
                padding-left: 12px;
                .icono-menu {
                    @include medidas (24px, 24px);
                }
            }
            .mobile-navbar {
                @include medidas (100%, 500px);
                background-color: $color-mobile;
                margin-top: 70px;
                padding: 50px;
                @include flex (column, center, center);
                text-align: center;
                gap: 30px;
                list-style: none;
                position: fixed;
                transition: all 0.5s;
                left: -100%;
                li{
                    @include flex (unset, center, center);
                    @include medidas (200px, 50px);
                    box-shadow: 6px 6px 30px 3px $box-shadow;
                    transition: all 0.5s;
                    &:hover{
                        background-color: $color-terciario;
                        transform:scale(1.1);
                    }
                    a{
                        @include flex (unset, center, center);
                        border-radius: 20px;
                        @include medidas (100%, 100%);
                        text-decoration: none;
                        color: $color-secundario;
                        font-family: $tipografia-secundaria;
                        font-weight: normal;
                        font-size: 18px;
                        &:hover{
                            font-weight: bold;
                        }
                    }
                }        
            }
            .logo-marca {
                height: 70px;
                justify-self: center;
                .logo-mobile {
                    height: 70px;
                }
            }
        }
```
**Cards con transiciones.**
**Cards with transitions.**

```html
                    <div class="servicios-fotos">
                        <figure>
                            <img src="../assets/img/coaching.jpg" alt="mujer joven hablando por altavoz">
                            <div class="capa">
                                <h3>Coaching</h3>
                                <p>Plan y estrategia para tu negocio. F.O.D.A. Venta de servicios y/o productos. Visibilización en RRSS. Rentabilidad. ¡Y más!</p>
                            </div>
                        </figure>
                    </div>
```
```sass
        .servicios-fotos {
            @extend %medidas;
            @include flex (row wrap, center, center);
            gap: 25px;
            figure {
                @include medidas (500px, 500px);
                position: relative;
                overflow: hidden;
                border-radius: 6px;
                box-shadow: 0px 15px 25px $box-shadow;
                cursor: pointer;
                img {
                    @include medidas (100%, 100%);
                    transition: all 500ms ease-out;
                }
                .capa {
                    position: absolute;
                    top: 0;
                    width: 100%;
                    height: 100%;
                    background: $color-terciario;
                    transition: all 500ms ease-out;
                    opacity: 0;
                    visibility: hidden;
                    text-align: center;
                }
                &:hover > .capa {
                    opacity: 1;
                    visibility: visible;
                }
                &:hover > .capa h3 {
                    margin-top: 10px;
                }
                .capa h3 {
                    color: $color-secundario;
                    font-family: $tipografia-secundaria;
                    font-weight: bold;
                    transition: all 500ms ease-out;
                }
                .capa p {
                    @include title (100%, center, 0, $tipografia-principal, normal, 26px);
                    color: $color-secundario;
                    line-height: 2;
                    max-width: 450px;
                    margin: auto;
                    transition: all 500ms ease-out;
                    margin-top: 0;
                }
            }
        }
```

## Tecnologías utilizadas / Implemented technologies

<p align="center"><img width="100%" src="https://i.postimg.cc/2jB088jC/technologies.png" alt="logos de html5, css3 y sass" title="logos de html5, css3 y sass"></p>

## Software utilizado / Implemented software

<p align="center"><img width="100%" src="https://i.postimg.cc/XNKpFqWV/software.png" alt="imagen con logos de Visual Studio Code, Node.js, Photoshop, Illustrator y Figma" title="logos de Visual Studio Code, Node.js, Photoshop, Illustrator y Figma"></p>

## Tipografías / Typo
**- Títulos/Headings/Navbar: Quicksand, sans-serif.**
<p align="center"><img width="100%" src="https://i.postimg.cc/G3B97Kvm/quicksand-font-character-map.png" alt="mapa de fuente Quicksand, sans-serif" title="mapa de fuente Quicksand, sans-serif"></p>

**- Párrafos/Paragraphs: Libre Baskerville, serif.**
<p align="center"><img width="100%" src="https://i.postimg.cc/9FY2Jwgf/libre-baskerville-font-character-map.png" alt="mapa de fuente Libre Baskerville, serif" title="mapa de fuente Libre Baskerville, serif"></p>

**- Logo: Playlist Script.**
<p align="center"><img width="100%" src="https://i.postimg.cc/LXtQ2L1Y/Playlist-Script.png" alt="fuente Playlist Script" title="fuente Playlist Script"></p>

## Colores / Colors

<p align="center"><img width="100%" src="https://i.postimg.cc/gJ73bRL3/colors-palette.png" alt="paleta de colores de la web"></p>

## Licencia / License
[MIT](https://opensource.org/licenses/MIT)