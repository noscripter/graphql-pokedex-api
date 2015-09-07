#  查询pokemon信息

`curl -XPOST -H"Content-Type:application/graphql" -d"{pokemon{name, type, stage, species}}" localhost:3001/graphql | python -m json.tool`
