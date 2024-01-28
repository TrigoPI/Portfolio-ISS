<script>
	import BigImage from "../../../components/big-image.svelte";
    import List from "../../../components/list.svelte";
    import Paragraph from "../../../components/paragraph.svelte";
    import Quote from "../../../components/quote.svelte";
</script>

<BigImage 
    link="https://images.pexels.com/photos/6325001/pexels-photo-6325001.jpeg?auto=compress&cs=tinysrgb&w=1920&h=1280&dpr=1"
    title="5G Technologies"
/>

<div class="py-12 px-4 md:px-12 lg:px-48 xl:px-80"> 
    <section>
        <h2 class="text-2xl py-2">Description</h2>
        <div class="py-2">
            <Paragraph>In the ever-evolving landscape of telecommunications, the advent of the fifth generation of wireless technology, commonly known as 5G, has emerged as a transformative force poised to redefine connectivity on a global scale. As society becomes increasingly reliant on seamless and high-speed communication, 5G promises to revolutionize the way we connect, communicate, and interact with the digital world.</Paragraph>
            <Paragraph>It offers a number of advantages</Paragraph>
            <List>
                <li><strong>Increased Data Speeds</strong></li>
                <li><strong>Low Latency</strong></li>
                <li><strong>Greater Network Capacity</strong></li>
                <li><strong>Enhanced Connectivity in Dense Areas</strong></li>
                <li><strong>Improved Energy Efficiency</strong></li>
                <li><strong>Support for Diverse Use Cases</strong></li>
                <li><strong>Global Connectivity and Standardization</strong></li>
            </List>
        </div>
    </section>

    <section>
        <h2 class="text-2xl py-2">Technical</h2>
        <div class="py-2">
            <Paragraph>In this courses, my group decided to focus on <strong>Apple and 6G.</strong></Paragraph>
            <Paragraph>What is 6G?</Paragraph>
            <Paragraph>6G technology was still in the conceptual and early research stages. Is envisioned as the next generation of wireless communication technology that would succeed 5G.</Paragraph>
            <Paragraph>Here is some key features and potential characteristics of 6G: </Paragraph>
            <List>
                <li><strong>Higher Data Speeds</strong></li>
                <li><strong>Ultra-Low Latency</strong></li>
                <li><strong>AI Integration</strong></li>
                <li><strong>Energy Efficiency</strong></li>
                <li><strong>Global Connectivity and Interoperability</strong></li>
            </List>
        </div>
    </section>
</div>