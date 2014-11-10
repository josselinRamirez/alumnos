alumnos
=======

es un breve registro de alumns donde se puede guardar eliminar edita. 
<!DOCTYPE html>
<html ng-app="aplicacion">
    <head>
        <meta charset="utf-8" />
        <title> registrar alumnos </title>
        <link type="text/css" href="/stylesheets/bootstrap.min.css" rel="stylesheet" />
        <script type="text/javascript" src="/javascripts/angular.min.js"></script>
        <script type="text/javascript" src="/javascripts/script.js"></script>
    </head>
    <body>
        <div class="container" ng-controller="Clientes">
            <h1> ALUMNOS </h1>
            <form action="javascript:void(0);">
                <div class="row">
                    <div class="span4">
                        <label> Nombre </label>
                        <input type="text" ng-model="nombre" />
                    </div>
                    <div class="span4">                    
                        <label> Apellido </label>
                        <input type="text" ng-model="apellido" />
                    </div>
                    <div class="span4">
                        <label> Domicilio </label>
                        <input type="text" ng-model="domicilio" />
                    </div>
                </div>
                <div class="row">
                    <div class="span4">
                        <label> Teléfono </label>
                        <input type="text" ng-model="telefono" />
                    </div>
                    <div class="span4">
                        <label> Email </label>
                        <input type="text" ng-model="email" />
                    </div>                    
                </div>
                <div class="row">
                    <div class="span4">
                        <input type="submit" value="Guardar" class="btn btn-success" ng-click="guardarCliente()" />
                        <input type="button" value="Limpiar" class="btn btn-danger" ng-click="limpiarDatos()" />
                    </div>
                </div>
            </form>
            <table class="table">
                <thead>
                    <tr>
                        <th> Nombre </th>
                        <th> Apellido </th>
                        <th> Domicilio </th>
                        <th> Teléfono </th>
                        <th> Email </th>
                        <th>  </th>
                        <th>  </th>
                    </tr>
                </thead>
                <tbody>
                    <tr ng-repeat="item in clientes">
                        <td> {{item.nombre}} </td>
                        <td> {{item.apellido}} </td>
                        <td> {{item.domicilio}} </td>
                        <td> {{item.telefono}} </td>
                        <td> {{item.email}} </td>
                        <td> <a href="javascript:void(0);" class="btn btn-info" ng-click="recuperarCliente($index)"> Editar </a> </td>
                        <td> <a href="javascript:void(0);" class="btn btn-danger" ng-click="eliminarCliente($index)"> Eliminar </a> </td>
                    </tr>
                </tbody>
            </table>
        </div>
    </body>
</html>
