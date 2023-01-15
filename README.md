# Factory Manager

#### By _**Hans Ellis**_

## \____________________

## Technologies Used

- _C#_
- _Entity Framework Core_
- _.NET 6.0 SDK_
- _Asp.Net Core MVC rendering_
- _Linq_

## Description

Dr Sillystrigz factory is an application that allows the factory owner to manage relationships between Machines and Engineers licensed to work on them. This is handled through a many-to-many relationship between the two, made possible by the use of a join table. A license can be added to an engineer and a licensed engineer can be added to a machine. Machines and engineers can be added seperately from eachother and validation ensures that no object can be added with an empty "name" field.

## Setup/Installation Requirements

### Set up mySQL database:
- Follow [these steps from LearnHowToProgram.com](https://www.learnhowtoprogram.com/c-and-net/getting-started-with-c/installing-and-configuring-mysql) to install both MySQL Server **8.0.19** and MySQL Workbench.
- Ensure the MySQL server is running by opening Terminal or Windows Powershell and entereng the command ```mysql -uroot -pepicodus```
- If you set up MySQL Server with a different username and/or password, the command will be ```mysql -u[YourUserName] -p[YourPassword]``` (omit square brackets).

### Importing ```hans_ellis.sql``` (the included database .sql file):

1. Open MySQL Workbench.
2. In the Navigator > Administration window, selet Data Import/Restore.
3. In Import Opitons select "Import from Self-Contained File."
4. Navigate to ```hans-ellis.sql```.
5 Under Default Schema to be Imported To, select "New" button.
6. Enter the name of the database.
    - in this case ```hans_ellis.sql```.
7. Click "Ok"
8. Click "Start Import."
9 Reopen the Navigator > Schemas tab. Right click and select Refresh All. _The new database will appear._

## Running the Program.

1. Clone the repository: [https://github.com/mrhansellis/hair-salon](https://github.com/mrhansellis/hair-salon)
2. Navigate to the hair-salon/ directory on your computer
3. Using your preferred terminal navigate to the ```hair-salon/``` directory on your computer. Proceed to the directory titled ```HairSalon/```.
4. Run the command ```touch appsettings.json```. Open the newly created "appsettings.json" file and add the following code to that file.

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Port=3306;database=hans_ellis;uid=[YourUserName];pwd=[YourPassword];",
    "TestConnection": "Server=localhost;Port=3306;hans_ellis;uid=[YourUserName];[YourPassword];"
  }
}
```
_Note: make sure to [YourPassword] and [YourPassword] match the ones you are using for your database on your local MySQL server (be sure to omit the square brackets)._

5. 
6. Enter the command "dotnet restore" in the terminal.
7. Enter the command "dotnet build" in the terminal.
8. Enter the command "dotnet watch run" in the terminal.


## Known Bugs

- No know bugs at this time. If any are found please reach out to me.

## Link to GH Pages:

n/a

## License

MIT License

Copyright (c) [2022] [Hans Ellis]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.