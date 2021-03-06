CustomListing is a Magneto extension that allows you to add the following pages to your Magento store:

- Bestsellers
- All Products
- Specials
- Products By Attribute

Those pages can be added by creating a CMS page and inserting corresponding shortcode. Below are the codes for each page with usage instructions.

**Bestsellers**

	{{block type="custom_listing/bestsellers" name="my-bestsellers" template="catalog/product/list.phtml" column_count="3"}}

or

	<reference name="content">
        <block type="custom_listing/bestsellers" name="my-bestsellers" template="catalog/product/list.phtml">
            <action method="setColumnCount"><count>3</count></action>
        </block>
    </reference>

This block outputs all store products sorted by ordered quantity.

**All Products**

	{{block type="custom_listing/all" name="my-all-products" template="catalog/product/list.phtml" column_count="3"}}

or

	<reference name="content">
        <block type="custom_listing/all" name="my-all-products" template="catalog/product/list.phtml">
            <action method="setColumnCount"><count>3</count></action>
        </block>
    </reference>

This block outputs all products of the store.

**Specials**

	{{block type="custom_listing/specials" name="my_specials" template="catalog/product/list.phtml" column_count="3"}}

or

	<reference name="content">
        <block type="custom_listing/specials" name="my-specials" template="catalog/product/list.phtml">
            <action method="setColumnCount"><count>3</count></action>
        </block>
    </reference>

This block outputs all products that currently have discounts.

**Products By Attribute**

	{{block type="custom_listing/attribute" name="my-manufacturer" template="catalog/product/list.phtml" attribute_code="ATTRIBUTE_NAME" value="ATTRIBUTE_VALUE" column_count="3"}}

or

	<reference name="content">
        <block type="custom_listing/attribute" name="my-manufacturer" template="catalog/product/list.phtml">
            <action method="setAttributeCode"><code>ATTRIBUTE_NAME</code></action>
            <action method="setValue"><value>ATTRIBUTE_VALUE</value></action>
            <action method="setColumnCount"><count>3</count></action>
        </block>
    </reference>

This block outputs all products with specified attribute set to specified value. Replace ATTRIBUTE_NAME with name of your attribute and ATTRIBUTE_VALUE with value of your attribute if attribute type is text or ID of the value of your attribute if the attribute type is select. The example bellow will output all products by manufacturer with ID = 3.

	{{block type="custom_listing/attribute" name="my-manufacturer" template="catalog/product/list.phtml" attribute_code="manufacturer" value="3" column_count="3"}}

or

	<reference name="content">
        <block type="custom_listing/attribute" name="my-manufacturer" template="catalog/product/list.phtml">
            <action method="setAttributeCode"><code>manufacturer</code></action>
            <action method="setValue"><value>3</value></action>
            <action method="setColumnCount"><count>3</count></action>
        </block>
    </reference>
