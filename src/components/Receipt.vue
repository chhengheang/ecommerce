<template>
        <form class="w-50 mx-auto at-5 mb-5">
        <div class="form-group">
        <label for="formGroupExampleInput">Product Id</label>
        <input type="number" class="form-control" id="ids" />
        </div>
        <div class="form-group">
            <label for="formGroupExampleInput">Product Name</label>
            <input type="text" class="form-control" id="product" />
        </div>
        <div class="form-group">
            <label for="formGroupExampleInput2">Price</label>
            <input type="number" class="form-control" id="prc" />
        </div>
        <div class="form-group">
            <label for="formGroupExampleInput2">Quantity</label>
            <input type="number" class="form-control" id="qty" onchange="calculate()" />
            </div>
            <div class="form-group">
                <label for="formGroupExampleInput2">Amount</label>
                <input type="number" class="form-control" id="amnt" />
            </div>
            <button type="button" class="btn btn-warning m=2" onclick="addData()">
                Add
            </button>
    </form>
    <hr>
    <table bgcolor="blue" width="100%">
        <tr>
            <td>
                <H1>
                    <font color="white">
                        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;INVOICE</font>
                </H1>
            </td>
            <td width="100"></td>
            <td>
                <font color="white">+8552300000<br>
                    GICcafe@gmail.com<br>
                    Giccrew@gmail.com</font>
            <td>
                <font color="white">ITC-Phnom Penh Campus<br>
                    Phnom Penh<br>
                    Cambodia</font>
            </td>
            </td>
        </tr>
    </table>
    <br><br>
    
    <table>
        <tr>
            <td width="5%"> </td>
            <td width="500">Billed to</td>
            <td width="500">&nbsp;&nbsp;&nbsp; Invoive Number</td>
            <td width="200">&nbsp;&nbsp;&nbsp;</td>
            <td width="200">Invoice Total</td>
        </tr>
        <tr>
            <td width="5%"> </td>
            <td width="500">Client Number</td>
            <td width="500">&nbsp;&nbsp;&nbsp; 10000001</td>
            <td width="200"></td>
            <td width="200"id="total-amount"><b>
                </b></td>
        </tr>
        <tr>
            <td width="5%"> </td>
            <td width="500">Client Address</td>
            <td width="500">&nbsp;&nbsp;&nbsp;</td>
            <td width="200">&nbsp;&nbsp;&nbsp;</td>
            <td width="200">&nbsp;&nbsp;&nbsp;</td>
        </tr>
        <tr>
            <td width="5%"> </td>
            <td width="500"> City,State Country</td>
            <td width="500">&nbsp;&nbsp;&nbsp; Date of issue</td>
            <td width="200">&nbsp;&nbsp;&nbsp;</td>
            <td width="200">&nbsp;&nbsp;&nbsp;</td>
        </tr>
        <tr>
            <td width="10%"> </td>
            <td width="500">ZIP CODE</td>
            <td width="500">&nbsp;&nbsp;&nbsp;10/07/14</td>
            <td width="200">&nbsp;&nbsp;&nbsp;</td>
            <td width="200">&nbsp;&nbsp;&nbsp;</td>
        </tr>
    </table>
    <!--lines-->
    <hr />
    <table class="table">
        <thead id="tablehead">
            <tr>
                <th id="ids">Id</th>
                <th>Product Name</th>
                <th>Price</th>
                <th>Quantity</th>
                <th>Amount</th>
            </tr>
        </thead>
        <tbody id="newtr">

        </tbody>

    </table>
    <hr>
    <table class="table">
        <tr>
            <th width="20%"></th>
            <th width="20%"></th>
            <th width="20%"></th>
            <th width="20%">Subtotal:</th>
            <th width="20%"id="subtotal-amount"></th>
        </tr>
        <tr>
            <th width="20%"></th>
            <th width="20%"></th>
            <th width="20%"></th>
            <th width="20%">Tax: </th>
            <th width="20%"></th>
        </tr>
        <tr>
            <th width="20%"></th>
            <th width="20%"></th>
            <th width="20%"></th>
            <th width="20%">Total Amount($):</th>
            <th width="20%" id="total"></th>
        </tr>
    </table>
</template>
<style>
    body{
        background-color: antiquewhite;
        background-size: cover;
        background-repeat: no-repeat;
    }
    label,
    td,
    th {
        color: black;
    }
    #tablehead{
        background-color: aquamarine;
        color: black;
    }
</style>




    <script>
        var price;
        var quantity;
        var amount;
        var prod_name;
        var ids;
        var tax = 0;
        function calculate(){
            ids = document.getElementById("ids").value;
            price = document.getElementById("prc").value;
            quantity = document.getElementById("qty").value;
            amount = price *quantity;
            document.getElementById("amnt").value = amount;
        }

        function addData(){
            prod_name = document.getElementById("product").value;
            document.getElementById('newtr').innerHTML += '<tr><td>' + prod_name + '</td><td>' + price + '</td> <td>' + quantity + '</td><td>' + amount + '</td></tr>'
            document.getElementById("ids").value = " ";
            document.getElementById("product").value = " ";
            document.getElementById("prc").value = " ";
            document.getElementById("amnt").value = " ";
            document.getElementById("amnt").value = " ";
            document.getElementById("subtotal-amount").innerHTML = price * quantity;
            document.getElementById("total-amount").innerHTML = price * quantity - tax;
            document.getElementById("total").innerHTML = price * quantity - tax;

        }

    </script>