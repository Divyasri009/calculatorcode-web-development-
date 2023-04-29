<html>
<head>
    <title>calculator</title>
</head>
<style>
    .calculator {
        border: 5px solid black;
        background-color: skyblue;
        display: inline-block;
        width: 500px;
        height: 550px;
    }

    table {
        table-align: center;
        border: 10px solid black;
        margin: 5px;
    }

    input {
        margin: 5px;
        border: 10px solid black;
        height: 90px;
        width: 490px;
        font-size: 30px;
    }

        input[type=button] {
            border-radius: 10px;
            font-size: 30px;
            width: 104px;
            height: 60px;
            cursor: pointer;
        }
</style>


<body>
    <div class="container" align="center">
        <h1>Calculator</h1>


        <div class="calculator">

            <input type="text" placeholder="0000" id="display">
            <table>

                <tr>
                    <td> <input type="button" value='(' onclick="display('(')"> </td>
                    <td> <input type="button" value=')' onclick="display(')')"> </td> 
                    <td>
                        <input type="button" value='clear' onclick="clearScreen()">
                    </td>
                    <td> <input type="button" value='X' onclick="display('*')"> </td>

                </tr>

                <tr>
                    <td> <input type="button" value='1' onclick="display('1')"> </td>
                    <td> <input type="button" value='2' onclick="display('2')"> </td>
                    <td> <input type="button" value='3' onclick="display('3')"> </td>
                    <td> <input type="button" value='/' onclick="display('/')"> </td>
                </tr>
                <tr>
                    <td> <input type="button" value='4' onclick="display('4')"> </td>
                    <td> <input type="button" value='5' onclick="display('5')"> </td>
                    <td> <input type="button" value='6' onclick="display('6')"> </td>
                    <td> <input type="button" value='-' onclick="display('-')"> </td>
                </tr>
                <tr>
                    <td> <input type="button" value='7' onclick="display('7')"></td>
                    <td> <input type="button" value='8' onclick="display('8')"> </td>
                    <td> <input type="button" value='9' onclick="display('9')"> </td>
                    <td> <input type="button" value='+' onclick="display('+')"></td>
                </tr>
                <tr>
                    <td> <input type="button" value='.' onclick="display('.')"> </td>
                    <td> <input type="button" value='0' onclick="display('0')"> </td>
                    <td> <input type="button" value='del' onclick="back('del')"> </td>
                    <td> <input type="button" value='Enter' onclick="calc()"> </td>

                </tr>
            </table>
        </div>
    </div>
</body>
<script type="text/javascript">
function clearScreen()
{
    document.getElementById("display").value = null;
}
 

function display(value) {
   document.getElementById("display").value += value;
}
 

function calc()
{
 try{
    document.getElementById("display").value=eval(document.getElementById("display").value);
}
catch(exception)
{
 document.getElementById("display").value = "Error";
}
}
function back()
{
document.getElementById("display").value =document.getElementById("display").value.slice(0,-1);
}

</script>
</html>
