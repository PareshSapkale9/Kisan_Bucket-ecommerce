### Requirment :

1. JAR file of Spring Boot app
   - JAVA latest Version v18.0.2.1
2. Build of React app
   - apache 2
3. Database Structre
   - MySQL
4. EC2 Instance AWS
   - local to EC2

### Process :

Create EC2 instance

- basic os system setup requirement t2.micro

- Associate IP with EC2 instance to relase elastic ip (5 are free): for not changing ip address 0.0.0.0:8080/8081

On React

- Make the new _config.js_
- Copy paste ip address and paste in _config.js_ file for axios url

- Build React app :`npm run build`
  _yarn build_ : zip the folder static to .txt

On STS Springboot

- Build Springboot app (_JAR file_)
  Right click on project Run as _maven_ install or local terminal enter cmd : _mvn clean install_
  target folder _JAR_ gets created .zip
  [Also clear the all test case completed]

On Cmder app

- Open the cmder where _pem.key_ lies
- select the instance and connect the ec2 with _pem.key_ file resides
- fetch the link :
  _ssh -i "test-vm.pem" ubantu@ec2_ paste & enter.
  set fingerprint : yes

---

On Ubantu cmd Phase 1

    load up with cmd

    1. sudo apt-get update
    2. for MySQL: sudo apt install mysql-server
    3. for apache2: sudo apt-get install -y apache2
    4. for Java: sudo apt install openjdk-11-jre-headless
      *sudo apt install openjdk-8-jdk*
    5. for zip opener: sudo apt install unzip
    6. for git optional : sudo apt-get install git

On Git by cmder/local repo

- Create public repo for deployment _(git clone)_
- Copy all JAR , Zip & Sql file.

On MySQL for _Sql file_

- on database follow steps:

  1. server > data export
  2. select database > select _Export to self-contained file_ > start export

  - by the cmder
    `1.
sudo mysql
`
    `2.
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
`

- Create database _make sure name of the insert sql file is same_ , then >
  `use database `

On Ubantu cmd Phase 2

> 1.  goto homr dir `cd`
> 2.  `cd var/www/html`
> 3.  `ls`
> 4.  delete this default apache `index.html` :
>     `sudo rm -r index.html`

> 5.  Move to build file (React)
>     `sudo mv  git  repo folder` build.zip to current dir
> 6.  unzip it`sudo unzip build.zip`

> 7.  go home `cd\` and `ls`
> 8.  then `cd git repo` check `ls`
> 9.  hide out the java process
 `nohup java -jar server.jar`
 for springboot
`cat nohup.out` 

On Ubantu cmd Phase 3

> 1. Run a JAR file `jar -jar Ecommerce-Backend-0.0.1-SNAPSHOT.jar`

==Last==

- show the task manager `htop`
- select the process for kill ->Press F9
- on aws realease the elastic ip and terminate the instance of ec2 .
