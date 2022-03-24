 
<template>
  
  <div id="app" class='white'>
    <!-- navbar -->
    <div class="navbar-fixed">
      <nav>
        <div class="nav-wrapper blue-grey lighten-5">
          <a href="#!" class="brand-logo teal-text">GreenSystem </a>
          <a href="#" data-target="mobile-demo" class="sidenav-trigger teal-text"><i class="material-icons">menu</i></a>
          <ul class="right hide-on-med-and-down">
            <li><router-link to="/about" class='blue-text'>Home</router-link></li>
            <li><router-link to="/" class='blue-text'>Ayuda</router-link></li>
            <li>
              <!-- Dropdown trigger -->
              <a class='dropdown-trigger teal darken-4' href='#' data-target='dropdown1'>maxandree@unamad.edu.pe</a>
              <!-- Dropdown Structure -->
              <ul id='dropdown1' class='dropdown-content'>
                <li><router-link to="/about"><i class="material-icons">person</i> Mi perfil</router-link></li>   
                <li><router-link to="/about"><i class="material-icons">build</i>Configuración</router-link></li>
                <li class='no-pading'><a href="#!" class='waves-effect waves-light  red white-text'><i class="material-icons left">logout</i>Cerrar Sesión</a></li>
              </ul>
            </li>
          </ul>
        </div>
      </nav>
    </div>
    <!-- sidebar lado derecho -->
    <ul class="sidenav" id="mobile-demo">
      <li>
        <div class="user-view">
          <div class="background">
            <img src="../public/img/icons/wall.jpg">
          </div>
          <div class=" container">
            <a href="#!" class="brand-logo teal-text"><h5>GreenSystem</h5> </a>
            <a href="#user"><img class="circle z-depth-2" src="../public/img/icons/android-chrome-192x192.png"></a>
            <a href="#name"><span class=" black-text name">Max Andree</span></a>
            <a href="#email"><span class="black-text email">jdandturk@gmail.com</span></a>
          </div>
        </div>
      </li>

      <li><router-link to="/about" ><i class="material-icons">home</i>Principal</router-link></li>
      <li><router-link to="/about"><i class="material-icons">person</i> Mi perfil</router-link></li>   
      <li><router-link to="/about"><i class="material-icons">build</i>Configuración</router-link></li>
      <li><router-link to="/" ><i class="material-icons">help</i>Ayuda</router-link></li>
      <li><router-link to="/about" class='red-text'><i class="material-icons red-text">logout</i>Cerrar Sesión</router-link></li>
    </ul>

     <!-- MENU LATERAL -->
     
    <div class="row light ">
      
      <div class="fixed-action-btn">
        <a class="btn-floating btn-large red">
          <i class="large material-icons">mode_edit</i>
        </a>
        <ul>
          <li><a class="btn-floating red"><i class="material-icons">insert_chart</i></a></li>
          <li><a class="btn-floating yellow darken-1"><i class="material-icons">format_quote</i></a></li>
          <li><a class="btn-floating green"><i class="material-icons">publish</i></a></li>
          <li><a class="btn-floating blue"><i class="material-icons">attach_file</i></a></li>
        </ul>
      </div>

    <!-- MENU LATERAL -->
      <div class='col m1 s1 l1 no-padding ' >   
          <div class=" submenu center-align z-depth-5">
              <div >
                <a href="" class=" center-align tooltipped" data-position="right" data-tooltip="Plantas"><i class="material-icons">forest</i></a>
              </div>
              <div>
                <a href="" class=" center-align tooltipped" data-position="right" data-tooltip="Medidas"><i class="material-icons">architecture</i></a>
              </div>
              <div>  
                <a href="" class=" center-align tooltipped" data-position="right" data-tooltip="Familias"><i class="material-icons">terrain</i></a>
              </div>
              <div>  
                <a href="" class=" center-align tooltipped" data-position="right" data-tooltip="Localización"><i class="material-icons">room</i></a>
              </div>
              <div>  
                <a href="" class=" center-align tooltipped" data-position="right" data-tooltip="Reportes"><i class="material-icons">analytics</i></a>
              </div>
              <div>  
                <a href="" class=" center-align tooltipped" data-position="right" data-tooltip="Ajustes"><i class="material-icons">build</i></a>
              </div>
          </div>
      </div>
    <!-- CUERPO DE LA PAGINA -->
      <div class="col m11 s11 l11 no-padding ">
        
          <!-- breadcrumps -->
          <div class="link">
            <nav>
              <div class=" row nav-wrapper white black-text">
                <div class='left col s3 l9 m8 '><h3>Plantas</h3></div>
                <div class="right col s9 l3 m4 blue-text">
                  <a href="#!" class="breadcrumb blue-text">Plantas</a>
                  <a href="#!" class="breadcrumb blue-text">Second</a>
                  <a href="#!" class="breadcrumb blue-text">Third</a>
                </div>
              </div>
            </nav>
          </div>

        <div class="cuerpo">
          <router-view/>
        </div>
      </div>

  
    </div>

 


  </div>
</template>

/* estilos css */
<style scoped>
  .submenu div{
    margin-top:20%;
  } 
  .submenu div a i{
    font-size: 40px;
    color:white;
  }
  .submenu{
    position:fixed;
    background-color: #004d40;
    height:100%;
    width:8%;
  }
  .cuerpo{
    margin: 2%;
    background-color: whitesmoke;
  }
    /*.no-padding{
      padding:0%;
      margin:0%;
    }
     .no-mt{

      margin-top: 0%;
    } */
    .no-nav{
      background: none;
      border:0px;
      box-shadow:none;
    }
  
    .submenu div a :hover{
      opacity:0.8;
    }

    /* BREADCRUMP O LINKS */
    .link{
      margin:1%;
      padding:1%;
    }

  /* estilos responsive */ 
  @media (max-width: 580px) {
    .submenu div a i{
        font-size: 20px;
        color:white;
    }
  }

</style>
<script>
    document.addEventListener('DOMContentLoaded', function() {
        var elems = document.querySelectorAll('.dropdown-trigger');
        var instances = M.Dropdown.init(elems,{
             alignment: 'right',
             hover: false,
             inDuration: 100,
             constrainWidth: true    
        });
    });
  //js para tooltips
    document.addEventListener('DOMContentLoaded', function() {
      var elems = document.querySelectorAll('.tooltipped');
      var instances = M.Tooltip.init(elems,{
        inDuration:500,
      });
    });
     /* document.addEventListener('DOMContentLoaded', function() {
    var elems = document.querySelectorAll('.sidenav');
    var instances = M.Sidenav.init(elems,{
        edge: 'left',
        inDuration: 800
    });
  }); */

 </script>