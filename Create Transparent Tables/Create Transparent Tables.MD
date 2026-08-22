# ⚙️ INITIAL SETUP

- Open tcode SE11
- Enter table name 
- Click create
- Enter table description in Short Text
- Go to delivery and maintenance tab
- Choose Delivery Class 'A'
- Data Browser/Table view editing as 'Display / Maintenance allowed' 
- Save the changes
- In the following popup select 'Local Object' as we are not moving the table to any other SAP environment
- Save the inputs.
- Table is saved.
- Click 'Go To'.
- Select Object Directory Entry.
- The Delivery Class in the popup shows $TMP as we chose to create a local object.

# ✍️ DEFINING FIELDS 

- Go to 'Fields' tab.
- Enter field names.
- Define 'Initial Values' for the field if necessary. It is a default value that can also be changed later while making entries in the table.
- Define a key field, there can be only one key field. Key field is used to uniquely identify an entry and to sort fields.
- Define data element.
- After below steps the data element attributes will be reflecting in the main field entry screen.
- Save the table and activate it.

## 🗒️ DATA ELEMENT

- Each field has a data element.
- Data element defines the attributes of the field e.g : Data type, Length, decimal, short text
- Enter a custom data element in the 'Data element' field.
- Double click on the data element to define it's properties.
- Define the Domain. This can have the same name as the Data Element.
- Define the data type.
- Define the type of values it can have (single values, interval range, value table [if large number of values] )
- Define the short, medium, long text and header.
- Save the data element and activate it.

## 🔨 TECHNICAL SETTINGS

- Go back to table
- Click on 'Technical Settings'.
- Choose Data Category
- Choose Size Class
- Choose Buffering not allowed
- Save table and activate it.





