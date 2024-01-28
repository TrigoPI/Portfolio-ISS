<script>
    import Circuit from "../../../public/img/circuit.png";

	import BigImage from "../../../components/big-image.svelte";
    import List from "../../../components/list.svelte";
    import Paragraph from "../../../components/paragraph.svelte";
    import Quote from "../../../components/quote.svelte";
</script>

<BigImage 
    link="https://images.pexels.com/photos/3520692/pexels-photo-3520692.jpeg?auto=compress&cs=tinysrgb&w=1920&h=1277&dpr=1"
    title="Smart Devices"
/>

<div class="py-12 px-4 md:px-12 lg:px-48 xl:px-80">  
    
    <section>
        <h2 class="text-2xl py-2">Description</h2>
        <div class="py-2">
            <Paragraph>For this part, I will bundle Microcontrollers and Open-Source Hardware, Embedded IA (M&OSH), CAD, manufacturing and integration of nano-technology sensors (AIME), Sensors introduction, Analog electronic labs.</Paragraph>
            <Paragraph>During this years we have to fully implement a smart device application, from sensor construction to the application. we achieved this goal through several steps: </Paragraph>
            <List>
                <li><strong>Create the sensor in the white room</strong></li>
                <li><strong>Design the circuit to comminucate with the microcontroller</strong></li>
                <li><strong>Design the PCB</strong></li>
                <li><strong>Lora communication for datas transmission</strong></li>
                <li><strong>Web application for displaying the datas</strong></li>
            </List>

            <Paragraph>For this project I work in a group of two, so I don't have a specific role.</Paragraph>
        </div>
    </section>

    <section>
        <h2 class="text-2xl py-2">Technical</h2>
        <div class="py-2">
            <Paragraph>The first step was to build the gaz sensor that needs the synthesis of nanoparticles, the active zone of capture of nanoparticles, the deposition of nanoparticles by dielectrophoresis until the contact of the cell. For this, we had 3 days to create the sensor. Unfortunately none of our sensors worked in the end, because the chimical formula used to detect a gaz leak in our sensors wasn't good enougth this year.</Paragraph>
            <Paragraph>The second step was to create a transimpedance amplifier to connect the gaz sensor to the microcontroller. The dising and simulation of the circuit was done on LtSpice : </Paragraph>
            
            <div class="py-4 flex items-center justify-center gap-4">
                <div class="max-w-2xl">
                    <img src={ Circuit } alt=" transimpedance amplifier">
                    <p class="italic font-thin text-center py-2">
                        <span> transimpedance amplifier</span>
                    </p>
                </div>
            </div>
        
            <Paragraph>After that, we can create the PCB with the circuit that we have just made with KiCad. It was the first time I created a PCB as a IR student and unfortunately we didn't have the time to finish the PCB.</Paragraph>
            <Paragraph>Normally, after creating the PCB, we had to send data over LoRa. To do that we used a LoRa module connected to an Arduino and and the ChirpStack platform.</Paragraph>
        
            <div class="py-4 flex items-center justify-center gap-4">
                <div class="w-96">
                    <img src="https://miro.medium.com/v2/resize:fit:1358/0*w4sts4D8kJ2SsOwT" alt="ChirpStack">
                    <p class="italic font-thin text-center py-2">
                        <a href="https://www.google.com/url?sa=i&url=https%3A%2F%2Fmedium.com%2F%40hendraputra%2Fhow-to-access-chirpstack-api-d9643a282c07&psig=AOvVaw32DnWcCh1h4HJn2axv3Sl2&ust=1706523880745000&source=images&cd=vfe&opi=89978449&ved=0CBIQjRxqFwoTCPDPx4bv_4MDFQAAAAAdAAAAABAy">ChirpStack</a>
                    </p>
                </div>
            </div>
        </div>
    </section>
</div>