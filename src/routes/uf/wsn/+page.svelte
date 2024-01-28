<script>
	import BigImage from "../../../components/big-image.svelte";
    import List from "../../../components/list.svelte";
    import Paragraph from "../../../components/paragraph.svelte";
    import Quote from "../../../components/quote.svelte";
</script>

<BigImage 
    link="https://images.pexels.com/photos/33153/raisting-sattelit-reception-signal.jpg?auto=compress&cs=tinysrgb&w=1920&h=1280&dpr=1"
    title="Wireless Sensor Networks"
/>

<div class="py-12 px-4 md:px-12 lg:px-48 xl:px-80">     
    <section>
        <h2 class="text-2xl py-2">Description</h2>
        <div class="py-2">
            <Paragraph>Wireless Sensor Networks consist of numerous tiny, resource-constrained devices equipped with sensing, computing, and communication capabilities. These sensors collaboratively gather and transmit data from their surroundings, forming a dynamic and interconnected network. The wireless nature of communication within these networks eliminates the need for cumbersome wired infrastructure, enabling flexible deployment in environments that were previously inaccessible or challenging.</Paragraph>
            <Paragraph>During this year we have to build a Physical and Mac layer protocol for an IOT application using GNU Radio. My team and I chose an application that can monitor. An application which is used to monitor a house and detect the fall of a person in it.My role was to develop the channel access method in python to create a new GNU Radio block.</Paragraph>
            <Paragraph>My role was to develop the channel access method in python to create a new GNU Radio block.</Paragraph>
        </div>
    </section>

    <section>
        <h2 class="text-2xl py-2">Technical</h2>
        <div class="py-2">
            <Paragraph>For the channel access method we choose Carrier Sense Multiple Access with Collision Avoidance (CSMA/CA). The main diffuclty was to understant who the GNU Python API work.</Paragraph>
            <div class="py-4 flex items-center justify-center gap-4">
                <div class="w-96">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/1/1d/Csma_ca.svg" alt="esp8266">
                    <p class="italic font-thin text-center py-2">
                        <a href="/https://www.google.com/url?sa=i&url=https%3A%2F%2Fen.wikipedia.org%2Fwiki%2FCarrier-sense_multiple_access_with_collision_avoidance&psig=AOvVaw0xqH2CuQbBGs9kl6oBnnwE&ust=1706191661940000&source=images&cd=vfe&opi=89978449&ved=0CBIQjRxqFwoTCNDDlbaZ9oMDFQAAAAAdAAAAABAe">CSMA/CA</a>
                    </p>
                </div>
            </div>
            <Paragraph>We choose this channel access, because there will be an important amount of sensors in the house.</Paragraph>
            <Paragraph>The Python execute a function on every samples, and we can modify these samples. To implement the CSMA/CA, I had to build the FFT on the channel we listen to detect if there are to detect if another sensor is emitting</Paragraph>
            <Paragraph>Now, I can detect if there are other sensors that emitting on the channel. The next step was just to develop the algorithm and to track the system state. As we the main function executes all the samples we can easily update the system.</Paragraph>
            <Paragraph>The main problem we had, was the time, because we didn't have time to assemble the Physical layer with the Mac layer.</Paragraph>

            <h3 class="text-md font-semibold">The knowledge and skills mobilized</h3>
        </div>
    </section>
</div>