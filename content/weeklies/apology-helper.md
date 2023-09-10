---
title: "Apology Helper"
description: "A (crappy) tool to help you apologize."
---

# Do you need to apologize?

Well, look no further! This tool will help you apologize to your friends, family, loved ones, and strangers on the street.

<script src="/js/a.js"></script>

<div id="apology-helper">
  <div id="question1">
    <p>To whom would you like to apologize?</p>
    <input type="text" id="recipient">
    <button onclick="mrhota.alphabetsuperset.a.nextQuestion(2)">Next</button>
  </div>
  
  <div id="question2" style="display:none;">
    <p>Are you actually sorry?</p>
    <select id="apologetic">
      <option value="yes">Yes</option>
      <option value="no">No</option>
    </select>
    <button onclick="mrhota.alphabetsuperset.a.nextQuestion(3)">Next</button>
  </div>

  <div id="question3" style="display:none;">
    <p>Which word best describes your feelings?</p>
    <select id="feeling">
      <option value="regretful">Regretful</option>
      <option value="sorrowful">Sorrowful</option>
      <option value="contrite">Contrite</option>
      <option value="rueful">Rueful</option>
      <option value="sorry">Sorry</option>
      <option value="remorseful">Remorseful</option>
      <option value="disappointed">Disappointed</option>
    </select>
    <button onclick="mrhota.alphabetsuperset.a.nextQuestion(4)">Next</button>
  </div>

  <div id="question4" style="display:none;">
    <p>Why do you feel that way?</p>
    <textarea id="reason" rows="5" cols="50"></textarea>
    <button onclick="mrhota.alphabetsuperset.a.generateApology()">Generate Apology</button>
  </div>

  <div id="result" style="display:none;">
    <p>Your apology:</p>
    <textarea id="apologyText" rows="5" cols="50"></textarea>
  </div>
</div>
