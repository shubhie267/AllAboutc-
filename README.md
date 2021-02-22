# AllAboutCSharp

### Razor Pages : 
- Razor Pages is a newer, simplified web application programming model.
- file-based routing approach.
- Each Razor Pages file found under the Pages directory equates to an endpoint.
- Additionally, each page works on the limited semantics of HTML, only supporting GET and POST methods.

It has 2 parts -
1. Razor Pge(UI/View)
2. Page Model(contain handlers - controller methods)


#### STEP 1 -- 

Nuget packages installed in visual studio 2019 : 4 packages should be there

1. microsoft.entityframeworkcore
2. microsoft.entityframeworkcore.sqlserver
3. microsoft.entityframeworkcore.tools - (for migration)
4. microsoft.ASPnetcore.mvc.razor.RuntimeCompilation


#### STEP 2 --

In startup.cs ----
change :
services.AddRazorPages()  to   services.AddRazorPages().AddRazorRuntimeCompilation(); 
// so that whatever changes you make in the code are seen just after refresh and you dont have to build the solution again and again. :)

#### STEP 3 --
make folder - Model - inside this make class - named book.cs

#### STEP 4 --
 go to appsettings.json --
 add this connection string
 
 {
  "ConnectionStrings": {
    "DefaultConnection": "Server=(LocalDB)\\MSSQLLocalDB;Database=BookListRazor;Trusted_Connection=True;MultipleActiveResultSets=True"
  }
}

#### STEP 5 --

open SSMS then connect with LocalDB -

#### TSEP 6 --

add class in Model - ApplicationDBContext // comment // which gets inherited from DBContext



