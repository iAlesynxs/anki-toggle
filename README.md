# anki-toggle
É um código que vai criar um botão nos cartões do anki para eventuais consultas nas revisões

Parte do Verso
(É preferível criar um campo específico para usar esse código. No meu caso, o campo que eu criei foi o "Query")

{{#Query}}

<div class="extra_toggle" id="extra_toggle_on_button" onclick="showQuery()">
               
Query</div>

<div class="Query" id="extrafield">   
<div class="extra_toggle" id="extra_toggle_off_button" onclick="hideQuery()">
Fechar Query</div>

 {{edit:Query}}

</div>
<br>
             

</div>

<script>
    function showQuery() {
        document.getElementById("extrafield").style.display = "block";
        document.getElementById("extra_toggle_on_button").style.display = "none";
    }
    function hideQuery() {
        document.getElementById("extrafield").style.display = "none";
        document.getElementById("extra_toggle_on_button").style.display = "block";
    }


</script>


{{/Query}}




Parte de estilo

.Query {
position: relative;
left: 50%;
transform: translateX(-50%);
display: none;
font-family: arial;
font-size: 20px;
text-align: justify;
color: black;
line-height: 30px;
height: auto;
width: 850px;
padding: 20px 20px;
margin-top: 0px;
background-color: #dcdcdd;
box-sizing: border-box;
}

.extra_toggle {
position: relative;
left: 50%;
transform: translateX(-50%);
display: block;
font-family:Segoe UI Black;
font-size: 17px;
color: rgb(0,0,0));
text-align: center;
margin-top: 20px;
border-radius: 20px;
padding-bottom: 10px;
background-color: #a3a1a1;
transition: background-color 0.15s ease-out;
}

.extra_toggle:hover {
  color: rgba(0,0,128);
}
