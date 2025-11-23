# Как пользоваться Кубиком в вашем мире Gazebo 
1. Распаковать содержимое архива dice.tar.gz в папку ~/catkin_ws/src/clover/clover_simulation/models/
2. В файле ~/catkin_ws/src/clover/clover_simulation/resourses/worlds/clover_aruco.world добавить еще одну секцию <include>
```
   <include>
      <uri>model://dice</uri>
      <pose>1 1 1 0 0 0</pose>
    </include>
```
>[!NOTE]
> Позицию Кубика можно изменить в теге \<pose\>x y z roll pith yaw\</pose\> и покрутить его тут же

3. В файле ~/catkin_ws/src/clover/clover_simulation/launch/simulator.launch поменяйте систему визуального позиционирования на LPE
```
    <arg name="est" default="lpe"/> <!-- PX4 estimator: lpe, ekf2 -->
```
4. Либо замените файлы настроек приложенными образцами по указанным местам.
5. После запуска нового мира должно "взлететь". Успехов в ваших полетах!
