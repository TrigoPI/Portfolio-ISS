<script>
	import BigImage from "../../../components/big-image.svelte";
    import List from "../../../components/list.svelte";
    import Paragraph from "../../../components/paragraph.svelte";
	import Quote from "../../../components/quote.svelte";
</script>

<BigImage 
    link="https://images.pexels.com/photos/1990764/pexels-photo-1990764.jpeg?auto=compress&cs=tinysrgb&w=1920&h=1277&dpr=1"
    title="Security"
/>

<div class="py-12 px-4 md:px-12 lg:px-48 xl:px-80"> 
    
    <section>
        <h2 class="text-2xl py-2">Description</h2>
        <div class="py-2">
            <Paragraph>By the end of 2023, reports estimate the world will have over 16.7 billion connected Internet of Things devices. This means there will be a tremendous amount of potentially vulnerable targets if they are not properly protected. As the world continues to implement more networks, the importance of IoT security will grow in order to maintain confidence in such devices and systems.</Paragraph>
            <Paragraph>This year we have to design a secure communication protocol for our innovative project. This year we have to design a secure communication protocol for our innovative project. However, as our project has no critical data to transport, we have decided to focus more on the RGPD side of the system. As the aim of our system is to take photos automatically, we have to comply with certain legal requirements.</Paragraph>
        </div>
    </section>

    <section>
        <h2 class="text-2xl py-2">Technical</h2>
        <div class="py-2">
            <Paragraph>Given that our system will be installed in the wild, the first thing we did was disable wifi and bluetooth on our system. In addition, the photos will be stored in an encrypted partition and if a human is detected in a photo, the photo will be automatically deleted. Communication between micro services is also only possible via the system controller and is therefore not accessible from the outside except via the application.</Paragraph>
            <Paragraph>In addition to our innovative project, we also had the opportunity to take part in some hacking challenges based on SQL and XSS injection.</Paragraph>
        </div>
    </section>
    <section>
        <h2 class="text-2xl py-2">The knowledge and skills mobilized</h2>
        <div class="py-2">
            <Paragraph>On the whole, I enjoyed the course, even though I'd already seen some of the concepts in 4th year. I'd already done some SQL and XSS injections on the RootMe site, but it never hurts to see how it works again. What's more, I discovered how to create and make a secure protocol, as well as how to detect potential flaws that an attacker could exploit to break the protocol.</Paragraph>
        </div>
    </section>
</div>