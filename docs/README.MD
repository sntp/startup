# Documentation

This module contains documentation for this project.

## File structure

+ */docs* - contains compiled documentation
  - */docs/api* - generated api from swagger file
+ */img* - images
  - */img/plantUml* - generated diagrams from plantUml files
+ */src* - source code of generated resources (swagger, plantUml)
  - */src/plantUml* - plantUml directory
  - */src/swagger/api.yml* - swagger source code

## Build
To build documentation run

    mvn clean process-resources
Please, keep all compiled files in repository