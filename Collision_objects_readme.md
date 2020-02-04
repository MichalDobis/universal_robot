# Collision objects stl/urdf

Do **~/catkin_ws/src/universal_robot/ur_e_description/meshes** som pridal priecinok **collision_objects**

Upraveny subor: **~/catkin_ws/src/universal_robot/ur_e_description/urdf/ur5e_robot.urdf.xacro**

kde je pridany include 

	  <!--Collision objects-->
	  <xacro:include filename="$(find ur_e_description)/urdf/collision_objects.xacro" />

Cize v subore: **~/catkin_ws/src/universal_robot/ur_e_description/urdf/collision_objects.xacro** su definovane vsetky kolizne objekty

# Moveit Config
Po kazdej zmene URDF odporucam pustit:
**roslaunch moveit_setup_assistant setup_assistant.launch**

1. Vybrat **Edit Existing MoveIt Configuration Package** a zvolit cestu k **/home/cocohrip/catkin_ws/src/universal_robot/ur5_e_moveit_config**
2. Zalozka **Self-Collision** - Nastavit **Sampling Density** na High a kliknut **Generate Collision Matrix**
3. Vyplnit zalozku **Author Information**
4. Zalozka **Configuration Files** - kliknut na **Generate Package**
5. spustit roslaunch ur5_e_moveit_config demo.launch a skontroval ci sa pocita kolizia s novym objektom

