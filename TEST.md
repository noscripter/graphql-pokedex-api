#  查询pokemon信息

>  注意这里的单引号和双引号
>  pay attention to single quotes and double quotes

## query
`curl -XPOST -H"Content-Type:application/graphql" -d"{pokemon{name, type, stage, species}}" localhost:3001/graphql | python -m json.tool | less`

## query with argument
`curl -XPOST -H'Content-Type:application/graphql' -d'{user(name:"test1"){name,caught,created}}' http://localhost:3001/graphql`

## mutation
`curl -XPOST -H'Content-Type:application/graphql' -d'mutation Mutation{upsertUser(name:"newUser"){name,caught,created}}' http://localhost:3001/graphql`

## mutation with many arguments
`curl -XPOST -H'Content-Type:application/graphql' -d'mutation Mutation{caughtPokemon(name:"newUser", pokemon: "Snorlax"){name,caught,created}}' http://localhost:3001/graphq`

# mongodb query

`show dbs`                          # show all databases;
`use pokedex`                       # use database pokedex
`db`                                # show current database;
`show tables`                       # show all collections in current database;  equivalent to `show collections`
`db.users.find()`                   # select all rows from collection usres
`db.users.remove({name:"david"})`   # delete from collection users where name equals david
`db.users.insert({name:"newUser"})` # insert into collection users with values name equals newUser

## more on mongodb

<http://www.tutorialspoint.com/mongodb/>
