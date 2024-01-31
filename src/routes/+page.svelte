<script lang="ts">
    import { base } from "$app/paths";

    import { faBolt, faBrain, faCircleNodes, faCloud, faGlobe, faHouseSignal, faLock, faNetworkWired, faTowerCell, faUser } from "@fortawesome/free-solid-svg-icons";
	import { faAndroid } from "@fortawesome/free-brands-svg-icons";

	import Chapter from "./chapter.svelte";
	import Cv from "./cv.svelte";
	import Paragraph from "../components/paragraph.svelte";

</script>

<div class="welcome relative w-screen h-screen flex flex-col gap-8 items-center justify-center overflow-hidden">
    <h1 class="slide-in-top text-5xl text-center font-bold sm:text-9xl text-white">Welcome to my portfolio</h1>
    <h3 class="slide-in-top text-xl text-white sm:text-3xl">I'm Payet Alexis</h3>
</div>
<div class="py-28 px-4 md:px-12 lg:px-48 xl:px-80">
    <section>
        <div class="flex flex-col gap-4 justify-between sm:flex-row">
            <h2 class="text-5xl">Introduction</h2>
            <p class="text-xl text-justify sm:w-8/12">Hey!! Welcome to my portfolio, I'm a 5ISS student at INSA Toulouse. I chose this orientation because it has the most modules that I liked related to web development that I liked related to web development. In this portfolio I will describe what I did this semester. I invite you to explore my portfolio, where you'll find a collection of my work.</p>
        </div>
    </section>


    <section>
        <div class="py-12">
            <h2 class="text-5xl py-2">Curriculum Vitae</h2>
            <Cv />
        </div>
    </section>

    <section>
        <h2 class="text-5xl pt-4 pb-12">Chapters</h2>
        <div class="chapters-grid justify-center">
            <Chapter 
                title="Service Oriented Architecture"
                link="{base}/uf/soa"
                icon={ faGlobe }
            />
            <Chapter 
                title="Machine to Machine"
                link="{base}/uf/m2m"
                icon={ faAndroid }
            />
            <Chapter 
                title="5G Technologies"
                link="{base}/uf/5g"
                icon={ faTowerCell }
            />
            <Chapter 
                title="Cloud And Edge Computing"
                link="{base}/uf/cloud"
                icon={ faCloud }
            />
            <Chapter 
                title="Wireless Sensor Networks"
                link="{base}/uf/wsn"
                icon={ faCircleNodes }
            />
            <Chapter 
                title="smart-devices"
                link="{base}/uf/smart-devices"
                icon={ faHouseSignal }
            />
            <Chapter 
                title="AI"
                link="{base}/uf/ai"
                icon={ faBrain }
            />
            <Chapter 
                title="Security"
                link="{base}/uf/security"
                icon={ faLock }
            />
            <Chapter 
                title="Skills Matrix"
                link="https://drive.google.com/drive/folders/1EnVcJqeLoouSE7C2lwz3xo8-MWrAQmC7?usp=drive_link"
                icon={ faBolt }
            />
        </div>
    </section>

    <section>
        <h2 class="text-5xl py-2">Conclusion</h2>
        <div class="py-2">
            <Paragraph>When I started at INSA, I wanted to do networking, but as time went by I realized that web development interested me more and more, and that's why I chose ISS, as it encompassed most of the subjects I was interested in.</Paragraph>
        </div>
    </section>
</div>

<style>
    .welcome {
        background-image: url(https://images.pexels.com/photos/167684/pexels-photo-167684.jpeg?cs=srgb&dl=pexels-lumn-167684.jpg&fm=jpg&w=1920&h=1280);
    }

    .chapters-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, 15rem);
        grid-auto-rows: 15rem;
        gap: 2rem;
    }
</style>