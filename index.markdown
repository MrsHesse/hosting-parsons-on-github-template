<div id="selection1-sortableTrash" class="sortable-code"></div> 
<div id="selection1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="selection1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="selection1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "for i in range(0, 4):\n" +
    "	 myTurtle.fd(50)\n" +
    "    myTurtle.rt(90)\n" +
    "    ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "selection1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.TurtleGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "executable_code": "",
    "programmingLang": "pseudo",
    "turtleModelCode": "for i in range(0, 4):\n\tmodelTurtle.fd(50)\n\tmodelTurtle.rt(90)\n    "
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#selection1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#selection1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
