<script lang="ts">
    import Highlight from "svelte-highlight";
    import typescript from "svelte-highlight/languages/typescript";
    import bash from "svelte-highlight/languages/bash";
    import atomOneDark from "svelte-highlight/styles/atom-one-dark";

    import Circuit from "../../../public/img/circuit.png";

	import BigImage from "../../../components/big-image.svelte";
    import List from "../../../components/list.svelte";
    import Paragraph from "../../../components/paragraph.svelte";
    import Quote from "../../../components/quote.svelte";

    const code: string = `const grpc = require("@grpc/grpc-js");
const device_grpc = require("@chirpstack/chirpstack-api/api/device_grpc_pb");
const device_pb = require("@chirpstack/chirpstack-api/api/device_pb");

// This must point to the ChirpStack API interface.
const server = "localhost:8080";

// The DevEUI for which we want to enqueue the downlink.
const devEui = "0101010101010101";

// The API token (can be obtained through the ChirpStack web-interface).
const apiToken = "...";


// Create the client for the DeviceService.
const deviceService = new device_grpc.DeviceServiceClient(
  server,
  grpc.credentials.createInsecure(),
);

// Create the Metadata object.
const metadata = new grpc.Metadata();
metadata.set("authorization", "Bearer " + apiToken);

// Enqueue downlink.
const item = new device_pb.DeviceQueueItem();
item.setDevEui(devEui);
item.setFPort(10);
item.setConfirmed(false);
item.setData(new Uint8Array([1, 2, 3]));

const enqueueReq = new device_pb.EnqueueDeviceQueueItemRequest();
enqueueReq.setQueueItem(item);

deviceService.enqueue(enqueueReq, metadata, (err, resp) => {
  if (err !== null) {
    console.log(err);
    return;
  }

  console.log("Downlink has been enqueued with id: " + resp.getId());
});`;
</script>

<svelte:head>
  {@html atomOneDark}
</svelte:head>

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

            <Paragraph>ChirpStack is an open-source LoRaWAN Network Server which can be used to setup LoRaWAN networks. ChirpStack provides a web-interface for the management of gateways, devices and tenants as well to setup data integrations with the major cloud providers, databases and services commonly used for handling device data.</Paragraph>
            <Paragraph>To retrieve the data, ChirpStack offers a Rest API, but we recommend using their gRPC API, which can easily be implemented in NodeJs : </Paragraph>
            <Highlight language={ typescript }  code={ code } /> 

            <div class="py-2">
                <a href="https://www.chirpstack.io/docs/chirpstack/api/js-examples.html" class="italic">
                    <center>ChirpStack exemple</center>
                </a>
            </div>

            <Paragraph>Unfortunately we didn't have time to create an interface to display the data.</Paragraph>
    </section>
    <section>
        <h2 class="text-2xl py-2">The knowledge and skills mobilized</h2>
        <div>
            <Paragraph>Overall, I really liked this uf, I was able to learn more about the design of a sensor from A to Z right through to its implementation. I also learned how to use a PCB modelling and design platform and how to use an open-source platform to retrieve data via LoRaWan.</Paragraph>
            <Paragraph>My knowledge of Arduino/C++ programming also meant that I didn't struggle too much with the programming of the microcontroller, which meant that we were able to complete this part quickly.</Paragraph>
        </div>
    </section>
</div>