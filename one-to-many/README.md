# How to do a one-to-many relationship with sequelize

This example will use Users and Clients table where a User has many Clients

## Client migration

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

## User model (ie, models/user.js)

Add an association in the User model
```
    User.associate = function(models){
        User.hasMany(models.Client, {as: 'clients'});
    };
```
## Client model (ie, models/client.js)

Add an association in the Clietn model
```
    Client.associate = function(models){
        Client.belongsTo(models.User, {as: 'user', foreignKey: 'UserId'});
    };
```
