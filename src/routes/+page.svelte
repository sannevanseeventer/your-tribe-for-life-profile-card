<script>
    import { SliceZone } from '@prismicio/svelte'
  
    import { components } from '$lib/slices'

    export let data
</script>



<section>
    <div class="card">
        <div class="container">
            <div class="name">   <h1>{data.name[0].text}</h1></div>
            <div class="job">    <h2>{data.job}</h2></div>
            <div class="savase"> <h3>{data.savase[0].text}</h3></div>
            <div class="icons">    
                <ul class="social">
                    <li><a href="https://www.linkedin.com/in/sanne-van-seeventer-51ab22bb/"><i class="ri-linkedin-box-fill"></i></a></li>
                    <li><a href="https://github.com/sannevanseeventer?tab=repositories"><i class="ri-github-fill"></i></a></li>
                    <li><a href="https://www.linkedin.com/in/sanne-van-seeventer-51ab22bb/"><i class="ri-mail-fill"></i></a></li>
                </ul>
            </div>
            <div class="phonenumber"><h4>{data.phonenumber}</h4></div>
            <div class="website"><h4>{data.website}</h4></div>
            <div class="content">  <p>Are you ready to go on a digital adventure with me? Let's create together and turn your digital dreams into reality.</p></div>
          </div>
        <div>
</div>
    </section>


<style>
@import url('https://fonts.googleapis.com/css2?family=Anton&family=Bebas+Neue&family=Kanit:ital,wght@0,400;0,600;1,500;1,600&family=Open+Sans&family=Poppins:wght@800&family=Roboto:wght@900&display=swap');

*{
    font-family: 'Bebas Neue', sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.container { 
display: grid;
  grid-template-columns: 0.3fr 1.7fr;
  grid-template-rows: 1fr 1fr 1fr 1fr 1fr 1fr 1fr;
  gap: 0;
  outline: 1px solid black;
  grid-auto-flow: row;
  grid-template-areas:
    "name name"
    "job job"
    "savase icons"
    "savase phonenumber"
    "savase content"
    "savase content"
    "website website";
}

.name { grid-area: name;
    border: 1px solid black; }

.job { grid-area: job;
    border: 1px solid black; }

.savase { 
    grid-area: savase;
    border: 1px solid black;
}

.icons { grid-area: icons;
    border: 1px solid black;
 }

.phonenumber { grid-area: phonenumber;
    border: 1px solid black; }

.website { grid-area: website;
    border: 1px solid black; }

.content { grid-area: content;
    border: 1px solid black; }

.social{
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 2rem;
    margin-top: 1rem;
    cursor: pointer;
}

.savase h3{
    font-family: "kanit";
    font-weight: 600;
    font-style: italic;
    writing-mode: vertical-lr;
    font-size: 2.5rem;
    color:rgb(0, 0, 0);
    -webkit-text-fill-color: transparent;
    -webkit-text-stroke: 2px rgb(0, 0, 0);
    letter-spacing: .3rem;
    margin-top: 1.5rem;
    margin-bottom: 1.5rem;
    text-transform: uppercase;
}

.card h4{
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 1rem;
    letter-spacing: .3rem;
}

.social li{
    text-decoration: none;
    list-style-type: none;
}

a{
    text-decoration: none;
    color: black;
    font-size: 1.3rem;
}

.card{
    width: 300px;
    height: auto;
    background: #efefef;
    box-shadow: 2px 1px 9px 1px rgb(188, 188, 188);
    padding: 1rem; 
    text-align: left;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    overflow: hidden;
}

.card:before{
    position: absolute;
    content: "";
    width: 200px;
    height: 200px;
    background: rgb(142, 227, 255);
    bottom: -100px;
    right: -100px; 
    z-index: -1;
    rotate: 45deg;
    transition: 5s;
}

.card:hover:before{
    transform: scale(100);
}

.card h1{
text-transform: uppercase;
text-align: center;
margin-top: 0.9rem;
letter-spacing: .2rem;
font-size: 1.35rem;
}

.card h2{
    font-family: "Kanit";
text-transform: uppercase;
text-align: center;
margin-top: 1.2rem;
letter-spacing: .2rem;
font-size: .5rem;
}

.card p{
font-family: "Kanit";
text-transform: uppercase;
text-align: left;
margin: 1.5rem;
letter-spacing: .1rem;
font-size: 0.5rem;
}









</style>