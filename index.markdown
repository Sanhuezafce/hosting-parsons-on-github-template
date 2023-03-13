---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Conociendo los problemas de Parsons !
---
# Parsons Practice

## Parsons 1
Re organiza los bloques para que digan el clasico mensaje "Hello World!"

<div id="p1-sortableTrash" class="sortable-code"></div>
<div id="p1-sortable" class="sortable-code"></div>
<div style="clear:both;"></div>
<p>
    <input id="p1-feedbackLink" value="Get Feedback" type="button" />
    <input id="p1-newInstanceLink" value="Reset Problem" type="button" />
</p>
<script type="text/javascript">
(function() {
  var initial = "print(\"Hello\")\n" +
    "print(\" \")\n" +
    "print(\"World\")\n" +
    "print(\"!\")";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "p1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": false,
    "x_indent": 50,
    "lang": "en",
    "trashId": "p1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#p1-newInstanceLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.shuffleLines();
  });
  $("#p1-feedbackLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.getFeedback();
  });
})();
</script>

## Parsons 2
A veces los problemas de Parsons pueden tener lineas que no corresponden al codigo final! (distractores)

<div id="Ejercicio 3-sortableTrash" class="sortable-code"></div> 
<div id="Ejercicio 3-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Ejercicio 3-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Ejercicio 3-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "altura = input(&quot;Porfavor ingrese la altura: &quot;)\n" +
    "ancho = input(&quot;Porfavor ingrese un ancho: &quot;)\n" +
    "area = int(altura) * int(ancho)\n" +
    "print(&quot;El area es: &quot;+ str(area))\n" +
    "area = altura * ancho #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Ejercicio 3-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "Ejercicio 3-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Ejercicio 3-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Ejercicio 3-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

### Siguiente ejemplo
[Next](./ej2.html)
