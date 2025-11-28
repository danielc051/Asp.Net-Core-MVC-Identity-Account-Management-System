
ASP.NET Core MVC project, with an authentication system using Asp.Net Core Identity scaffolded items. It includes the Account Registration and Account Login identities where users can input fields in the form for user profile management.

---
Overview of Project:

- Add New Scaffolded Items - Asp.Net Core Identity Library
  - Account\Registration
  - Account\Login
 
- Add Nuget Packages
  - Microsoft.AspNetCore.Identity.EntityFrameworkCore
  - Microsoft.AspNetCore.Identity.UI
  - Microsoft.Entity.FrameworkCore.Sqlserver
  - Microsoft.Entity.FrameworkCore.Tools
  
- Integrate SQL Database: DbContext class inherits from IdentityDbContext<IdentityUser>
  - AuthDbContext.cs
    - public class ApplicationDbContext : IdentityDbContext<IdentityUser>
  - Program.cs
    - builder.Services.AddDbContext<ApplicationDbContext>(options => options.UseSqlServer(connectionString));
  - appsettings.json
    - "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Database=AuthSystem;Trusted_Connection=True;MultipleActiveResultSets=true;" }
---

## Images of Account Management User Interface

### Account Login

<img src="AuthSystem/AuthSystem/wwwroot/images/AuthSystem-Account-Login.png" alt="Account Login" />

### Account Registation

<img src="AuthSystem/AuthSystem/wwwroot/images/AuthSystem-Account-Registration.png" alt="Account Login" />

### Account Management
<img src="AuthSystem/AuthSystem/wwwroot/images/AuthSystem-Manage-Account.png" alt="Account Login" />

