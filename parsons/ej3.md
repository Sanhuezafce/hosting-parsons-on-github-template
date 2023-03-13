---
layout: default
title: Conociendo los problemas de Parsons ! - Limitaciones
---

Construya un programa que solicite al usuario una altura y un ancho y que imprima el area de un rectangulo.
Para su programa, solicite primero la altura y luego el ancho. En caso contrario, el sistema mostrara un error.

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "altura = input(&quot;Porfavor ingrese la altura: &quot;)\n" +
    "ancho = input(&quot;Porfavor ingrese un ancho: &quot;)\n" +
    "area = int(altura) * int(ancho)\n" +
    "print(&quot;El area es: &quot;+ str(area))\n" +
    "area = altura * ancho #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
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
