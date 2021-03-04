<template>
    <div>
            <nav class = "navbar navbar-light barColor navbar-expand-sm">
                <div class="container-fluid">
                    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarTogglerDemo01" aria-controls="navbarTogglerDemo01" aria-expanded="false" aria-label="Toggle navigation">
                        <span class="navbar-toggler-icon"></span>
                    </button>
                    <div class="collapse navbar-collapse" id="navbarTogglerDemo01">
                        <a class="navbar-brand" href="#">Moover</a>
                        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                            <li class="nav-item">
                                <a class="nav-link navLink" aria-current="page" >Yo Repartidor</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link navLink" > Yo Empresa</a>
                            </li>
                        </ul>
                    </div>
                </div>
                
                    
                    
               
            </nav>
        <div id = "fondo">
            <div class="content-inicio" >
                <div class="about-section">
                    <h1>Moover</h1>
                    <p>Somos una empresa dedicada a simplificarte la vida.</p>
                    <p>Tienes un pedido, necesitas movilidad, nosotros la tenemos de forma inmediata</p>
                    <p>Moover...Cuando quieras, donde quieras</p>
                </div>
                



            </div>
        </div>
        
    </div>
</template>
<style>
#fondo {

	
    display: flex;
    align-items: center;
    flex-direction: column;
    width: 100%;
    min-width: 320px;
    height: 100vh;
    background-image: linear-gradient(rgb(246,245,245, 0.5),rgb(246,245,245,.5)),url(http://www.commercebloom.com/wp-content/uploads/2018/02/AdobeStock_93938728-1200x800.jpeg);
    background-position: 50%;
    background-size: cover;
    background-repeat: no-repeat;
}
h1{
    color:#1f3c88;
}

a{
    color: white;
    font-weight: bold;
}
.content-inicio{
      background:#f6f5f5 ;
    padding: 10pt;
    border-radius: 10pt;
}


.about-section {
  padding: 50px;
  text-align: center;
  color: #070d59;
  margin: 0 auto;
  margin-top: 10%;
  margin-bottom: 10%;
}



.barColor{
    background: #1f3c88;
}


</style>