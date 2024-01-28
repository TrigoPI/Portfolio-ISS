<script>
	import BigImage from "../../../components/big-image.svelte";
    import List from "../../../components/list.svelte";
    import Paragraph from "../../../components/paragraph.svelte";
	import Quote from "../../../components/quote.svelte";
</script>

<BigImage 
    link="https://images.pexels.com/photos/3785931/pexels-photo-3785931.jpeg?auto=compress&cs=tinysrgb&w=1920&h=1277&dpr=1"
    title="Machine To Machine"
/>

<div class="py-12 px-4 md:px-12 lg:px-48 xl:px-80">     
    <section>
        <h2 class="text-2xl py-2">Description</h2>
        <div class="py-2">
            <Quote>"The concept of machine to machine, sometimes abbreviated by the sign m2m, uses telecommunications and computing to allow communications between machines, without human intervention."</Quote>
            <Paragraph>Deployment of Machine-to-Machine technology is growing significantly these days due to several factors:</Paragraph>
            <List>
                <li>Industrial Process Automation.</li>
                <li>Internet Of Things.</li>
                <li>Improved Resource Management.</li>
                <li>Energetic efficiency.</li>
            </List>
    
            <Paragraph>Its ability to enable communication between machines and provide real-time information plays a crucial role in the digital transformation of many industries.</Paragraph>
            <Paragraph>Yeah, all these features, but, how can machines communicate between each others?</Paragraph>
        </div>
    </section>

    <section>
        <h2 class="text-2xl py-2">Technical</h2>
        <div class="py-2">
            <Paragraph>The main objectives was to discover differents technologies for m2m.</Paragraph>

            <h3 class="text-md font-semibold">MQTT:</h3>
            <Paragraph>MQTT (Message Queuing Telemetry Transport) is a lightweight and efficient communications protocol designed for environments where network bandwidth and reliability are important concerns.</Paragraph>
            <Paragraph>This technology work with a Publish/Subscribe system:</Paragraph>
            <div class="py-4 flex items-center justify-center gap-4">
                <div class="w-96">
                    <img src="https://hlassets.paessler.com/common/files/infographics/mqtt-architecture.png" alt="MQTT">
                    <p class="italic font-thin text-center py-2">
                        <a href="https://www.paessler.com/fr/it-explained/mqtt">MQTT</a>
                    </p>
                </div>
            </div>

            <Paragraph>Why MQTT?</Paragraph>
            <List>
                <li>Low Bandwidth</li>
                <li>Reliability</li>
                <li>Light and Simple</li>
                <li>Easy Integration with other Technologies</li>
            </List>

            <Paragraph>We implemented the MQTT protocol with Mosquitto for the broker. Mosquitto is an open source message broker that implements the MQTT protocol.</Paragraph>
            <Paragraph>We used an esp8266 and MQTT library for messaging and decoding.</Paragraph>

            <div class="py-4 flex items-center justify-center gap-4">
                <div class="w-96">
                    <img src="https://m.media-amazon.com/images/I/6110Sqg1AqL._AC_UF1000,1000_QL80_.jpg" alt="esp8266">
                    <p class="italic font-thin text-center py-2">
                        <a href="/m2m">esp8266</a>
                    </p>
                </div>
            </div>
        </div>

        <h3 class="text-md font-semibold">OneM2M:</h3>
        <Paragraph>One of the major problem with IOT is, the diversity of protocols.</Paragraph>
        <Paragraph>That why OneM2M enter the game. The goal of the organization is to create a global technical standard for interoperability concerning the architecture, API specifications, security and enrolment solutions for Machine-to-Machine and IoT technologies.</Paragraph>
        <Paragraph>Here is somes features of OneM2M:</Paragraph>
        <List>
            <li><strong>Modular Architecture</strong></li>
            <li><strong>Resource Management</strong></li>
            <li><strong>Scalability</strong></li>
        </List>
        
        <Paragraph>For this part, we just discovered how to use the protocol via a notebook.</Paragraph>
    </section>
</div>