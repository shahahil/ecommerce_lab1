
## Lab 2 : Adding Brand, Category and Product




### Introduction

In this lab,We constructed a product module. Now we'll add a brand, a product, and a category to the product module, which follows the following diagram structure:

![Er diagram, the product module](https://scontent.fktm3-1.fna.fbcdn.net/v/t1.15752-9/285961942_572298934250985_7888553134652948235_n.png?stp=dst-png_p206x206&_nc_cat=100&ccb=1-7&_nc_sid=aee45a&_nc_ohc=WgUp0p4hx6YAX-QSRz2&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.fktm3-1.fna&oh=03_AVLyTKVY33L0u29xZ_T-YqtBcWzNU-SRxmvPC2cFeNu6Eg&oe=62C3A3AB)
### Objectives

- To include models for products, brands, and categories.
- To learn more about how to create models and how models.py works 
 - To learn more about the admin.py, models.py, and other files provided by the Django framework 
 - To execute CRUD operations on all three models

### Procedure

- **Adding the model Brand in the models.py**

```
  class Brand(models.Model):
    name = models.CharField(max_length=200)
    is_active = models.BooleanField()
```
- **Adding the model Category in the models.py**

```
  class Category(models.Model):
    name = models.CharField(max_length=200)
    is_active = models.BooleanField()
  class Meta:
    verbose_name_plural = "Categories"
```
- **Adding the model Product in the models.py**

```
  class Product(models.Model):
    name = models.CharField(max_length=200)
    price = models.FloatField()
    quantity = models.IntegerField()
    image_url = models.CharField(max_length=500)
    color_code = models.CharField(max_length=20)
    brand = models.ForeignKey(Brand, on_delete=models.CASCADE)
    category = models.ForeignKey(Category, on_delete=models.CASCADE)
    registered_on = models.DateTimeField()
    is_active = models.BooleanField()
```
- **Making changes to the db by performing migrations**

```
  python manage.py makemigrations
  python manage.py migrate
```
- **Adding the following code to admin.py for enabling CRUD operations in the admin site**

```
  from .models import Brand, Category, Product
  admin.site.register(Brand)
  admin.site.register(Category)
  admin.site.register(Product)
```

- **Finally, running the project and performing CRUD operations on Brand, Category and Product**

```
 python manage.py runserver
```

### Outputs

- **Adding the models Brand, Category and Product**

![](https://scontent.fktm3-1.fna.fbcdn.net/v/t1.15752-9/286075453_4900252943436290_8366396888011893027_n.png?stp=dst-png_p206x206&_nc_cat=106&ccb=1-7&_nc_sid=aee45a&_nc_ohc=YzcpAK9lOeMAX-FsWCi&_nc_oc=AQk8JOVqp7I87z8DM5zPr7OkvV7v3S-rgzfLXfXSAPUZUyHG4ImTsa_Ijpha9RleNatuBtizuIVb6LwOGAlr8Jat&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.fktm3-1.fna&oh=03_AVIo6oZ5BgmqokYUopQSpheJCJLajmeuhA5Qcy2q336WFQ&oe=62C2FCB2)

- **The Brand model**

![](https://scontent.fktm3-1.fna.fbcdn.net/v/t1.15752-9/285062099_546984270264834_7721264771442810466_n.png?stp=dst-png_s526x296&_nc_cat=108&ccb=1-7&_nc_sid=aee45a&_nc_ohc=tUxskWp9QuMAX8Egp2C&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.fktm3-1.fna&oh=03_AVKrmQXcVwbW5rXQnuOpFV2tyD83QMaZvRwS_97Qz74LcQ&oe=62C230E2)


- **The Category model**

![](https://scontent.fktm3-1.fna.fbcdn.net/v/t1.15752-9/285243843_709451920307452_5056620266487673530_n.png?stp=dst-png_p206x206&_nc_cat=105&ccb=1-7&_nc_sid=aee45a&_nc_ohc=git5HdanUrYAX8bUM3q&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.fktm3-1.fna&oh=03_AVJPzCYB5sK_4EXkIilhCE4KUM3zoJLbKmTkDUl7QBg6qA&oe=62C3B870)


- **The Product model**

![](https://scontent.fktm3-1.fna.fbcdn.net/v/t1.15752-9/285768640_1220040992075177_4758745311887278860_n.png?stp=dst-png_p206x206&_nc_cat=104&ccb=1-7&_nc_sid=aee45a&_nc_ohc=bxknTjEw6rkAX9Qwmwo&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.fktm3-1.fna&oh=03_AVLjga9wKyLGWC8d91IfgsfRLZmTmiClYzRZkVHafYMrrg&oe=62C25E5C)


### Conclusion
As a result, we constructed the Brand, Category, and Product models for our ecommerce site in our lab. Models are inherited by all three models. Model. The product and brand, as well as the category model, are linked by a one-to-many connection. We've also made advantage of django's many data kinds.
