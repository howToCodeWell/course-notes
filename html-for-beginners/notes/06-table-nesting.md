---
course_slug: html-for-beginners
tutorial_number: 6
type: note
---
For complicated layouts, HTML tables can be nested.  Placing tables withing tables is a common approach when structuring HTML e-mails.
A nested table will be placed inside the parents `<td></td>` element like so
<table>
   <tr>
       <td>This is the first cell</td>
       <td>
           <table border="1">
               <tr>
                    <td>Nested table cell 1</td>
                    <td>Nested table cell 2</td>
               </tr>
               <tr>
                    <td>Nested table cell 3</td>
                    <td>Nested table cell 4</td>
               </tr>
           </table> 
      </td>
   </tr>    
</table>

In this example there is one nested table with 4 table cells.  The width and the height of the first table cell matches the width and height of the nested table


```html
<table>
   <tr>
       <td>This is the first cell</td>
       <td>
           <table>
               <tr>
                    <td>Nested table cell 1</td>
                    <td>Nested table cell 2</td>
               </tr>
               <tr>
                    <td>Nested table cell 3</td>
                    <td>Nested table cell 4</td>
               </tr>
           </table> 
      </td>
   </tr>    
</table>
```


## Multiple nested tables
Complex layouts may required multiple nested tables.  In this invoice example there is a nested table for line items and a nested table for payment totals.


<table>
    <tr>
       <td align="center">Invoice</td>
    </tr>
    <tr>
       <td>
           <table>
               <tr>
                    <td>Product 1</td>
                    <td>£10.99</td>
               </tr>
               <tr>
                    <td>Product 2</td>
                    <td>£4.99</td>
               </tr>
           </table> 
      </td>
   </tr>   
   <tr>
       <td>
           <table>
               <tr>
                    <td>Sub Total</td>
                    <td>£15.98</td>
               </tr>
               <tr>
                    <td>Tax</td>
                    <td>£3.20</td>
               </tr>
                <tr>
                    <td>Total payable</td>
                    <td>£19.18</td>
               </tr>
           </table> 
      </td>
   </tr> 
</table>

```html

<table>
    <tr>
       <td align="center">Invoice</td>
    </tr>
    <tr>
       <td>
           <table>
               <tr>
                    <td>Product 1</td>
                    <td>£10.99</td>
               </tr>
               <tr>
                    <td>Product 2</td>
                    <td>£4.99</td>
               </tr>
           </table> 
      </td>
   </tr>   
   <tr>
       <td>
           <table>
               <tr>
                    <td>Sub Total</td>
                    <td>£15.98</td>
               </tr>
               <tr>
                    <td>Tax</td>
                    <td>£3.20</td>
               </tr>
                <tr>
                    <td>Total payable</td>
                    <td>£19.18</td>
               </tr>
           </table> 
      </td>
   </tr> 
</table>
```
