## Bookstore!

This application was created with the following commands:

```bash
$ rails new bookstore --database=postgresql
$ cd bookstore/
```

Set your database configuration in `database.yml` file and the run the following commands:

```bash
$ rake db:create
$ rails g scaffold Book name:string author:string description:string slug:string
$ rails g scaffold User name:string email:string
$ rails g scaffold Comment book_id:integer user_id:integer description:string
$ rake db:migrate
```

After that Devise was incorpored:

- First the gem was included into the `Gemfile` 
- Then the following commands were runned:

```bash
$ rails g devise:install
$ rails g devise:views
$ rails g devise User
$ rake db:migrate
```

Finally run  `db:seed` to load some data

```bash
$ rake db:seed
```
