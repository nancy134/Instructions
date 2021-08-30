# How to do a one-to-many relationship with sequelize

This example will use Users and Clients table where a User has many Clients

## Modify client table migration (migrations/0013-create-client.js)

Add UserId as foreign key in Clients table

```
            UserId: {
                type: Sequelize.INTEGER,
                allowNull: false,
                references: {
                    model: 'Users,
                    key: 'id'
                }
            },
```

## Add hasMany association in User model (models/user.js)

Add an association in the User model (see models/association.js as an example)
```
    User.associate = function(models){
        User.hasMany(models.Client, {as: 'clients'});
    };
```
## Client model (ie, models/client.js)

Add an association in the Clietn model (see models/user.js as an example)
```
    Client.associate = function(models){
        Client.belongsTo(models.User, {as: 'user', foreignKey: 'UserId'});
    };
```
