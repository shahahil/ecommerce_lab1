
## Lab 3 : Adding image in a product




### Introduction

In this lab,We added image and quantiy in product module. We verify the database , table and records.

### Objectives

- To include image and quantity in product model.
- To learn more about how to create models and how models.py works 
 - To learn more about the admin.py, models.py, and other files provided by the Django framework 
 - To execute CRUD operations on all three models.

### Procedure

- **Enhance the admin for search enhancements in admin.py**

```
  admin.site.register(Product)

  class ProductAdmin(admin.ModelAdmin):
 list_display = ["name", "price", "brand", "category",]
 search_fields = ["name", "price", "brand__name", "category__name",]
 list_filter = ["brand","category",]
 readonly_fields = ["quantity",]
 
 class Meta:
 model = Product
admin.site.register(Product, ProductAdmin)
```

- **Finally, running the project and performing CRUD operations on Brand, Category and Product**

```
 python manage.py runserver
```
- **To display image in list view, first add a field “image_tag” to Product class in 
‘models.py’**

```
  ...
from django.utils.html import mark_safe
...
class Product(models.Model):
...
def image_tag(self):
return mark_safe(f'<img src="{self.image_url}" width="50" 
height="50" />')
image_tag.short_description = "Product"
def __str__(self):
return self.name
```
- **Let’s display image to list view. Go to 'admin.py' and modify the ProductAdmin as 
below:**

```
  class ProductAdmin(admin.ModelAdmin):
 list_display = ["image_tag", "name", "price", "brand", "category",]
 search_fields = ["name", "price", "brand__name", "category__name",]
 list_filter = ["brand","category","price",]
 # readonly_fields = ["quantity",]
 class Meta:
 model = Product
admin.site.register(Product, ProductAdmin)

```

- **Finally, running the project and performing CRUD operations on Brand, Category and Product**

```
 python manage.py runserver
```

### Outputs

- **Adding the qunatity in product module**

![](https://scontent.fktm3-1.fna.fbcdn.net/v/t1.15752-9/285409059_545202073923716_1990107548234487023_n.png?stp=dst-png_s350x350&_nc_cat=101&ccb=1-7&_nc_sid=aee45a&_nc_ohc=jdn_Qo_vx7UAX95H_6d&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.fktm3-1.fna&oh=03_AVLpAnu01hQhR2dwgDPQiN4O0LY-OVTwQF8AZ2gvmXr7Jw&oe=62C20B93)

- **Adding the image in the product module**

![](https://scontent.fktm3-1.fna.fbcdn.net/v/t1.15752-9/285768640_1220040992075177_4758745311887278860_n.png?stp=dst-png_p206x206&_nc_cat=104&ccb=1-7&_nc_sid=aee45a&_nc_ohc=bxknTjEw6rkAX9Qwmwo&_nc_ht=scontent.fktm3-1.fna&oh=03_AVKHPSOrKrCUoafO2sXniXc0rd6AvGbGwL64VFD12LBxAw&oe=62C25E5C)




### Conclusion
As a result, we added the image and quantity in Product models for our ecommerce site in our lab. Models are inherited by all three models. Model. 
