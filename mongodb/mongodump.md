# mongodump

## Version 2.x
2.4 after?.

### milliseconds

#### Debian/Ubuntu

    $ date -d "2015-06-10 0:00:00+0900" +%s000

#### mac.
    
     $ date -jf '%Y-%m-%dT%H:%M:%S%z' '2015-06-10T0:00:00+0900' +%s000
    
or

     $ date -jf "%Y-%m-%d %H:%M:%S%z" "2015-06-15 04:02:12+0900"


### Go dump!
    
     $ mongodump -h host_name -d db_name -c collection_name -q '{created: {$gte: new Date(1433862000000), $lte: new Date(1433905200000)}}'


## Version 3.x

    ISODateとかも使える
