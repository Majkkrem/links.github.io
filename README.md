# links.github.io

## Backend links:

Backend projekt [Node.js keretprojekt](https://github.com/hgabor/nestjs-keret-2024)

Seeding example [Prisma Seeding](https://www.prisma.io/docs/orm/prisma-migrate/workflows/seeding)

Prisma Schema [Prisma Schema Example](https://www.prisma.io/docs/orm/prisma-schema/data-model/models)

Faker doksi [Faker](https://www.npmjs.com/package/@faker-js/faker)

Service-ts [db.service.ts example](https://taylor-reis.com/blog/building-a-nestjs-crud-app:-part-1/?utm_source=chatgpt.com)


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


Database [Database connection](https://dev.mysql.com/doc/connector-net/en/connector-net-connections-string.html)

Console output [STAThread](https://ikriv.com/blog/?p=2470)



```
import {env} from "../environtment.ts";
import type {Icar} from "../models/car.interface";
import type {Irental} from "../models/rental.interface"
import type { IcarCreate } from "../models/carCreate.interface.ts";

export  class HttpRequests{
    static async getCarData(endpoint: string){
        const response = await fetch(`${env.LOCAL_API_URL}${endpoint}`,{
            method:"GET",
            headers: {
                'Content-Type': 'application/json; charset=UTF-8',
                'Accept':'application/json'
            }
        })

        if(!response.ok){
            throw new Error("Couldn't load data")
        }
        else{
            const result: Icar[] = await response.json();
            return result;
        }
    }

    static async createCar(endpoint: string, data: IcarCreate){
        const response = await fetch(`${env.LOCAL_API_URL}${endpoint}`, {
            method:"POST",
            headers:{
                'Content-Type': 'application/json; charset=UTF-8',
                'Accept':'application/json'
            },
            body: JSON.stringify(data)
        });
        if (!response.ok){
            const result = await response.json()
            throw new Error(result.message || "Error creating entry")
        }else{
            return await response.json();
        }
    }

    static async rentCar(endpoint: string, id: number){
        const response = await fetch(`${env.LOCAL_API_URL}${endpoint}/${id}/rent`, {
            method:"POST",
            headers:{
                'Content-Type': 'application/json; charset=UTF-8',
                'Accept':'application/json'
            },
        })
        if (!response.ok){
            const result = await response.json()
            throw new Error(result.message || "Error renting entry")
        }else{
            return await response.json();
        }
    }
}

```








