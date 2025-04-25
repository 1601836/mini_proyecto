# mini_proyecto
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel='stylesheet'>
    <title>Document</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            text-decoration: none;
            list-style: none;
            font-family: sans-serif;
        }
        header {
            background-color: blue;
            color: white;
            position: fixed;   
            top: 0;
            left: 0;
            width: 100%;          
            z-index: 1000;        
            height: 80px;
        }

        .contenedor_menu {
            max-width: 1200px;
            margin: auto;
            height: 100%;
            display: flex;
            align-items: center;
            background-color: blue;
            box-shadow: 0px 0px 50px 20px rgba(0, 0, 0, 0.5); 
            justify-content: space-between;
        }        
        .menu{
            display: flex;
            align-items: center;   
            height: 100%;
            background-color: blue;         
        }
        #check_menu{display: none;}
        #label_menu{display: none;}
        nav{
            width: 100%;
            height: 100%;
        }
        nav > ul{
            height: 100%;
            display: flex;
            align-items: center;
            background-color: blue;
        }
        nav > ul > li{
            padding: 30px 50px;
            height: 100%;


        }
        nav > ul > li > a{
            height: 100%;
            color: white;
        }
        nav > ul > li:hover{
            background-color: aqua;
            font-weight: bolder;
            transition: all 300ms ease;
            box-shadow: 0px 0px 50px 20px rgba(0, 0, 0, 0.5);
            
        }
        nav > ul > li:hover a{ 
            padding: 0;          
            color: black;
            transition: all 300ms ease
            
        }
        main{
            height: 500%;
        }
        footer{
            display: grid;
            place-items: center;
            background-color: beige;
        }
        main{
            background: url(Imagenes/ParCurFondo.avif);
            margin-top: 80px;
            width: 100%;
            background-size: 100%;
            background-repeat: repeat-y;
            height: 3800px;      /*            main{
                background: url(Imagenes/ParCurFondo.avif);
                margin-top: 80px;
                width: 100%;
                background-size: 100%;
                background-repeat: repeat-y;
                height: 1500px;          
            }*/
        }
        main::before {
            content: "";
            position: absolute;
            top: 0; left: 0;
            width: 100%;
            height: 410%;
            background-color: rgba(0, 0, 0, 0.5); 
            z-index: 1;
        }
        .contenido{
            height: 100dvh;
            display: grid;
            grid-template-areas:  
                "texto texto"
                "cont pro";
            grid-template-columns: 20% 80%;
            grid-template-rows: 20% 80%;
            gap: 10px;
            padding: 25px;
        }
        .texto{
            grid-area: texto;
            background-color: rgba(0, 0, 0, 0.5);
            padding: 10px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .subtexto{
            max-width: 1200px;
            padding-left: 10px;
        }
        .texto p{
            font-size: 20px;
            color: whitesmoke;
        }
        .texto img{
            z-index: 1;
        }
        .imagenes_submenu{
            display: flex;
            gap: 10px;
            margin-right: 20px;
        }
        .imagenes_submenu img:hover {
                transform: scale(1.30);
            }
        .sum_menu{
            grid-area: cont;
            
            
        }
        .productos{
            grid-area: pro;
            
        }

        /*main sub_menu*/
        .sum_menu {
            top: 300px;
            z-index: 10;
            width:350px;
            position: fixed;
            background-color: transparent;
             
        }
        .sum_menu > nav > ul{   
            background-color: transparent;
            width: 100%;    
            display: block;
            height: 110px;
            

        }
        .sum_menu > nav > ul > li{
            background-color: transparent;
            display: grid;
            place-items: center;
            padding-top: 70px;
            background-color: transparent;             
        }
        .sum_menu > nav > ul > li > a{
            color: black;  
            font-size: 27px;
            font-weight: bolder; 
                      
        }
        .sum_menu > nav > ul > li:hover {
            padding: 50px 20px;
            align-items: center;
            justify-content: center;
            background-color: red;
            transition: all 300ms ease;
            font-size: 30px;
        }

        /*main productos*/
        .productos{
            display: block;  
            z-index: 600;     
            height: 500%;     
        }
        .ofertas{
            text-align: center; 

        }
        h1{
            margin-top: 40px;
            color: white;
        }
        .productos_one{
            display: flex;
            justify-content: space-around;
            padding: 120px 30px;
            z-index: 50;
        }
        .pren_ni{
            z-index: 150;
            background-color: beige;
            border-radius: 10px;
            
        }
        .pren_ni img{
            padding-top: 10px;
            padding: 10px 5px;
            width: 300px;
            height: 300px;
        }
        h2{
            display: block;
            margin: 10px;
        }
        input{
            margin: 10px;
            width: 90%;
            height: 30px;
            padding: auto;
            border-radius: 5px;
            background-color: brown;
            color: black;
            font-weight: bolder;
            font-size: 15px;
        }

        @media (max-width:750px){

            #label_menu{display: flex;  margin-right: -150px;}
            .menu nav ul{
                flex-direction: column;
                visibility: hidden;
                opacity: 0;
                background-color: blue;
                height: 350px;
                z-index: 10; 
                text-align: center;  
                margin-top: 80px;
                width: 180px;
                     
            }
            nav ul li{
                width: 100%;
                
            }
            #check_menu:checked ~ nav ul{
                visibility: visible;
                opacity: 1;                
            }
            main{
                background: url(Imagenes/ParCurFondo.avif);
                margin-top: 80px;
                width: 100%;
                background-size: 100%;
                background-repeat: repeat-y;
                height: 7900px;          
            }
            .texto{
                width: 100%;
                height:450px;
                flex-direction: column;
            }
            p{
                display: none;
            }
            .imagenes_submenu {
                
                align-items: center;
                margin-top: -20px;
                flex-direction: column; 
                z-index: 1;
                text-align: center;               
            }
            .imagenes_submenu img{               
                margin-top: 10px;
                z-index: 1;
            }

            .imagenes_submenu img:hover {
                transform: scale(1.30);
            } 
            .sum_menu{
                width: 100px;
                display: flex;
                top: -200px;
                
            }
            .sum_menu nav{
                display: flex;
            }
            .sum_menu,.productos{
                margin-top: 280px;
                height: 800px;
            }   
            .sum_menu nav > ul > li{
                
                padding: 20px 20px;
                width: 150px;             
            }
            .sum_menu nav > ul > li > a{
                display: grid;
                place-items: center;
            }
            
            .sum_menu nav > ul > li > a{
                text-align: center;
                justify-content: center;
                align-items: center;
            }

            /*main productos*/
            .productos_one{
                display: block;
                justify-content: space-around;
                padding: 30px 30px;
                z-index: 50;
            }
            .pren_ni{
                margin-top: 30px;
            }
            
        }
    </style>
</head>
<body>
    <div>
        <header>
            <div class="contenedor_menu">
                <div class="logo">
                    <i class='bx bxl-go-lang' style="font-size: 150px; color: black;margin-left: 20px;"></i>                 
                </div>
                <div class="menu">
                    <input type="checkbox" id="check_menu">
                    <label for="check_menu" id="label_menu">
                        <i class='bx bx-menu icono' style="font-size: 50px; margin-right: 0;"></i></label>
                    <nav>
                        <ul>
                            <li><a href="WEB.HTML">HOME</a></li>
                            <li><a href="Index.html">TIENDA</a></li>
                            <li><a href="">SOBRE NOSOTROS</a></li>
                            <li><a href="">CONSULTAS</a></li>
                        </ul>
                    </nav>
                </div>
            </div>
        </header>
        <main>
            <div class="contenido">
                <div class="texto">
                    <div class="subtexto">
                        <p>Hacer ejercicio no solo es para quienes quieren verse bien. Es una de las mejores decisiones que una persona puede tomar para cuidar su cuerpo y su mente.
                            Cuando hacés ejercicio, fortalecés tu corazón, mejorás tu respiración y aumentás tu energía. Además, tu cuerpo libera endorfinas, que ayudan a reducir 
                            el estrés y mejorar el ánimo. También dormís mejor, pensás con más claridad y sentís más motivación en tu día a día.                     
                            No se trata de ser un atleta, sino de moverse. Caminar, estirarte, bailar o andar en bici ya cuentan. Lo importante es empezar y hacerlo parte de tu vida.                      
                        </p> 
                    </div>  
                    <div class="imagenes_submenu">
                        <img src="Imagenes/Woman.jpg" alt="" width="150px">
                        <img src="Imagenes/BalonNiña.jpg" alt="" width="200px">
                        <img src="Imagenes/Gol.jpg" alt="" width="150px">
                    </div>                
                </div>
                <div class="sum_menu">
                    <nav>
                        <ul>
                            <li><a href="">DEPO. NIÑOS</a></li>
                            <li><a href="">DEPO. ADULTO</a></li>
                            <li><a href="">URBAN HOMBRES</a></li>
                            <li><a href="">URBAN MUJERES</a></li>
                            <li><a href="">ELEGANCIA</a></li>
                        </ul>
                    </nav>
                </div>
                <div class="productos">
                    <div class="ofertas" id="one">
                        <h1>DEPORTIVO NIÑOS</h1>
                        <div class="productos_one">
                            <div class="pren_ni">
                                <img src="Imagenes/adidas.jpg" alt="">
                                <h2>Conjunto Depo.</h2>
                                <label for="">$ 40.00</label>
                                <input type="submit" value="Agregar prenda" onclick="mostrarMensaje('Conjunto Depo.')">
                            </div>
                            <div class="pren_ni">                           
                                <img src="Imagenes/mesi.jpeg" alt="">
                                <h2>Camisetas Depo.</h2>
                                <label for="">$ 40.00</label>
                                <input type="submit" value="Agregar prenda" onclick="mostrarMensaje('Camisetas Depo.')">
                            </div>
                            <div class="pren_ni">
                                <img src="Imagenes/besi.webp" alt="">
                                <h2>Fans Wolf</h2>
                                <label for="">$ 40.00</label>
                                <input type="submit" value="Agregar prenda" onclick="mostrarMensaje('Fans Wolf')">
                            </div>
                        </div>
                    </div>
                    <div class="ofertas" id="two">
                        <h1>DEPORTIVO ADULTO</h1>
                        <div class="productos_one">
                            <div class="pren_ni">
                                <img src="Imagenes/Deport.jpg" alt="">
                                <h2>Cacheta Adidas</h2>
                                <label for="">$ 40.00</label>
                                <input type="submit" value="Agregar prenda" onclick="mostrarMensaje('Cacheta Adidas')"> 
                            </div>
                            <div class="pren_ni">
                                <img src="Imagenes/Liugi.avif" alt="">
                                <h2>Luigi Mix</h2>
                                <label for="">$ 40.00</label>
                                <input type="submit" value="Agregar prenda" onclick="mostrarMensaje('Luigi Mix')">
                            </div>
                            <div class="pren_ni">
                                <img src="Imagenes/Mbape.jpg" alt="">
                                <h2>Conjunto Mbappé</h2>
                                <label for="">$ 40.00</label>
                                <input type="submit" value="Agregar prenda" onclick="mostrarMensaje('Conjunto Mbappé')"> 
                            </div>
                        </div>
                    </div>
                    <div class="ofertas" id="three">
                        <h1>EXCLUSIVO URBAN HOMBRES</h1>
                        <div class="productos_one">
                            <div class="pren_ni">
                                <img src="Imagenes/Urban.jpeg" alt="">
                                <h2>New York .Man</h2>
                                <label for="">$ 40.00</label>
                                <input type="submit" value="Agregar prenda" onclick="mostrarMensaje('New York .Man')">
                            </div>
                            <div class="pren_ni">
                                <img src="Imagenes/CargoHOm.jpg" alt="">
                                <h2>Cargo .Man</h2>
                                <label for="">$ 40.00</label>
                                <input type="submit" value="Agregar prenda" onclick="mostrarMensaje('Cargo .Man')">
                            </div>
                            <div class="pren_ni">
                                <img src="Imagenes/CargoShort.avif" alt="">
                                <h2>Cargo short .Man</h2>
                                <label for="">$ 40.00</label>
                                <input type="submit" value="Agregar prenda" onclick="mostrarMensaje('Cargo short .Man')">
                            </div>
                        </div>
                    </div>
                    <div class="ofertas" id="four">
                        <h1>EXCLUSIVO URBAN MUJERES</h1>
                        <div class="productos_one">
                            <div class="pren_ni">
                                <img src="Imagenes/CargoWonman.jpg" alt="">
                                <h2>Cargo .Woman</h2>
                                <label for="">$ 40.00</label>
                                <input type="submit" value="Agregar prenda" onclick="mostrarMensaje('Cargo .Woman')">
                            </div>
                            <div class="pren_ni">
                                <img src="Imagenes/BluzaWoman.jpg" alt="">
                                <h2>Cacheta .Woman</h2>
                                <label for="">$ 40.00</label>
                                <input type="submit" value="Agregar prenda" onclick="mostrarMensaje('Cacheta .Woman')">
                            </div>
                            <div class="pren_ni">
                                <img src="Imagenes/CoatWoman.jpg" alt="">
                                <h2>Coats .Woman</h2>
                                <label for="">$ 40.00</label>
                                <input type="submit" value="Agregar prenda" onclick="mostrarMensaje('Coats .Woman')">
                            </div>
                        </div>
                    </div>
                    <div class="ofertas" id="five">
                        <h1>TRAJES ELEGANTES</h1> 
                        <div class="productos_one">
                            <div class="pren_ni">
                                <img src="Imagenes/EleNeWo.jpg" alt="">
                                <h2>Vestino negro .W</h2>
                                <label for="">$ 40.00</label>
                                <input type="submit" value="Agregar prenda" onclick="mostrarMensaje('Vestino negro .W')">
                            </div>
                            <div class="pren_ni">
                                <img src="Imagenes/EleWom.webp" alt="">
                                <h2>Elegante .Woman</h2>
                                <label for="">$ 40.00</label>
                                <input type="submit" value="Agregar prenda" onclick="mostrarMensaje('Elegante .Woman')">
                            </div>
                            <div class="pren_ni">
                                <img src="Imagenes/EleHom.jpg" alt="">
                                <h2>Traje Elegante</h2>
                                <label for="">$ 40.00</label>
                                <input type="submit" value="Agregar prenda" onclick="mostrarMensaje('Traje Elegante Hombre')">
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </main>
        <footer>
            <h1>Pie de pagina</h1>
        </footer>
    </div>
    <script>
        /*seccion 1*/
        function mostrarMensaje(prenda) {
          alert("Se agrego ->    " + prenda  );
        }

      </script>
</body>
</html>
