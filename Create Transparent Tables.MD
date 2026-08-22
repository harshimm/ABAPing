# INITIAL SETUP :

1. Open tcode SE11
2. Enter table name 
3. Click create
4. Enter table description in Short Text
5. Go to delivery and maintenance tab
6. Choose Delivery Class 'A'
7. Data Browser/Table view editing as 'Display / maintenence allowed' 
8. Save the changes
9. In the following popup select 'Local Object' as we are not moving the table to any other SAP environment
10. Save the inputs.
11. Table is saved.
12. Click 'Go To'.
13. Select Object Directory Entry.
14. The Delivery Class in the popup shows $TMP as we chose to create a local object.

# DEFINING FIELDS :

1. Go to 'Fields' tab.
2. Enter field names.
3. Define 'Initital Values' for the field if necessary. It is a default value that can also be changed later while making entries in the table.
4. Define a key field, there can be only one key field. Key field is used to uniquely identify an entry and to sort fields.
5. Define data element.
6. After below steps the data element attributes will be reflecting in the main field entry screen.
7. Save the table and activate it.

## DATA ELEMENT

1. Each field has a data element.
2. Data elment defines the attributes of the field e.g : Data type, Length, decimal, short text
3. Enter a custom data element in the 'Data element' field.
4. Double click on the data element to define it's properties.
5. Define the Domain. This can have the same name as the Data Element.
6. Define the data type.
7. Define the type of values it can have (single values, interval range, value table [if large number of values] )
8. Define the short, medium, long text and header.
9. Save the data element and activate it.

## TECHNICAL SETTINGS

1. Click on 'Techinical Settings'.
2. Choose Data Category
3. Choose Size Class
4. Choose Buffering not allowed
5. Save table and activate it.





