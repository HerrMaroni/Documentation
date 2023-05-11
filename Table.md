# HTML Tables

| Question | Answer |
| :---  | :--- |
| What are tables in HTML used for?  | Tables in HTML are used to organize and display tabular data in rows and columns. They provide a way to present data in a structured format, making it easier for users to comprehend and compare information.  |
| How do we create a table in HTML?  | To create a table, we use the `<table>` element. This element serves as the container for the entire table. Inside the `<table>` element, we use other tags to define the structure of the table, such as rows, columns, and cell data.  |
| How do we define the rows and columns of a table?  | We use two main tags to define the structure of a table: `<tr>` and `<td>`. The `<tr>` tag represents a table row, and it contains one or more `<td>` tags, which represent table cells. Each `<td>` tag defines a single cell within a row.  |

<table>
	<tr>
		<td>

```html
<table>
    <tr>
        <td>Cell 1</td>
        <td>Cell 2</td>
    </tr>
    <tr>
        <td>Cell 3</td>
        <td>Cell 4</td>
    </tr>
    <tr>
        <td>Cell 5</td>
        <td>Cell 6</td>
    </tr>
</table>
```

</td>
		<td>
			<picture>
				<img alt="First example" src="https://raw.githubusercontent.com/HerrMaroni/Documentation/main/E1.png">
			</picture>
		</td>
	</tr>
</table>

| Can we have table headers in our table?  | Yes, we can include headers in our table. HTML provides a specific tag for this called `<th>`. The `<th>` tag is similar to the `<td>` tag, but it is used to define table headers instead of regular data cells. Typically, table headers are placed in the first row or column of the table.  |
| :---  | :--- |


<table>
	<tr>
		<td>

```html
<table>
    <tr>
        <th>Header 1</th>
        <th>Header 2</th>
    </tr>
    <tr>
        <td>Cell 1</td>
        <td>Cell 2</td>
    </tr>
    <tr>
        <td>Cell 3</td>
        <td>Cell 4</td>
    </tr>
    <tr>
        <td>Cell 5</td>
        <td>Cell 6</td>
    </tr>
</table>
```

</td>
		<td>
			<picture>
				<img alt="First example" src="https://raw.githubusercontent.com/HerrMaroni/Documentation/main/E2.png">
			</picture>
		</td>
	</tr>
</table>

| How can we add borders and other formatting to our table?  | We can apply various formatting options to our table using CSS (Cascading Style Sheets). CSS allows us to add borders, change colors, adjust spacing, and apply other visual styles to our table. We can either use inline CSS by adding style attributes directly to the HTML elements or define a separate CSS file and link it to our HTML document.  |
| :---  | :--- |

<table>
	<tr>
		<td>

```html
<style>
    table {
        width: 100%;
        border-collapse: collapse;
        border: 1px solid black;
    }
    th,
    td {
        padding: 10px;
        border: 1px solid black;
        text-align: left;
    }
</style>
```

</td>
		<td>
			<picture>
				<img alt="First example" src="https://raw.githubusercontent.com/HerrMaroni/Documentation/main/E3.png">
			</picture>
		</td>
	</tr>
</table>

| Can we merge cells in a table?  | Yes, we can merge cells in a table using the rowspan and colspan attributes. The rowspan attribute specifies how many rows a cell should span vertically, while the colspan attribute specifies how many columns a cell should span horizontally. By using these attributes, we can create cells that span multiple rows or columns. |
| :---  | :--- |

<table>
	<tr>
		<td>

```html
<table>
    <tr>
        <th>Header 1</th>
        <th>Header 2</th>
    </tr>
    <tr>
        <td colspan="2">Cell 1 & 2 merged</td>
    </tr>
    <tr>
        <td rowspan="2">Cell 3 & 5 merged</td>
        <td>Cell 4</td>
    </tr>
    <tr>
        <td>Cell 6</td>
    </tr>
</table>
```

</td>
		<td>
			<picture>
				<img alt="First example" src="https://raw.githubusercontent.com/HerrMaroni/Documentation/main/E4.png">
			</picture>
		</td>
	</tr>
</table>
