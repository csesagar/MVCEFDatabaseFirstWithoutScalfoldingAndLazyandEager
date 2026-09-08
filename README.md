Default loading is lazy loading only and if we want to use eager loading then we need to first set
“<DbContextClass>.Configuration.LazyLoadingEnabled = false”, and the above code should be replaced as below:
dc.Configuration.LazyLoadingEnabled = false;
var Emps = dc.Employees.Where(E => E.Status == true).Include(E => E.Department);
