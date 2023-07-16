# Entity Framework Core
Entity Framework Core (EF Core) is a lightweight and cross-platform version of the Entity Framework data access technology. It serves as an object-relational mapper (O/RM), allowing .NET developers to work with databases using .NET objects and reducing the need for manual data-access code. EF Core supports various database engines and provides flexibility in model development approaches.

With EF Core, data access is performed through a model consisting of entity classes and a context object that represents a session with the database. LINQ is used for querying data, and changes to the database are made by manipulating instances of entity classes. Best practices such as understanding the underlying database server, testing, performance optimization, security review, logging, error recovery, and migration planning should be considered when using EF Core in production applications.


## Entity Framework Core provides multiple ways to seed data into a database:

- Model Seed Data: EF Core allows associating seed data with entity types as part of the model configuration. This data can be automatically applied during migrations, ensuring consistency between the model and the database. However, there are limitations such as the need to specify primary key values and potential data removal when primary keys change.

- Manual Migration Customization: By manually customizing the migrations, you can work around the limitations of model seed data. You can use methods like InsertData(), UpdateData(), and DeleteData() to manipulate the data during migrations according to your specific requirements.

- Custom Initialization Logic: Another approach is to manually seed data using the SaveChanges() method of the DbContext before the main application logic begins execution. This gives you more control over the seeding process, allowing conditional checks and custom transformations. However, it's important to execute the initialization code separately from the normal app execution and ensure proper permissions for modifying the database schema.
# User Secrets
user Secrets in .NET Core is a secure and convenient way to store private user information, such as API keys and connection strings, locally on your development machine. By using User Secrets, sensitive data is kept separate from your source control and remains confidential.

Enabling User Secrets involves adding a secrets.json file to your project, which contains key/value pairs of your secret information. This file is not uploaded to source control but is stored securely on your local machine.

To access User Secrets within your code, you need to configure the project to use the secrets.json file. This is done by modifying your .csproj file and adding the UserSecretsId and DotNetCliToolReference.

In your controllers or other parts of your code, you can access the secrets using the Configuration API provided by .NET Core. Inject the IConfiguration object into your controller's constructor and use Configuration["KEY"] to retrieve the secret values.

When deploying to Azure, you can add the user secret data as environment variables in the application settings of your Azure App Service, ensuring that the secrets are securely stored in the production environment.


## Things I  want to know more about it 

Dive deeper into API Designing . 
[Home](./README.md)  