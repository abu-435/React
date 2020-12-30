# React adding subration and div and mul

<html>

<head>


    <div class="function" style="width: 100%;height: 100%;">
        Enter the Value1: <input id="input1" type="text" size="5" /> <br>
        Enter the Value2: <input id="input2" type="text" size="5" /> <br>
        <br>
        select the operator : <br>
        <button id="+" onclick="calculation('add')">+</button>
        <button id="-" onclick="calculation('sub')">-</button>
        <button id="*" onclick="calculation('mul')">*</button>
        <button id="/" onlclick="calculation('div')">/</button> <br><br>
        <button id="==" onclick="settime()">=</button>
        Output is : <input id="=" size="10" placeholder="Answer" /><br><br>
        clearInterval : <button onclick="clearin()">Clear</button>
    </div>


<body>
    <script>


        var c = 0;
        var settime;

        function settime(){
            settime=setInterval(abc,3000)
        }
        // function settime(){
        //     settime=setTimeout (abc,3000)
        // }
        function clearin()
        {
            clearInterval(settime)
        }
        function calculation(operator) {

            var a = document.getElementById("input1").value;
            var a = parseInt(a);

            var b = document.getElementById("input2").value;
            var b = parseInt(b);

            
            

            switch (operator) {
                case 'add':
                    
                    c = a + b;
                
                    break;
                case 'sub':
                    // if (a>b){
                    // c = a - b;
                    // }
                    // else{
                    //     c=b-a
                    // }
                    c=a>b ? a-b:b-a
                    break;
                case 'mul':
                    c = a * b;
                    break;
                case 'div':
                    
                    c = a / b;
                    break;
            
                // case 'd':
                // document.getElementById("=").value=c
                // break;

            

             
            }
        }
        function abc(aa){
            // switch (aa){
            //     case 'd':

            // document.getElementById("+").addEventListener(onclick,calculation('add'))
            // document.getElementById("-").addEventListener(onclick,calculation('sub'))
            // document.getElementById("*").addEventListener(onclick,calculation('mul'))
            // document.getElementById("/").addEventListener(onclick,calculation('div'))
            
            document.getElementById("=").value=c
           console.log(c)
        //}
        }

        // setTimeout(function(aa){
        //     console.log(c)

        // },3000)

        // setTimeout(function abc(aa){

        //     switch (aa){
        //         case 'd':
        //         document.getElementById("=").value=c

        //     }

        // },2000)

        
            //document.getElementById("=").value=document.getElementById("==").value
            //document.write(c)

        


    </script>
</body>




</head>

</html>
