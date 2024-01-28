<script>
	import BigImage from "../../../components/big-image.svelte";
    import List from "../../../components/list.svelte";
    import Paragraph from "../../../components/paragraph.svelte";
	import Quote from "../../../components/quote.svelte";
</script>

<BigImage 
    link="https://images.pexels.com/photos/557782/pexels-photo-557782.jpeg?auto=compress&cs=tinysrgb&w=1920&h=1280&dpr=1"
    title="Cloud And Edge Computing"
/>

<div class="py-12 px-4 md:px-12 lg:px-48 xl:px-80"> 
    
    <section>
        <h2 class="text-2xl py-2">Description</h2>
        <div class="py-2">
            <Quote>“A cloud is an IT environment that separates, groups and shares IT resources on a network. An edge computing site is a computing location at the edge of a network that brings together hardware and software. Cloud computing involves running workloads in cloud environments, while edge computing involves running workloads on devices at the edge of the network”</Quote>
            <Paragraph>These days, cloud technologies are more and more used, with virtualisation and the growing use of connected objects.</Paragraph>
            <p class="py-2">This technology offers a number of advantages :</p>
            <List>
                <li>Scalability: Resources can be rapidly adjusted to meet changing needs</li>
                <li>Global accessibility: Users can access services from anywhere in the world</li>
                <li>Security: Cloud providers often invest heavily in data security</li>
            </List>
            <p class="py-2">Moreover, there's also a desire to bring data processing closer to the end nodes, like the Cloud Computing, Edge Computing also has a number of advantages:</p>
            <List>
                <li>Reduced latency: Data is processed locally, reducing transmission time</li>
                <li>Optimised bandwidth: Only relevant data is transmitted to the cloud, reducing network load</li>
                <li>Reliability: critical applications can run even when there is no connectivity to the cloud</li>
            </List>
        </div>
    </section>

    <section>
        <h2 class="text-2xl py-2">Technical</h2>
        <div class="py-2">
            <h3 class="text-md font-semibold">Hypervisor:</h3>
            <Paragraph>Acquire knowledge about the concept and techniques of virtualization. Discover various types of virtualization technologies, such as VM and containers, and test functionalities provided by Cloud providers as IaaS (Infrastructures as a Service).</Paragraph>
            <Paragraph>There are many tools for virtualisation, such as VirtualBox, VmWare, OpenStack, etc.</Paragraph>
            <Paragraph>For this course we have mainly used VirtualBox and OpenStack. VirtualBox is a Level 2 hypervisor and OpenStack is a Level 1 hypervisor.</Paragraph>
        
            <div class="py-4 flex items-center justify-center gap-4">
                <div class="w-96">
                    <img class="py-2" src="https://www.datocms-assets.com/17507/1606815700-tsilavo-ranarison-hyperviseur.jpg?fit=max&fm=webp&q=60&w=736" alt="type 1 vs type 2" />
                    <p class="italic font-thin text-center py-2">
                        <a href="https://www.appvizer.fr/magazine/services-informatiques/virtualisation/type-virtualisation">Type 1 vs Type 2</a>
                    </p>
                </div>
            </div>
        
            <Paragraph>We chose these solutions because they were already installed on INSA's machines.</Paragraph>
            <Paragraph>Now that we can virtualise a machine, we need to be able to communicate with it over the network.</Paragraph>
            <Paragraph>Hypervisors can be used to create virtual networks for VMs, so that they can communicate with each other. However, communication between a host outside this network is impossible.</Paragraph>
            
            <p class="py-2">To overcome this problem, hypervisors offer several solutions:</p>
            <List>
                <li>NAT</li>
                <li>Bridge acces</li>
                <li>Static IP</li>
            </List>
        
            <div class="py-4 flex items-center gap-4">
                <div class="flex-1">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/c/c7/NAT_Concept-en.svg" alt="NAT">
                    <p class="italic font-thin text-center py-2">
                        <a href="https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.nakivo.com%2Fblog%2Fvirtualbox-network-setting-guide%2F&psig=AOvVaw03HmNLSdBgdsj8YSPnQ9SV&ust=1705052950388000&source=images&cd=vfe&opi=89978449&ved=0CBQQjhxqFwoTCJix_rKH1YMDFQAAAAAdAAAAABAD">NAT</a>
                    
                    </p>
                </div>
        
                <div class="flex-1">
                    <img src="https://www.nakivo.com/blog/wp-content/uploads/2019/07/VirtualBox-network-settings-%E2%80%93-bridged-networking.webp" alt="Bridge">
                    <p class="italic font-thin text-center py-2">
                        <a href="https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.nakivo.com%2Fblog%2Fvirtualbox-network-setting-guide%2F&psig=AOvVaw03HmNLSdBgdsj8YSPnQ9SV&ust=1705052950388000&source=images&cd=vfe&opi=89978449&ved=0CBQQjhxqFwoTCJix_rKH1YMDFQAAAAAdAAAAABAD">Bridge</a>
                    </p>
                </div>
            </div>
        
            <Paragraph>With these solutions we can now communicate with the VM.</Paragraph>

            <h3 class="text-md font-semibold">Container:</h3>

            <Paragraph>Like a VM we can deploy a container using different technologies.</Paragraph>
            <Paragraph>There are various container solutions available on the market, with LCX Linux and Docker as two of the most used.</Paragraph>
            
            <p class="py-2">Why container over OS virtualisation?</p>
            <List>
                <li>Lighter</li>
                <li>Only virtualize the libraries</li>
                <li>Faster access to physical resources for the application</li>
                <li>Modular and high portability</li>
            </List>
            <div class="py-4 flex items-center justify-center gap-4">
                <div class="w-96">
                    <img src="https://www.docker.com/wp-content/uploads/2021/11/docker-containerized-appliction-blue-border_2.png" alt="Docker Container">
                    <p class="italic font-thin text-center py-2">
                        <a href="https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.nakivo.com%2Fblog%2Fvirtualbox-network-setting-guide%2F&psig=AOvVaw03HmNLSdBgdsj8YSPnQ9SV&ust=1705052950388000&source=images&cd=vfe&opi=89978449&ved=0CBQQjhxqFwoTCJix_rKH1YMDFQAAAAAdAAAAABAD">Bridge</a>
                    </p>
                </div>
            </div>

            <Paragraph>The main used of a container, is to isolate an application in his own environment. It's better in terms of security, scalability and portability.</Paragraph>
            <Paragraph>Like a virtualised machine, we can communicate with a container with the network. However, theire are in theire own network. We can use the same techniques as we saw before for network communication.</Paragraph>
        
            <h3 class="text-md font-semibold">Automation:</h3>
            <Paragraph>All the work we saw previously was done manually and can be very long. He can be cool, if we can deploy, configure or manage a VM or container with a script?</Paragraph>
            <Paragraph>The anwser is yes we can!</Paragraph>
            <Paragraph>We saw OpenStack Rest API and Docker Command Line API</Paragraph>
            
            <div class="py-4 flex items-center justify-center gap-4">
                <div class="w-96">
                    <img src="https://www.astera.com/wp-content/uploads/2020/01/rest.png" alt="Rest api">
                    <p class="italic font-thin text-center py-2">
                        <a href="https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.nakivo.com%2Fblog%2Fvirtualbox-network-setting-guide%2F&psig=AOvVaw03HmNLSdBgdsj8YSPnQ9SV&ust=1705052950388000&source=images&cd=vfe&opi=89978449&ved=0CBQQjhxqFwoTCJix_rKH1YMDFQAAAAAdAAAAABAD">Rest api</a>
                    </p>
                </div>
            </div>

            <Paragraph>With these API we can easily manage our VM or Container with a script writen in Python or Bash for exemple.</Paragraph>
        </div>
    </section>
    <section>
        <h2 class="text-2xl py-2">The knowledge and skills mobilized</h2>
        <div>
            <Paragraph>In this course I already know the used of an Rest api and the used of VirtualBox and how to communicate with a VM.</Paragraph>
            <Paragraph>However, I learn how to work with OpenStack and how we can scale, deploy, clone a VM on demand. Moreover, I learn how to use Docker and how I can isolate my application, because I create a lot of web application and now I know how I can isolate them withou creating another VM.</Paragraph>
        </div>
    </section>
</div>