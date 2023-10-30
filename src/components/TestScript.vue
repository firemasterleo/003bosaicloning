<template>
    <div class="link" @mouseover="showPopup" @mouseleave="hidePopup">
        <a href="#">Hover Me</a>
        <div class="firstpopup" v-if="isHovered" >
            <div @mouseover="showsecondPopup" @mouseleave="hidesecondPopup">
                <h1 >this is popup one</h1>
                <div class="secondpopup" v-if="isHovered2" @mouseleave="hidesecondPopup"><h1>this is popup two</h1></div>        
            </div>
            
        </div>
    </div>

</template>

<script>
export default {
data() {
return {
isHovered: false, // Initially, the popup is hidden
isHovered2: false,
};
},
methods: {
showPopup() {
this.isHovered = true; // Show the popup when hovering

},
hidePopup() {
this.isHovered = false; // Hide the popup when not hovering

},
showsecondPopup() {
this.isHovered2 = true; // Show the popup when hovering
},
hidesecondPopup() {
this.isHovered2 = false; // Show the popup when hovering
},
},
};
</script>
<style>

.link {
    margin-top: 10rem;
    margin-left: 10rem;
    border-style: solid;
    padding: 2rem;
    width: 5rem;
    height: 5rem;
}

.firstpopup {
    position: absolute;
    top: 15rem;
    border-style: solid;
    width: 20rem;
    height: 30rem;
}

.secondpopup {
    position: absolute;
    bottom: 3rem;
    left: 19rem;
    border-style: solid;
    width: 20rem;
    height: 30rem;
}
</style>