---
layout: default
title: Conociendo los problemas de Parsons ! - Distractores
---
## Parsons 2
A veces los problemas de Parsons pueden
tener lineas que no corresponden al 
codigo final! (distractores)

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "Nombre = input(&quot;¿Cual es tu nombre? &quot;)\n" +
    "Apellido = input(&quot;¿Cual es tu apellido? &quot;)\n" +
    "print(&quot;Hola mi nombre es &quot; + str(Nombre) + &quot; &quot; + str(Apellido))\n" +
    "print(&quot;Hola mi nombre es &quot; + (Nombre) + &quot; &quot; + (Apellido)) #distractor\n" +
    "Nombre = (&quot;¿Cual es tu nombre? &quot;) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": false,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


### Ultimo ejemplo !
[Next](./ej3.html)
