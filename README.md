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

---
## Advanced Tables

**What if we want to merge cells in a more precise way?**

For this we can use the `<col>` tag. The `<col>` tag in HTML is used to define attributes for a group of columns within a table. It allows you to apply styling or formatting to multiple columns simultaneously.

<table>
	<tr>
		<td>

```html
<table>
    <colgroup>
        <col style="width: 20%;">
        <col style="width: 20%;">
        <col style="width: 20%;">
        <col style="width: 20%;">
        <col style="width: 20%;">
    </colgroup>
    <tr>
        <th colspan="3">Header 1</th>
        <th colspan="2">Header 2</th>
    </tr>
    <tr>
        <td>Cell 1</td>
        <td>Cell 2</td>
        <td>Cell 3</td>
        <td>Cell 4</td>
        <td>Cell 5</td>
    </tr>
    <tr>
        <td colspan="3">Cell 6</td>
        <td colspan="1">Cell 7</td>
        <td colspan="1">Cell 8</td>
    </tr>
    <tr>
        <td colspan="2">Cell 9</td>
        <td colspan="1">Cell 10</td>
        <td colspan="2">Cell 11</td>
    </tr>
</table>
```

</td>
		<td>
			<picture>
				<img alt="First example" src="https://raw.githubusercontent.com/HerrMaroni/Documentation/main/E5.png">
			</picture>
		</td>
	</tr>
</table>

In this example, we use the `<colgroup>` element to group the `<col>` elements together. Each <col> element specifies a specific width using the width style attribute. We set the widths to 20%, 20%, 20%, 20%, and 20% respectively (total 100%), representing the five columns of the table.

The first row contains two headers that span two and three columns using the colspan attribute. This ensures that the header cells cover multiple columns.

The second row contains data cells in each column, maintaining the specified widths.

In the third row, the first data cell span across three columns using colspan="3", while the next two data cells occupy a single column each.

In the fourth row, the first data cell span across two columns using colspan="2", while the next data cell occupys a single column. The last data cell span across two columns using colspan="2" again.

---

To give a better example of how to achieve different cell spacing, let's create a table with 20 columns that all have a spacing of 5% (100% / 20 = 5%). This way we can make finer adjustments.

```html
<table>
    <colgroup>
        <col width="5%"><col width="5%">
        <col width="5%"><col width="5%">
        <col width="5%"><col width="5%">
        <col width="5%"><col width="5%">
        <col width="5%"><col width="5%">
        <col width="5%"><col width="5%">
        <col width="5%"><col width="5%">
        <col width="5%"><col width="5%">
        <col width="5%"><col width="5%">
        <col width="5%"><col width="5%">
    </colgroup>
    <tr>
        <th colspan="4">Cell 1</th>
        <td colspan="16">Cell 2</td>
    </tr>
    <tr>
        <th colspan="6">Cell 3</th>
        <td colspan="14">Cell 4</td>
    </tr>
    <tr>
        <th colspan="4">Cell 5</th>
        <td colspan="6">Cell 6</td>
        <th colspan="4">Cell 7</th>
        <td colspan="6">Cell 8</td>
    </tr>
    <tr>
        <th colspan="3">Cell 9</th>
        <td colspan="17">Cell 10</td>
    </tr>
</table>
```

</td>
		<td>
			<picture>
				<img alt="First example" src="https://raw.githubusercontent.com/HerrMaroni/Documentation/main/E6.png">
			</picture>
		</td>
	</tr>
</table>
