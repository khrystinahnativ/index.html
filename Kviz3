<!DOCTYPE html>
<html lang="cs">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Costa Quiz</title>

<style>

body{
    font-family: Arial, sans-serif;
    background:#ffd6e7;
    margin:0;
    padding:20px;
}

.quiz-container{
    max-width:900px;
    margin:auto;
}

.title{
    text-align:center;
    color:#c2185b;
    margin-bottom:30px;
}

.question-box{
    background:white;
    padding:20px;
    margin-bottom:20px;
    border-radius:20px;
    box-shadow:0 4px 10px rgba(0,0,0,0.1);
}

.question{
    font-weight:bold;
    color:#d63384;
    margin-bottom:15px;
    font-size:18px;
}

.answer{
    background:#ffe4ef;
    padding:12px;
    margin:8px 0;
    border-radius:12px;
    cursor:pointer;
    transition:0.2s;
}

.answer:hover{
    background:#ffc1da;
}

.correct{
    background:#b7f5c8 !important;
}

.wrong{
    background:#ff9d9d !important;
}

.result{
    text-align:center;
    font-size:30px;
    margin-top:30px;
    color:#c2185b;
    font-weight:bold;
}

</style>
</head>

<body>

<div class="quiz-container">

<h1 class="title">☕ COSTA COFFEE QUIZ ☕</h1>

<div id="quiz"></div>

<div class="result" id="result"></div>

</div>

<script>

const questions = [

{
question:"1. Kdo založil Costa Coffee a kdy?",
answers:[
{text:"Sergio a Bruno Costa v roce 1971", correct:true},
{text:"Howard Schultz v roce 1980", correct:false}
]
},

{
question:"2. Co je směs Mocha Italia?",
answers:[
{text:"Směs Arabiky a Robusty", correct:true},
{text:"Pouze Robusta", correct:false}
]
},

{
question:"3. Jaký je rozdíl mezi Arabikou a Robustou?",
answers:[
{text:"Arabica má více aroma a méně kofeinu", correct:true},
{text:"Robusta má méně kofeinu", correct:false}
]
},

{
question:"4. Která káva obsahuje více kofeinu?",
answers:[
{text:"Robusta", correct:true},
{text:"Arabica", correct:false}
]
},

{
question:"5. Která káva dodává více aroma a kyselosti?",
answers:[
{text:"Arabica", correct:true},
{text:"Robusta", correct:false}
]
},

{
question:"6. V jakých nadmořských výškách roste Arabica?",
answers:[
{text:"900–2000 m n. m.", correct:true},
{text:"100–300 m n. m.", correct:false}
]
},

{
question:"7. Jak dlouho trvá než začne kávovník plodit?",
answers:[
{text:"Přibližně 5 let", correct:true},
{text:"6 měsíců", correct:false}
]
},

{
question:"8. Jaké jsou typy sklizně kávy?",
answers:[
{text:"Výběrové, mechanické a v pásech", correct:true},
{text:"Ruční a vodní", correct:false}
]
},

{
question:"9. Co znamená Rainforest Alliance?",
answers:[
{text:"Ochrana farmářů a půdy", correct:true},
{text:"Druh kávy", correct:false}
]
},

{
question:"10. Jaký tlak vody má mít kávovar?",
answers:[
{text:"9–10 bar", correct:true},
{text:"2–3 bar", correct:false}
]
},

{
question:"11. Jaký tlak páry má mít kávovar?",
answers:[
{text:"1–1,5 bar", correct:true},
{text:"5 bar", correct:false}
]
},

{
question:"12. Jaké druhy pák používáme?",
answers:[
{text:"Dvojpáka, trojpáka, bezkofeinová a slepá", correct:true},
{text:"Pouze dvojpáka", correct:false}
]
},

{
question:"13. K čemu slouží slepá páka?",
answers:[
{text:"K čištění kávovaru", correct:true},
{text:"K přípravě latte", correct:false}
]
},

{
question:"14. Kolik gramů kávy je v dvojpáce?",
answers:[
{text:"14 g", correct:true},
{text:"21 g", correct:false}
]
},

{
question:"15. Kolik gramů kávy je v trojpáce?",
answers:[
{text:"21 g", correct:true},
{text:"14 g", correct:false}
]
},

{
question:"16. Co se stane když je káva moc jemně namletá?",
answers:[
{text:"Teče pomalu", correct:true},
{text:"Teče rychle", correct:false}
]
},

{
question:"17. Co se stane když je káva moc hrubě namletá?",
answers:[
{text:"Teče rychle", correct:true},
{text:"Neteče vůbec", correct:false}
]
},

{
question:"18. Co nastavujeme první?",
answers:[
{text:"Grind", correct:true},
{text:"Dose", correct:false}
]
},

{
question:"19. Jaký je recept na perfektní espresso?",
answers:[
{text:"14 g + 20 s = 60 ml", correct:true},
{text:"5 g + 5 s = 20 ml", correct:false}
]
},

{
question:"20. Jak má vypadat správná créma?",
answers:[
{text:"Sametová a oříšková", correct:true},
{text:"Velké bubliny", correct:false}
]
},

{
question:"21. Jak vysoká má být créma?",
answers:[
{text:"3–15 mm", correct:true},
{text:"30 mm", correct:false}
]
},

{
question:"22. Jaké 4 chutě musí být v rovnováze?",
answers:[
{text:"Sladkost, slanost, kyselost, hořkost", correct:true},
{text:"Sladkost a kyselost", correct:false}
]
},

{
question:"23. Jak dlouho po nadávkování musí začít extrakce?",
answers:[
{text:"Do 15 sekund", correct:true},
{text:"Po 1 minutě", correct:false}
]
},

{
question:"24. Proč nahříváme šálky?",
answers:[
{text:"Aby espresso zůstalo déle horké", correct:true},
{text:"Kvůli dekoraci", correct:false}
]
},

{
question:"25. Jaké jsou 4 baristické kroky?",
answers:[
{text:"Zarovnání, tamper, twist, setření", correct:true},
{text:"Míchání a vaření", correct:false}
]
},

{
question:"26. Jak dlouho extrahujeme ristretto?",
answers:[
{text:"15 sekund", correct:true},
{text:"40 sekund", correct:false}
]
},

{
question:"27. Kolik ml má ristretto?",
answers:[
{text:"20 ml", correct:true},
{text:"80 ml", correct:false}
]
},

{
question:"28. Jaký je recept na triple espresso?",
answers:[
{text:"21 g + 35 s = 80 ml", correct:true},
{text:"14 g + 10 s", correct:false}
]
},

{
question:"29. Jaká je ideální teplota mléka?",
answers:[
{text:"150–152 °F", correct:true},
{text:"190 °F", correct:false}
]
},

{
question:"30. Kdy je mléko přepálené?",
answers:[
{text:"Nad 161 °F", correct:true},
{text:"Pod 100 °F", correct:false}
]
},

{
question:"31. Proč nikdy neohříváme mléko dvakrát?",
answers:[
{text:"Kvůli bakteriím a kvalitě", correct:true},
{text:"Protože je studené", correct:false}
]
},

{
question:"32. Jak poznáš správně napěněné mléko?",
answers:[
{text:"Je jemné a sametové", correct:true},
{text:"Má velké bubliny", correct:false}
]
},

{
question:"33. Jaký je rozdíl mezi latte a cappuccinem?",
answers:[
{text:"Latte má méně pěny", correct:true},
{text:"Cappuccino nemá pěnu", correct:false}
]
},

{
question:"34. Jak má vypadat správné latte?",
answers:[
{text:"Jednolitá barva bez vrstev", correct:true},
{text:"Oddělené vrstvy", correct:false}
]
},

{
question:"35. Kolik pěny má mít latte?",
answers:[
{text:"1 cm", correct:true},
{text:"5 cm", correct:false}
]
},

{
question:"36. Jak má vypadat cappuccino?",
answers:[
{text:"Hustá pěna a prstenec", correct:true},
{text:"Bez pěny", correct:false}
]
},

{
question:"37. Co je cortissimo?",
answers:[
{text:"Krátká extrakce pro flat white", correct:true},
{text:"Typ mléka", correct:false}
]
},

{
question:"38. Jaký je recept na flat white?",
answers:[
{text:"21 g + 15 s = 30 ml", correct:true},
{text:"14 g + 5 s", correct:false}
]
},

{
question:"39. Jaký latte art používáme jako základ?",
answers:[
{text:"Rozeta", correct:true},
{text:"Srdce", correct:false}
]
},

{
question:"40. Jaký je rozdíl mezi mocha latte a horkou čokoládou?",
answers:[
{text:"Mocha obsahuje espresso", correct:true},
{text:"Čokoláda obsahuje espresso", correct:false}
]
},

{
question:"41. Jak označujeme sóju?",
answers:[
{text:"S", correct:true},
{text:"SO", correct:false}
]
},

{
question:"42. Proč nikdy nepíšeme víčka dopředu?",
answers:[
{text:"Kvůli alergenům", correct:true},
{text:"Kvůli designu", correct:false}
]
},

{
question:"43. Jaké alternativní nápoje Costa používá?",
answers:[
{text:"Sójové, ovesné, kokosové...", correct:true},
{text:"Pouze kravské", correct:false}
]
},

{
question:"44. Jak často měníme hadr na mléko?",
answers:[
{text:"Po 4 hodinách", correct:true},
{text:"1× týdně", correct:false}
]
},

{
question:"45. Co je backflush?",
answers:[
{text:"Čištění hlavy kávovaru", correct:true},
{text:"Druh kávy", correct:false}
]
},

{
question:"46. Proč čistíme trysku před i po použití?",
answers:[
{text:"Kvůli bakteriím", correct:true},
{text:"Kvůli hluku", correct:false}
]
},

{
question:"47. Co bys nikdy neměl udělat s použitým mlékem?",
answers:[
{text:"Znovu ho ohřát", correct:true},
{text:"Vylít ho", correct:false}
]
},

{
question:"48. Co uděláš když espresso teče moc rychle?",
answers:[
{text:"Nastavím jemnější mletí", correct:true},
{text:"Hrubší mletí", correct:false}
]
},

{
question:"49. Co uděláš když espresso skoro neteče?",
answers:[
{text:"Nastavím hrubší mletí", correct:true},
{text:"Jemnější mletí", correct:false}
]
},

{
question:"50. Proč je důležité dělat espresso až jako poslední?",
answers:[
{text:"Aby bylo čerstvé", correct:true},
{text:"Kvůli dekoraci", correct:false}
]
},

{
question:"51. Co způsobí velké bubliny v cappuccinu?",
answers:[
{text:"Moc vzduchu při pěnění", correct:true},
{text:"Studené mléko", correct:false}
]
},

{
question:"52. Co uděláš když zákazník řekne že je mléko studené?",
answers:[
{text:"Udělám nový nápoj", correct:true},
{text:"Ignoruji to", correct:false}
]
},

{
question:"53. Jak poznáš správně nastavený mlýnek?",
answers:[
{text:"Podle extrakce a chuti", correct:true},
{text:"Podle barvy hrnku", correct:false}
]
},

{
question:"54. Co je nejčastější chyba u latte?",
answers:[
{text:"Vrstvení nápoje", correct:true},
{text:"Málo kávy", correct:false}
]
},

{
question:"55. Co je nejčastější chyba u cappuccina?",
answers:[
{text:"Velké bubliny", correct:true},
{text:"Moc kávy", correct:false}
]
},

{
question:"56. Jaký je rozdíl mezi flat white a latte?",
answers:[
{text:"Flat white je silnější", correct:true},
{text:"Latte je silnější", correct:false}
]
},

{
question:"57. Proč je důležité pořadí přípravy nápojů?",
answers:[
{text:"Kvůli čerstvosti", correct:true},
{text:"Kvůli rychlosti hudby", correct:false}
]
},

{
question:"58. Co uděláš při alergii zákazníka na mléko?",
answers:[
{text:"Použiju alternativu a čisté náčiní", correct:true},
{text:"Použiju stejné mléko", correct:false}
]
},

{
question:"59. Proč cappuccino nesmí mít velké bubliny?",
answers:[
{text:"Pěna musí být jemná", correct:true},
{text:"Protože je to zakázané", correct:false}
]
},

{
question:"60. Co dělá dobrého baristu?",
answers:[
{text:"Konzistence, čistota a přístup", correct:true},
{text:"Jen rychlost", correct:false}
]
}

];

const quiz = document.getElementById("quiz");
const result = document.getElementById("result");

let score = 0;
let answered = 0;

questions.forEach((q)=>{

const box = document.createElement("div");
box.classList.add("question-box");

const question = document.createElement("div");
question.classList.add("question");
question.innerText = q.question;

box.appendChild(question);

q.answers.forEach(answer=>{

const btn = document.createElement("div");
btn.classList.add("answer");
btn.innerHTML = "• " + answer.text;

btn.onclick = ()=>{

if(box.classList.contains("done")) return;

box.classList.add("done");

answered++;

if(answer.correct){
btn.classList.add("correct");
score++;
}else{
btn.classList.add("wrong");
}

Array.from(box.getElementsByClassName("answer")).forEach(el=>{
el.style.pointerEvents="none";
});

if(answered === questions.length){
result.innerHTML = `🎉 Výsledek: ${score}/${questions.length}`;
}

};

box.appendChild(btn);

});

quiz.appendChild(box);

});

</script>

</body>
</html>
