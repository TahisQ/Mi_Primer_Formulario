# Mi_Primer_Formulario
Formulario para el ingreso al perfil de estudiante.
<!DOCTYPE html>

<html>
    <head>
        <title>TODO supply a title</title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
    </head>
    <body>
        
        <h1>Formulario usuario</h1>
        
        <form class="form" method="post">
            <label>Nombre</label>
            <input type="text" name="nombre" value=""><br>
            <label id="validar_nombre"></label><br>
            <label>Apellido</label>
            <input type="text" name="apellido" value="">
            <label id="validar_apellido"></label><br>
            <br><label>Edad</label>
            <input type="text" name="edad" value="">
            <label id="validar_edad"></label><br>
            <br><label>Nacionalidad</label>
            <input type="text" name="nacionalidad" value="">
            <label id="validar_nacionalidad"></label><br>
            <br><label>Correo</label>
            <input type="email" name="correo" value="">
            <label id="validar_correo"></label><br>
            <br><label>Contraseña</label>
            <input type="password" name="contraseña" value="">
            <p>Contraseña debe contener 8 o mas caracteres</p>
            <label id="validar_contraseña"></label><br>
            
            <br><input type="button" name="enviar" value="ENVIAR" onclick="enviarDatos()">   
        </form>
        
        <script>
            
            function enviarDatos(){
                let nombre = document.getElementsByName('nombre')[0].value;
                let validar_nombre =document.getElementById('validar_nombre');
                
                if(nombre===''){
                    validar_nombre.innerHTML = "debe ingresar un nombre";
                }else{
                    validar_nombre.innerHTML = "OK";
                }
                 
                let edad = document.getElementsByName('edad')[0].value;
                let validar_edad=document.getElementById('validar_edad');
                
                if(edad >= 18 && edad !== ''){
                    validar_edad.innerHTML = "OK";
                }else{
                    validar_edad.innerHTML = "Debe ingresar una edad mayor o igual a 18";      
                }
             
                let nacionalidad = document.getElementsByName('nacionalidad')[0].value;
                let validar_nacionalidad=document.getElementById('validar_nacionalidad');
                
                if(nacionalidad===''){
                    validar_nacionalidad.innerHTML = "debe ingresar una nacionalidad";
                }else{
                    validar_nacionalidad.innerHTML = "OK";
                }
                
                let correo = document.getElementsByName('correo')[0].value;
                let validar_correo=document.getElementById('validar_correo');
                
                if(correo===''){
                    validar_correo.innerHTML = "debe ingresar un correo";
                }else{
                    validar_correo.innerHTML = "OK";
                }
             
                let contraseña = document.getElementsByName('contraseña')[0].value;
                let validar_contraseña=document.getElementById('validar_contraseña');
                
                if(contraseña.length>=8){
                    validar_contraseña.innerHTML = "";
                }else{
                    validar_contraseña.innerHTML = "OK";
                }
 
            }
                
               
        </script>
    </body>
</html>
