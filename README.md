# Project Thor Arm Robot

## Instalacion
Se requiere la instalacion de un espacio de trabajo en: [Moveit](https://ros-planning.github.io/moveit_tutorials/)

Cada vez que hay cambios, correr:
```sh
catkin build
```

Recostrucciòn hecha del github: Thor Arm Moveit (https://github.com/b-adkins/thor_arm_moveit)


* Si se desea hacer una nueva creacion de un mejor diseño, se debe usar el moveit assistant, seguir los pasos de:
(https://ros-planning.github.io/moveit_tutorials/doc/setup_assistant/setup_assistant_tutorial.html)


Pasos para correr todo:
### Probar obstaculos
Abrir Rviz del Thor:
```sh
roslaunch thor_arm_new_moveit demo.launch
```

Correr codigo en Python para obtener informacion:
```sh
rosrun thor_group_python thor_group.py
```

Correr codigo de colocar obstaculos:
```sh
rosrun thor_arm_pick_place thor_arm_pick_place
```

### Probar obstaculos capturados por la camara
Abrir Rviz del Thor:
```sh
roslaunch thor_arm_new_moveit demo.launch
```
Obtener imagenes y guardarlo en un txt:
Seguir el repositorio: (https://github.com/Johguxo/generate_obstacles)

Instalar requeriments.txt en un nuevo workspace:
Correr:
```sh
python test/botellasCustomTest.py
```
Presionar Enter, cuando se tengan los obstaculos, otro enter si quieres colocar caracteristicas de los obstaculos en el txt.

Correr codigo de colocar obstaculos a partir del txt:
```sh
rosrun thor_arm_pick_place thor_arm_configuration_1
```
