---
layout: default
---
- [Primary][1]

<!DOCTYPE html>
<html>
<style type="text/css">
body { line-height: 1.8; }
#enhancement { max-width: 50px; }
#quantity { max-width: 25px; }

</style>
<script type="text/javascript">
var arrayEnhancements = {
    "COLUMNS": [
        "ENH_NAME",
        "ENH_VALUE",],
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
$.each(arrayEnhancements.DATA, function () {
    var $option = $('<option/>').text(this[1]).val(this[0]);
    $('#enhancement').append($option);
});
</script>
<body>
<h1>Display a Number Field</h1>

<br />
<form>
  <label for="quantity">Quantity (between 1 and 5):</label>
  <br />
  <select name="enhancement" id="enhancement" /><input type="number" id="quantity" name="quantity" min="1" max="5" maxlength="2" /> <input type="button" value="Save" />
  <br />
  <input type="button" value="Add" />
</form>

</body>
</html>



Except where otherwise <a href="#">noted</a>, content on this site is licensed under the <a href="https://creativecommons.org/publicdomain/zero/1.0/" target="_blank">Creative Commons Zero v1.0 Universal</a>


<!-- Reference-Style Links -->
[1]: {% link Primary/index.md %} "Primary"

