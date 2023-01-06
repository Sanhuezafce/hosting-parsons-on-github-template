---
layout: default
title: Page 3 Example (Variable Check Grader)
---

<div id="ej1-sortableTrash" class="sortable-code"></div> 
<div id="ej1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="ej1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="ej1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "def hola():\n" +
    "	return 123\n" +
    "def hola: #distractor\n" +
    "	return hola #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "ej1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "ej1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#ej1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#ej1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      console.log(parsonsPuzzle.getFeedback()); 
      
  }); 
})(); 
</script>

[Previous](./example1.html)