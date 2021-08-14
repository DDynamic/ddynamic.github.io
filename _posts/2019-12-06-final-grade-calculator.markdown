Here is a calculator that you can use to determine what you’d need to score on a final to earn the grade you want.

<input type="number" id="q1" placeholder="Quarter 1 Grade">
<input type="number" id="q1w" placeholder="Quarter 1 Worth %"><br>
<input type="number" id="q2" placeholder="Quarter 2 Grade">
<input type="number" id="q2w" placeholder="Quarter 2 Worth %"><br>
<input type="number" id="want" placeholder="Want">
<input type="number" id="final" placeholder="Final Worth %"><br>
<button onclick="calculate()">Calculate</button>
<script>
function getPercentFromInputElementId(input) {
    return parseFloat(document.getElementById(input).value) / 100;
}
function calculate() {
    const q1 = getPercentFromInputElementId('q1') * getPercentFromInputElementId('q1w');
    const q2 = getPercentFromInputElementId('q2') * getPercentFromInputElementId('q2w');
    const combined = q1 + q2;
    const want = getPercentFromInputElementId('want');
    const final = getPercentFromInputElementId('final');
    alert('You will need to score a ' + (((want-combined)/final) * 100).toFixed(2) + '% on the final.');
}
</script>