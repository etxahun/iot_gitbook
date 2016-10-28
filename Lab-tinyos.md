# TinyOS

## Instalar TinyOS en Debian 7.x o Ubuntu 14.x

A continuación se describen los diferentes pasos a seguir:


1. Tell apt about the TinyProd Signing Key:

  >wget -O - http://tinyprod.net/repos/debian/tinyprod.key | sudo apt-key add -

2. Add the two new lines to /etc/apt/sources.list.d/tinyprod-debian.list:

  >sudo -s
  
  >cd /etc/apt/sources.list.d
  
  >echo "deb http://tinyprod.net/repos/debian wheezy main" >> tinyprod-debian.list
  
  >echo "deb http://tinyprod.net/repos/debian msp430-46 main" >> tinyprod-debian.list
  
3. Install the new packages:

  >sudo apt-get update
   
  >sudo apt-get install nesc tinyos-tools  
  
  Y si queremos, dependiendo de nuestro hardware:
  
  >sudo apt-get install msp430-46 avr-tinyos
  
4. Get the code from the TinyOS release repository:

  >wget http://github.com/tinyos/tinyos-release/archive/tinyos-2_1_2.tar.gz
  
  >tar xf tinyos-2_1_2.tar.gz  

5. You will need to add some environment variables to your shell. The following file includes the necessary ones. Substitute the placeholder with the path where you chose to place the code in the previous section (full path recommended):

		# Here we setup the environment
		# variables needed by the tinyos 
		# make system

		export TOSROOT="<local-tinyos-path>"
		export TOSDIR="$TOSROOT/tos"
		export CLASSPATH=$CLASSPATH:$TOSROOT/support/sdk/java
		export MAKERULES="$TOSROOT/support/make/Makerules"
		export PYTHONPATH=$PYTHONPATH:$TOSROOT/support/sdk/python

		echo "setting up TinyOS on source path $TOSROOT"

	Suppose you named this file tinyos.env. There are now at least two possibilities to have these variables accessible in your shell:
    
      1. Place it as root user in /etc/profile.d/
      2. Place it in <local-tinyos-path> and add the following line to your **.bashrc**:
			
  >source <local-tinyos-path>/tinyos.env`  
6. **UNINSTALL:** If you want to uninstall the packages you can do it like this:

  >sudo apt-get autoremove --purge nesc tinyos-tools msp430-46 avr-tinyos`

7. **ECLIPSE IDE:** Para instalar la última versión de Eclipse (Neon) tendremos que tener Java 1.8 como mínimo. Para ello:

    To install Java version 8 (OpenJDK 8 edition - not ORACLE Java 8) open a terminal and execute :

  >sudo add-apt-repository ppa:openjdk-r/ppa
  
  >sudo apt-get update
  
  >sudo apt-get install openjdk-8-jdk`

  **Intercambiar entre varias versiones:**

  Podemos tener ambas versiones instaladas a la vez, además de OpenJDK, para así hacer frente a las distintas situaciones en que nos podamos encontrar. 

  Para elegir cual versión de las instaladas queremos utilizar, ejecutamos:
  >sudo update-alternatives --config java

  **Establecimiento de variables de entorno de Java:**

  Para configurar automáticamente las variables de entorno Java 8, podemos instalar el siguiente paquete:
  >sudo apt-get install oracle-java8-set-default
  
  Si ya has instalado "oracle-java6-set-default" o "oracle-java7-set-default", se eliminan automáticamente al instalar "oracle-java8-set-default" y las variables de entorno se pueden establecer para Oracle Java 8 en su lugar .

  **Establecimiento de variables de entorno de Java:**

  Para configurar automáticamente las variables de entorno Java 8, podemos instalar el siguiente paquete:
  >sudo apt-get install oracle-java8-set-default
  
  Si ya has instalado "oracle-java6-set-default" o "oracle-java7-set-default", se eliminan automáticamente al instalar "oracle-java8-set-default" y las variables de entorno se pueden establecer para Oracle Java 8 en su lugar .

**Referencias:**

* http://askubuntu.com/questions/483916/installing-tinyos-on-recent-version-of-ubuntu
* http://tinyos.stanford.edu/tinyos-wiki/index.php/Automatic_installation
* http://tinyprod.net/repos/debian/
* http://askubuntu.com/questions/727065/updating-java-version-to-8-on-ubuntu

