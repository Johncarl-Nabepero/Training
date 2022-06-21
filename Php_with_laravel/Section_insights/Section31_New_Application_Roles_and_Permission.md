## Section Insights

**Creating Migration**

**This is gonna be a pivot table the pivot can be relate the roles with the users**

```
PS C:\xampp\htdocs\new_cms> php artisan make:migration create_users_permission_table --create=permission_user
Created Migration: 2022_06_21_032613_create_users_permission_table

PS C:\xampp\htdocs\new_cms> php artisan make:migration create_users_roles_table --create=role_user 
Created Migration: 2022_06_21_032800_create_users_roles_table

PS C:\xampp\htdocs\new_cms> php artisan make:migration create_roles_permission_table --create=permission_role 
Created Migration: 2022_06_21_032922_create_roles_permission_table
```