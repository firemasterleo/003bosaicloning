<script>

</script>



<style>
@font-face {
font-family: amerigobt;
src: url(../assets/font/AmerigoBT.ttf);
}

@font-face {
font-family: proximareg;
src: url(../assets/font/proximanova-regular.otf);
}

@font-face {
font-family: proximabold;
src: url(../assets/font/proximanova-semibold.otf);
}

.image {
    width: 42rem;
    height: auto;
    position: relative;
    bottom: 36.5rem;
    left: 41.3rem;
}
.headercontainer {
    background-color: rgb(254, 252, 252);
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 5rem;
    z-index: 100;
    display: flex;
    justify-content: left;
    align-items: center;
    font-family: amerigobt;
    letter-spacing: 5px;   
}

.namelogo {
    color: #00b289;
    font-family: amerigobt;
    font-size: 12px;
    letter-spacing: 1px;
    margin-left: 4rem;
}

.resourcescontainer {
    padding-bottom: 1.5rem;
    position: absolute;
    top: 1.9rem;
    left: 26.5rem;
    margin-right: 6rem;
}

.resourceslink {
    font-family: amerigotbt;
    font-size: 17px;
    text-decoration: none;
    color: rgba(0, 0, 0, 0.669);
    letter-spacing: 1px;
}

.resourceslink:hover {
    color: rgba(0, 0, 0, 0.959);
}


.popup {
    position: absolute;
    top: 2rem;
    left: -7.5rem;
    height: 33rem;
    width: 18rem;
    background-color: white;
    padding-right: 2rem;
    padding-left: 2rem;
    box-shadow: 20px 20px 40px rgba(0, 0, 0, 0.03),
              -20px -20px 40px rgba(0, 0, 0, 0.03),
              20px -20px 40px rgba(0, 0, 0, 0.03),
              -20px 20px 40px rgba(0, 0, 0, 0.03);
    display: flex;
    flex-direction: column;  
   

}
.popupcontainer1content1 {
    border-bottom-style: solid;
    padding-bottom: 2rem;
    border-width: 0.5px;
    border-color: silver;
    margin-top: 2rem;
    height: 8rem;

}

.popupcontainer1content1hover {
    border-bottom-style: solid;
    padding-bottom: 2rem;
    border-width: 0.5px;
    border-color: rgb(255, 255, 255);
    margin-top: 2rem;
    height: 8rem;
}
.h3popupcontainer1content1 {
    position: absolute;
    top: 2.5rem;
    font-family: amerigobt;
    font-size: 22px;
    color: rgba(0, 0, 0, 0.811);
    letter-spacing: 0.02em;
    font-weight: 200;
    margin-right: 2rem;
    margin-top: 1rem;
}
.ppopupcontainer1content1{
    position: absolute;
    top: 5rem;
    
    font-family: amerigotbt;
    font-size: 17px;
    width: 18rem;
    letter-spacing: 0.03em;
    color: rgba(0, 0, 0, 0.628);


}
.secondpopup{
    position: absolute;
    top: 0rem;
    bottom: 0rem;
    left: 20rem;
    height: 31rem;
    width: 38rem;
    background-color: white;
    padding-left: 3rem;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(3, 1fr);

    padding-top: 2rem;
    
    margin-bottom: 0rem;
}
.secondpopupcont {
display:  flex;
flex-direction: column;
width: 17rem;
height: 6rem;
}

.secondpopupcont:hover {
    background-color: rgba(0, 0, 0, 0.046);
}

.secondpopupcont svg {
    position: relative;
    top: 0.5rem;


}

.secondpopupcont h3 {
    position: relative;
    top: -1.8rem;
    left: 1.8rem;
    font-family: amerigotbt;
    font-size: 14px;
    color: rgba(0, 0, 0, 0.667);
    letter-spacing: 0.03em;
    margin-bottom: -2rem;



}

.secondpopupcont p {
    position: relative;
    left: 1.8rem;
    top: 0rem;
    bottom: -10rem;
    font-family: amerigotbt;
    font-size: 13.5px;
    letter-spacing: 0.03em;
    color: rgba(0, 0, 0, 0.628);
    width: 15rem;

}



.templatecontainer {
    padding-bottom: 3rem;
    position: relative;
    top: 1.5rem;
    left: 20rem;
    margin-right: 6rem;
    z-index: -1;

}

.templatelink {
    font-family: amerigotbt;
    font-size: 17px;
    text-decoration: none;
    color: rgba(0, 0, 0, 0.669);
    letter-spacing: 1px;
}
.templatelink:hover {
    color: rgba(0, 0, 0, 0.959);
}
.templatepopup {
    position: absolute;
    top: 3rem;
    left: -16rem;
    height: 50rem;
    width: 26rem;
    background-color: white;
    padding-right: 2rem;
    padding-left: 3rem;
    box-shadow: 20px 20px 40px rgba(0, 0, 0, 0.03),
              -20px -20px 40px rgba(0, 0, 0, 0.03),
              20px -20px 40px rgba(0, 0, 0, 0.03),
              -20px 20px 40px rgba(0, 0, 0, 0.03);
    display: flex;
    flex-direction: column;  
}
.templatecontent1 {

}

.templatecontent1popup {
    position: absolute;
    top: 0rem;
    left: 30rem;
    height: 50rem;
    width: 40rem;
    background-color: white;
    display: flex;
    flex-direction: column;
    gap: 4rem;
    z-index: 0;
    transition: 10s;
    border-style: solid;
}

.templatecontent2popup {
    position: absolute;
    top: 0rem;
    left: 30rem;
    height: 50rem;
    width: 40rem;
    background-color: white;
    display: flex;
    flex-direction: column;
    gap: 4rem;
    z-index: 0;
    transition: 10s;
    border-style: solid;
}

.templatecontent3popup {
    position: absolute;
    top: 0rem;
    left: 30rem;
    height: 50rem;
    width: 40rem;
    background-color: white;
    display: flex;
    flex-direction: column;
    gap: 4rem;
    z-index: 0;
    transition: 10s;
    border-style: solid;
}

.pricingcontainer {
    padding-bottom: 3rem;
    position: relative;
    top: 1.5rem;
    left: 17rem;
    margin-right: 6rem;
}

.pricinglink {
    font-family: amerigotbt;
    font-size: 17px;
    text-decoration: none;
    color: rgba(0, 0, 0, 0.669);
    letter-spacing: 1px;
}

.reviewscontainer {
    padding-bottom: 3rem;
    position: relative;
    top: 1.5rem;
    left: 14rem;
    margin-right: 6rem;
}

.reviewslink {
    font-family: amerigotbt;
    font-size: 17px;
    text-decoration: none;
    color: rgba(0, 0, 0, 0.669);
    letter-spacing: 1px;
}

.login {


  color: #00b289;
  background-color: white;
  border-style: solid;
  border-color: #00b289;
  border-width: 0.5px;
  font-family: amerigotbt;
  font-weight: 600;
  padding: 11px;
  width: 5.8rem;
  border-radius: 4px;
  position: absolute;
    left: 59rem;
}
.login:hover {
    background-color: hsl(166, 100%, 36%);
    border-color: #00b289;
    color: white;
}

.startfree {
    color: white;
    background-color: #00b289;
    border-color: #00b289;
    border-style: solid;
    border-width: 0.5px;
    font-family: amerigotbt;
    font-weight: 600;
    padding: 11px;
    width: 8.5rem;
    border-radius: 4px;
    position: absolute;
    left: 65.8rem;
}
.startfree:hover {
    background-color: hsl(166, 100%, 30%);
    border-color: #00b289;
}


.bodycontainer {
    height: 100rem;
    overflow: hidden;
}
.backgroundbox {
    position: relative;
    left: 31rem;
    bottom: 23rem;
    width: 50rem;
    height: 50rem;
    background-color: rgb(230, 244, 253);
    rotate: -23deg;
    border-radius: 6rem;
    
}
</style>