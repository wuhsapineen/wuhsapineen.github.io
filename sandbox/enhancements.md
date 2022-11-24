---
title: Enhancements
description: 
layout: page
created: 2022-11-08 05:14:00 +1000
tags: notes, games, sandbox
source: 
author: wuhsapineen
nav: false
reference:
- []

---
<style type="text/css">
#formEnhancementSlots { line-height: 1.8; }
ul { 
	list-style-type:none; 
    margin: 0px 0px 0px -35px;
}
.enhancement {  }
.warning { font-style: italic; }
.quantity { max-width: 35px; }

</style>
<script type="text/javascript">
var arrayEnhancements = {
    "COLUMNS": [
        "ENH_VALUE",
        "ENH_NAME",],
        "DATA": [
        ["accuracy","Accuracy"],
        ["confuse","Confuse"],
        ["damage","Damage"],
        ["defense_buff","Defense Buff"],
        ["defense_debuff","Defense Debuff"],
        ["disorient","Disorient"],
        ["endurance_modification","Endurance Modification"],
        ["endurance_reduction","Endurance Reduction"],
        ["fear","Fear"],
        ["flight","Flight"],
        ["healing_absorb","Healing/Absorb"],
        ["hold","Hold"],
        ["immobilization","Immobilization"],
        ["intangibility","Intangibility"],
        ["interrupt","Interrupt"],
        ["jump","Jump"],
        ["knockback","Knockback"],
        ["range","Range"],
        ["recharge_reduction","Recharge Reduction"],
        ["resist_damage","Resist Damage"],
        ["run_speed","Run Speed"],
        ["sleep","Sleep"],
        ["slow","Slow"],
        ["taunt_placate","Taunt/Placate"],
        ["tohit_buff","To Hit Buff"],
        ["tohit_debuff","To Hit Debuff"],
        ]
};
var arrayDisplayed = [];
</script>

<pre class="mermaid">
mindmap
  root((Cannon))
    [Code]
        (Web)
    [Spirit]
    [Something Else]
</pre>
<script type="module">
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@9/dist/mermaid.esm.min.mjs';
  mermaid.initialize({ startOnLoad: true });
</script>

<form id="formEnhancementSlots">
  <label ><b>Enhancement Slots:</b></label>
  <br />
  <ul id="ulEnhancementSlots">
    <!-- <li id="0">
      <select id="selectEnhancement_">
        <option selected="true">Enhancements</option>
      </select> 
      <input type="number" id="quantity" name="quantity" min="1" max="99" maxlength="2" /> 
      <input type="button" onclick="enhancementSave()" value="Save" /> 
      <input type="button" onclick="enhancementRemove()" value="Remove" />
      <br />
    </li> -->
    <!-- <li id="99">Accuracy (1) <input type="button" onclick="enhancementEdit(99)" value="Edit" /> <input type="button" onclick="enhancementRemove(99)" value="Remove" /><br /></li> -->
  </ul>
  <ul>
    <li id="add_btn">
      <input type="button" onclick="enhancementAdd()" value="Add" />
	</li>
  </ul

</form>
<br />
<br />
<div id="ToDo">
<h3>To do:</h3>
<ul>
<li>Option to export JSON data</li>
<li>Option to save JSON data to local drive</li>
</ul>
</div>
<br />

<script type="text/javascript">
// --- test ---
const divTest = document.getElementById("test");
const divResults = document.getElementById("results");
// --- endtest ---

	// Declare variables
    enhIndex = 0;
    
    // Functions
    function enhancementPopulate(id) {
    	// get select input to modify
        var dropdown = document.getElementById("selectEnhancement_" + id);
        // loop for each item in array
        for (let x in arrayEnhancements.DATA) {
        	// get enhancement value and name
            var enhValue = arrayEnhancements.DATA[x][0];
            var enhName = arrayEnhancements.DATA[x][1];
            // check if enhancement is already used

            // create new <option>
            var option = document.createElement("option");
            // fill option with array data at position arrayEnhancements.DATA[x][1]
			option.value = enhValue;
            option.text = enhName;
            // add option to select input
            dropdown.add(option);
        }
    }
    
    function enhancementAdd() {
    	// declare id
        var id = enhIndex;
        // select list
        const ulParent = document.getElementById("ulEnhancementSlots");
        // set list item contents
        var newEditLine = '<select id="selectEnhancement_' + id + '" class="enhancement"><option selected="true">Enhancements</option></select> <input type="number" id="quantity_' + id + '" class="quantity" name="quantity" min="1" max="99" maxlength="2" value="1" /> <input type="button" onclick="enhancementSave(' + id + ')" value="Save" /> <input type="button" onclick="enhancementRemove(' + id + ')" value="Remove" /> <span id="warning_' + id + '" class="warning"></span><br />\n';
        // create new list item
        var newLi = document.createElement("li");
        // set list item id
        newLi.id = id;
        // fill list item with contents
        newLi.innerHTML = newEditLine;
        // append list item to list
        ulParent.appendChild(newLi);
        // populate select input with contents from json data
        enhancementPopulate(id);
        // increment id
        enhIndex++;
    }
    
    function enhancementSave(id) {
        // get input values
        var dropdown = document.getElementById("selectEnhancement_" + id);
        var number = document.getElementById("quantity_" + id);
        var enhIndex = dropdown.selectedIndex;
        var enhName = dropdown.options[dropdown.selectedIndex].text;
        var enhValue = dropdown.options[dropdown.selectedIndex].value;
        var enhQty = number.value;
        
        // check if enhancement is already saved
		if (arrayDisplayed.includes(enhName)) { 
        	// write warning at right of line that enhancement is already used
            var warning = document.getElementById("warning_" + id).innerHTML = " ! - Enhancement already slotted.";
		}
        
	   	else { 
			// set list item contents (savedLine)
       		var savedLine = '<span id="enhIndex_' + id + '" hidden="true">' + enhIndex + '</span><span id="enhName_' + id + '">' + enhName + '</span><span id="enhValue_' + id + '" hidden="true">' + enhValue + '</span> (<span id="enhQty_' + id + '">' + enhQty + '</span>) <input type="button" onclick="enhancementEdit(' + id + ')" value="Edit" /> <input type="button" onclick="enhancementRemove(' + id + ')" value="Remove" /><br />\n';
       		// get list item to modify
       		var modifyLi = document.getElementById(id);
       		// replace contents of list item (id) with input values
			modifyLi.innerHTML = savedLine;                
			// add entry to array of displayed enhancements
        	arr.push(enhName);
		}
    }
    
    function enhancementRemove(id) {
    	// decrement id
        //enhIndex--;
        // get list item
        var listItem = document.getElementById(id);
        // remove() it
        listItem.remove()
    }
    
    function enhancementEdit(id) {
    	// get enhIndex
        var enhIndex = document.getElementById("enhIndex_" + id).innerHTML;
        // get enhQty
        var enhQty = document.getElementById("enhQty_" + id).innerHTML;
        // set list item contents
        var editLine = '<select id="selectEnhancement_' + id + '" class="enhancement"><option selected="true">Enhancements</option></select> <input type="number" id="quantity_' + id + '" class="quantity" name="quantity" min="1" max="99" maxlength="2" value="1" /> <input type="button" onclick="enhancementSave(' + id + ')" value="Save" /> <input type="button" onclick="enhancementRemove(' + id + ')" value="Remove" /> <span id="warning_' + id + '" class="warning"></span><br />\n';
        // modify list item
        document.getElementById(id).innerHTML = editLine;
        // populate select input
        enhancementPopulate(id);
        // select the appropriate enhancement
        var dropdown = document.getElementById("selectEnhancement_" + id).selectedIndex = enhIndex;
        // set quantity in number input
        var qty = document.getElementById("quantity_" + id).value = enhQty;
    }
    

</script>