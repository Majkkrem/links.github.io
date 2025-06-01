# links.github.io

## Backend links:

Backend projekt [Node.js keretprojekt](https://github.com/hgabor/nestjs-keret-2024)

Seeding example [Prisma Seeding](https://www.prisma.io/docs/orm/prisma-migrate/workflows/seeding)

Prisma Schema [Prisma Schema Example](https://www.prisma.io/docs/orm/prisma-schema/data-model/models)

Faker doksi [Faker](https://www.npmjs.com/package/@faker-js/faker)


```
npx prisma db push
npx nest generate resource
npm install --save-dev @faker-js/faker
```

## Frontend links

Bootstrap doksi [Bootstrap](https://getbootstrap.com/docs/5.3/getting-started/introduction/)

useEffect doksi [useEffect](https://scrimba.com/links/react-docs-useeffect)

useState doksi [useState](https://react.dev/reference/react/useState)


## C# links

```
using var conn = new MySql.Data.MySqlClient.MySqlConnection("server=localhost;uid=root;;database=test");
```

Database [Database connection](https://dev.mysql.com/doc/connector-net/en/connector-net-connections-string.html)

Console output [STAThread](https://ikriv.com/blog/?p=2470)

Deletion:
```
var selectedItem = dataGrid.SelectedItem as Class;

using var conn = new MySql.Data.MySqlClient.MySqlConnection("server=localhost;uid=root;database=db");
conn.Open();
var cmd = conn.CreateCommand();
cmd.CommandText = "DELETE FROM db WHERE id: @id";
cmd.Parameters.AddWithValue("@id", selectedMember.Id);
statisztika.Members.Remove(selectedItem);
cmd.ExecuteNonQuery();

dataGrid.ItemsSource = statisztika.item;
```







