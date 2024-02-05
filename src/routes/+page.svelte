<script lang="ts">
    import { base } from "$app/paths";

    import { faBolt, faBrain, faCircleNodes, faCloud, faFolder, faGlobe, faHouseSignal, faLock, faNetworkWired, faTowerCell, faUser } from "@fortawesome/free-solid-svg-icons";
	import { faAndroid } from "@fortawesome/free-brands-svg-icons";

	import Chapter from "./chapter.svelte";
	import Cv from "./cv.svelte";
	import Paragraph from "../components/paragraph.svelte";
	import Fa from "svelte-fa";

</script>

<div class="welcome relative w-screen h-screen flex flex-col gap-8 items-center justify-center overflow-hidden">
    <h1 class="slide-in-top text-5xl text-center font-bold sm:text-9xl text-white">Welcome to my portfolio</h1>
    <h3 class="slide-in-top text-xl text-white sm:text-3xl">I'm Payet Alexis</h3>
</div>
<div class="py-28 px-4 md:px-12 lg:px-48 xl:px-80">
    <section>
        <div class="flex flex-col gap-4 justify-between sm:flex-row">
            <h2 class="text-5xl">Introduction</h2>
            <p class="text-xl text-justify sm:w-8/12">Hey!! Welcome to my portfolio, I'm a 5ISS student at INSA Toulouse. I chose this orientation because it has the most modules that I liked related to web development. In this portfolio I will describe what I did this semester. I invite you to explore my portfolio, where you'll find a collection of my work. Enjoy 🦫</p>
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
        <div class="chapters-grid py-12 justify-center">
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
            <a 
                href="https://docs.google.com/spreadsheets/d/1PZVjrCK6dcHxQr1n-zz10F3lho7dfKMW/edit?usp=drive_link&ouid=109299935010732913269&rtpof=true&sd=true"
                class="flex flex-col items-center gap-4 rounded-md px-12 py-8 shadow-lg duration-150 hover:scale-110"
            >
                <div class="px-4 text-2xl border-b flex-1">
                    <h1 class="text-center py-2">Skill Matrixs</h1>
                </div>
                <div class="text-3xl py-4">
                    <Fa icon={ faBolt } />
                </div>
            </a>
            <a 
                href="https://drive.google.com/drive/folders/15NRXU-UHsJvPkJG8JdqNPmcRUBxMzVuv?usp=drive_link"
                class="flex flex-col items-center gap-4 rounded-md px-12 py-8 shadow-lg duration-150 hover:scale-110"
            >
                <div class="px-4 text-2xl border-b flex-1">
                    <h1 class="text-center py-2">Repports</h1>
                </div>
                <div class="text-3xl py-4">
                    <Fa icon={ faFolder } />
                </div>
            </a>
        </div>
    </section>

    <section>
        <h2 class="text-5xl py-2">Conclusion</h2>
        <div class="py-2">
            <Paragraph>When I started at INSA, I wanted to do networking, but as time went by I realized that web development interested me more and more, and that's why I chose ISS, as it encompassed most of the subjects I was interested in.</Paragraph>
            <Paragraph>When I arrived at ISS I thought I wasn't going to like the more electronics-oriented subjects, but in the end I rather enjoyed them even though I don't have a great deal of expertise in this subject. Even if I wouldn't be able to make complex circuits, I at least think I have the skills to understand how it works if it's explained to me.</Paragraph>
            <Paragraph>What I also really enjoyed was working with people from different backgrounds. Even if some subjects are more oriented towards one field, each person has a different point of view depending on their orientation. This was particularly evident in the innovative project, where each member of our group was able to contribute his or her expertise, whether in electronics or software.</Paragraph>
            <Paragraph>I've been meaning to do a portfolio for a long time, but in the end I never got round to it because I wasn't sure what to put in it. I think I'll continue to update this portfolio as the years go by, but I'll just put projects that are more related to what I want to do.</Paragraph>
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