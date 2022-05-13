## Objective:
*   Create a super user and users, as well as run the server.
*  To test CRUD operations and add components.
*  To prepared an environment to run and compile the project.
## Introduction:
* In this lab, we implement a frameworks and platforms. The IDE was Visual Studio Code, and the framework was Python/Django. An e-commerce website is one that allows users and sellers to buy and sell things over the internet. It is one of the most effective current company models. E-commerce platforms make purchasing products and services easier. For this lab report, we will create an e-commerce website.
 We may also utilize Github Desktop to commit and push our work to a GitHub repository. 
## Procedure:
1.  We Download<br/> Python3, pip or pip3, Sqlite, DBeaver community, Django, VS code, Github account.
2.  Open command use to check whether python is install or not.
Syntax:
<br/>Syntax:<br/>
 python3 –version
3.  Initialize Django project to create the user 
Syntax:
django-admin startproject ecommerce_shahil
<br/>Syntax:<br/>
django-admin startproject ecommerce_ashna <br/>
cd ecommerce_shahil
4.  Migrating and creating users
Syntax:
 ecommerce_shahil
<br/>Syntax:<br/>
 ecommerce_shahil<br/>
python manage.py migrate
in this process we got link for server for 127.0.0.1:8000
5.  Verify the admin side using 127.0.0.1:8000\admin
Syntax:
<br/>Syntax:<br/>
python manage.py runserver
6.  Database verification and CRUD operations:
Syntax:
python manage.py startapp product_module
<br/>Syntax:<br/>
python manage.py startapp product_module<br/>
python manage.py runserver
7.  Source Control
Lastly, for source control, we utilized Git. We built a repository called ecommerce ashna and a markdown file called "lab1.md" that contains this document. The code and folder were then committed and published to the repository. The repository may now be found at: https://github.com/shahahil/ecommerce_shahil
36
## Output:
* Installation of python| pip

![alt text](https://scontent.fktm8-1.fna.fbcdn.net/v/t1.15752-9/278162363_535159071348207_4631905168955827836_n.png?_nc_cat=107&ccb=1-6&_nc_sid=ae9488&_nc_ohc=yVxHf-Jgq8IAX-4bR_m&_nc_ht=scontent.fktm8-1.fna&oh=03_AVJh5Rac7ep52PMV0rYftEwHz-YYWPPDdPCyzeWP111euA&oe=62A15D25)

* Creation of project folder

![alt text](https://scontent.xx.fbcdn.net/v/t1.15752-9/278983753_575745483766427_3748886200780575028_n.png?stp=dst-png_s526x296&_nc_cat=104&ccb=1-6&_nc_sid=aee45a&_nc_ohc=crOliPYXH4QAX-UZGTF&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.xx&oh=03_AVLDTXlmwggANY1i26kzN9dIMHjD-rC4F6bBEuuv8N_Z9w&oe=62A3D35B)

* Migration and creating super user:
 
![alt text](https://scontent.xx.fbcdn.net/v/t1.15752-9/278176476_1451288888674246_77467148134497754_n.png?stp=dst-png_p206x206&_nc_cat=101&ccb=1-6&_nc_sid=aee45a&_nc_ohc=JX4n2BLtw60AX9dOend&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.xx&oh=03_AVLwT9hUn38Bc0ASGpCGCdqYAoDmBiNISiLJ6Lv2DdBIQQ&oe=62A48A55)

* Running server

 ![alt text](https://scontent.xx.fbcdn.net/v/t1.15752-9/280326100_374482437946718_5000888598667940158_n.png?stp=dst-png_p206x206&_nc_cat=103&ccb=1-6&_nc_sid=aee45a&_nc_ohc=J_7vBdcCeOkAX8ie2E9&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.xx&oh=03_AVJB-2rzl4-_NJuXC8rduzdVArOz4RCU_TOCgo1d1bKohQ&oe=62A57134)

* Logging In

 ![alt text](https://scontent.xx.fbcdn.net/v/t1.15752-9/280100316_1003713720281266_8116799199405200024_n.png?stp=dst-png_p206x206&_nc_cat=110&ccb=1-6&_nc_sid=aee45a&_nc_ohc=UoCtO5jCiLMAX-lzpmU&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.xx&oh=03_AVI7V0C15LLKboKxyO1enPerH_2DFjyZ9xC9ggzImibihw&oe=62A38007)

* CRUD operation

![alt text](https://scontent.xx.fbcdn.net/v/t1.15752-9/280074081_5301103239910089_4016633097419564794_n.png?stp=dst-png_p206x206&_nc_cat=111&ccb=1-6&_nc_sid=aee45a&_nc_ohc=TORX6hhZPFgAX_OO-ju&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.xx&oh=03_AVJAqtsFrisVwL470AZJ1T2OXC_hkrksIDi20PSocdfm7g&oe=62A5B402)
 

## Conclusion:
In this lab we setup allowed us in quickly creating scenarios and setting up. Then we knew how to create a Django project.On the server, we knew how to do CRUD operations. Finally, we learned more about Git and Github for source control. 
