<template>
    <div id='home'></div>
    
  <span id="text">Hello World</span>
</template>

<script>
export default {

}
function waitForMs(ms) {
    return new Promise((resolve) => setTimeout(resolve, ms));
}
async function deleteWord() {
    let sentence = document.querySelector("#text").innerHTML.trim();
    console.log(sentence);

    let characters = sentence.split("");
    console.log(characters);

    while (characters.length > 0) {
        await waitForMs(100);
        characters.pop();
        document.querySelector("#text").innerHTML = characters.join("");

    }
}


async function writeWord(word) {
    let character = word.split("");
    console.log(character);

    let i = 0
    while (i < character.length) {
        await waitForMs(100);
        document.querySelector("#text").append(character[i]);
        i++;
    }
}

async function typingEffect() {
    await deleteWord();
    await waitForMs(500);
    await writeWord("My name is Zharne Desember");
    await waitForMs(700);
    await deleteWord();
    await waitForMs(500);
    await writeWord("I am a web developer");
    await waitForMs(700);
    await deleteWord();
    await waitForMs(500);
    await writeWord("Im more than that")
    await waitForMs(500);
    await deleteWord();
    await waitForMs(500);
    await writeWord("DESTINY")
}

typingEffect();


</script>

<style>
#home{
      background: url('https://i.postimg.cc/ryd5c9kk/pexels-tirachard-kumtanom-733857.jpg');
      background-size: cover;
    }
/* #home{
    min-height: 300vh;
} */
</style>