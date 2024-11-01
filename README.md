<p align="center">
  <img src="https://github.com/itu-rover/iturover_obstacle_avoidance_assignment/assets/99661459/ac4adfa5-b237-4c0e-9f1e-56532de83b65" alt="iturover" width="300"/>
</p>
<p align="center">
</p>


# ITU Rover Keyboard Control Robot Assignment

Bu ödevde göreviniz python'da pynput kütüphanesini kullanarak klavyenizde basılan tuşları okumak ve klavyenizdeki w,a,s,d tuşlarını kullanarak Turtlebot simülasyonunda robotu aktif bir şekilde hareket ettirmektir.

<br>
<br>



<p align="center">
  <img src="https://github.com/itu-rover/iturover_obstacle_avoidance_assignment/assets/99661459/e3828def-fe18-4531-a2a4-796c0e6797b1" alt="harita" width="1200"/>
</p>
<p align="center">
  <em>Robotun hareketini gerçekleştireceği parkur</em>
</p>
<br>
<br>




/config/Screencast 2024-11-01 22:43:01.mp4





<br>
<br>



Ödevle ilgili daha fazla bilgiye ve yardımcı olacak kaynaklara aşağıdan ulaşabilirsiniz.

# Kurulum

Bir workspace oluşturun.

```
mkdir ~/rover_ws
cd ~/rover_ws
catkin_init_workspace
mkdir src
```

Bu paketi klonlayıp derleyin.

```
cd ~/rover_ws/src
git clone ----------------
cd ..
catkin build
```
İçerisinde launch dosyası olan yeni bir paket oluşturun.

```
cd ~/rover_ws/src
catkin_create_pkg reactive_robot std_msgs rospy geometry_msgs message_generation
cd reactive_robot
mkdir launch
```


# Kullanım

Turtlebot simülasyonunu kullanmak için gerekli paketleri kurun.

`
sudo apt install ros-noetic-turtlebot3-simulations
`

Gazebo ve RViz'i çalıştırmak için aşağıdaki komutu terminal yardımıyla çalıştırın.

`
roslaunch reactive_robot_sim reactive_robot_sim.launch
`


## İsterler ve Kısıtlamalar
<br>
<br>




* Robot klavyenin tuşları ile aktif bir şekilde hareket ettirilebiliyor olmalıdır.
* Robot harekete geçtikten sonra 60 saniye hareket etmelidir.
* 60 saniyelik sürenin sonunda robot hareketini sonlandırmalı ve node kapanmalıdır.
* Robotun hareketindeki değişimler _rospy.loginfo_ yardımıyla terminalde gösterilmelidir. Örneğin: _Started rotating left._ Her değişim için yapmayı unutmayınız.
* Node ile ilgili bilgiler _rospy.loginfo_ yardımıyla terminalde gösterilmelidir. Örneğin: _Time limit reached. Stopping..._
* Script'iniz ve simülasyon ortamı aynı anda launch dosyası yardımıyla çalıştırılmalıdır.
* Launch dosyasının ismi reactive_robot.launch_ olmalıdır.
* Kodunuz yorum satırlarıyla açıklanmalıdır.

<br>
<br>




# Ayrıca bakınız

* https://wiki.ros.org/ROS/Tutorials
* https://wiki.ros.org/Robots/TIAGo/Tutorials/motions/cmd_vel
