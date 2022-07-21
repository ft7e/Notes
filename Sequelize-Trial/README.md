# Sequelize Relations

## One to One from one side :

_Here we assume we have 2 tables, Country and Capital_

Country.hasOne(Capital)

- We can also add options to the foreignKey column :

`Country.hasOne(Capital, foreignKey : { name : countryId, type : DataTypes.INTEGER }`

- another option to delete the record in both tables if one was deleted :
  `Country.hasOne(Capital, {onDelete : 'CASCADE')`
- can also use onUpdate

### Connection when we create a record :

`country = Country.create(params)`
`country.createCapital(params)`

### Connection when a record already exists :

1- find the parent
2- find the child
3- connect parent to child

` country = Country.findOne()`
` capital = Capital.findOne()`
` country.setCapital(capital)`

### If the tables are already connected :

find the country then use getCapital

`country = Country.findOne()`
`country.getCapital`

_This will return the capital record with the forgen key_

### To connect capital to country back :

` Capital.belongsTo(Country)`

**typing that will make things starts to work the other way around :**

`capital.setCountry(country)`
