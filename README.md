# penta-world-gazebo
A little world created using gazebo simulator, with self-created and imported models and plugins.

### Requirements:

The project was made using Gazebo7. You can install it by visiting the [Gazebo Installation Page](http://gazebosim.org/tutorials?tut=install_ubuntu&ver=7.0).

### Directory Structure:
```bash
.
├── CMakeLists.txt
├── images
│   └── PentaWorld.jpg
├── model
│   ├── PentaBuilding
│   │   ├── model.config
│   │   └── model.sdf
│   └── ServiceBot
│       ├── model.config
│       └── model.sdf
├── README.md
├── script
│   ├── hello.cpp
│   └── model_push.cc
└── world
    └── AmanWorld
```

### Running the simulation:

#### Update and upgrade packages:
```bash
$ sudo apt update && sudo apt upgrade
```

#### Clone the repo on your system after changing to your preferred installation directory, then navigate to our cloned directory:
```bash
$ git clone https://github.com/amanarora9848/penta-world-gazebo.git
$ cd penta-world-gazebo
```

#### First, we need to compile our code. Follow the following steps to compile it.
```bash
$ mkdir build
$ cd build/
$ cmake ../
$ make
```
The c++ script files are located in the `scripts` directory inside of our cloned directory `penta-world-gazebo`.

#### Run this and copy the directory path
```bash
$ pwd
```
Let's say it is: `/home/user/penta-world-gazebo/build`

#### Navigate back to our main directory `penta-world-gazebo`:
```bash
$ cd ../
```

#### Add the library path to the Gazebo plugin path
```bash
$ export GAZEBO_PLUGI_PATH=${GAEBO_PLUGIN_PATH}:/home/user/penta-world-gazebo/build
```

#### Run the Gazebo world file.
```bash
$ gazebo world/AmanWorld
```

#### If everything works fine, you should see something like the image which exists in the `images` folder.