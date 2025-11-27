<template>
    <div id="skills-container" class="container my-4">
        <div class="row">
            <div class="col-12 px-5 py-4 d-flex flex-column col-lg-4">
                <h3>As videogame lover...</h3>
                <p>I consider video games to be complete cultural works, which can captivate us with rich experiences of different art forms. I have enjoyed them since I was a child and I am committed to creating my own stories to captivate more people.</p>
                <p><span>Favourites videogames: </span>Red Dead Redemption 2, Ultrakill, Bloodborne, Hollow Knight and Cult of the Lamb.</p>
            </div>
            <div class="col-12 px-5 py-4 d-flex flex-column col-lg-4">
                <h3>As developer...</h3>
                <p>Organization, simplicity, and clean code are the most important things to me, so it's something I try to improve. I like learning to solve patterns in a simple way, finding efficient solutions, and reinforcing principles and good practices in my knowledge.</p>
                <p><span>Dev tools: </span>Visual Studio Code, Vue, Django, Bootstrap, Godot Engine, Pixi.js</p>
            </div>
            <div class="col-12 px-5 py-4 d-flex flex-column col-lg-4">
                <h3>As artist...</h3>
                <p>I have a clear tendency towards pixel-art and every day I take a step closer to perfecting this beautiful and complex technique. As in any creative discipline, the process of improvement is continuous, and there is always a long way to go.</p>
                <p><span>Fun fact: </span>all the pixel-art you find on this page was drawn by me c:</p>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
#skills-container {
    color: $dark_2;
    h3 {
        font: {
            family: $pixel-font;
            weight: bolder;
        }
    }
    span {
        color: $primary;
    }
}
.placeholder {
    background-color: $dark_1;
    width: 100%;
    height: 4rem;
}
</style>