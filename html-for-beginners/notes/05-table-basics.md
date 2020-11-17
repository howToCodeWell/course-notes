HTML tables contain tabular data in rows and columns.  
The `<tr>` element represents a table row and a `<td>` is a table cell.
```html
<table>
   <tr>
       <td>First Table column</td>
       <td>Second Table column</td>
   </tr>    
   <tr>
       <td>First Table column</td>
       <td>Second Table column</td>
   </tr>   
</table>
```

## Table header, body and footer
HTML tables may contain table headings within `<th>` elements.  Table headings are styled differently to the table cells. 
Tables can also be split into a body `<tbody>` and a footer `<tfoot>` however both of these use standard table cells `<td>`. 
```html
<table>
   <thead>
       <tr>
           <th>First name</th>
           <th>Last name</th>
       </tr>   
   </thead>
   <tbody>
         <tr>
            <td>Murphy</td>
            <td>Fisher</td>
        </tr>   
    </tbody>
    <tfoot>
        <td>Pet:</td>
        <td>Dog</td>
    </tfoot>
</table>
```
