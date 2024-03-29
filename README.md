Build a device database application with libAlmondDBM which should do the following actions. libAlmondDBM is a library that will store the data as key-value pairs.

It should give options to the user to add, edit and delete devices as well as an option to delete all devices. 

For each device,

it should store the metadata structure with the device id as the key.

it should store the list of its values like temperature, humidity, fire state, etc. as a "device value pair" structure. The key for each of these values is "<deviceID>.<indexID>", for example, "2.1" where 2 is device id and the 1 represents that the value is of the first index.

The example metadata structures and device value pair structure are presented below. Feel free to modify them if they are not sufficient for the requirement.

struct deviceData {

    int id;

    int deviceType; //define some enumerations

    char name[32];

    char location[32];

    char manufacturer[32];

    int lastModifiedTime;

}

struct dvPair {

    int type;

    int id; // to indicate the dvPair number

    char value[32];
