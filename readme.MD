https://github.com/qtungnui07/auto-complete-survey-of-cmc.git

```javascript
(function autoFillSurvey() {
    const questions = document.querySelectorAll('.student-choose');

    if (questions.length === 0) {
        console.warn("not fodun");
        return;
    }
    let count = 0;
    questions.forEach((questionBlock, index) => {
        const radios = questionBlock.querySelectorAll('input[type="radio"]');
        if (radios.length >= 5) {
            const goodOptions = [radios[3], radios[4]];
            const randomOption = goodOptions[Math.floor(Math.random() * goodOptions.length)];
            if (randomOption) {
                randomOption.click();
                count++;
            }
        }
    });

    console.log(`${count} questions`);
    alert("Done, kiểm tra trước khi submit");
})();
```