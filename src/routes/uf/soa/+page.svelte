<script lang="ts">
    import "svelte-highlight/styles/github.css";

    import Highlight from "svelte-highlight";
    import typescript from "svelte-highlight/languages/typescript";
    import bash from "svelte-highlight/languages/bash";
    import atomOneDark from "svelte-highlight/styles/atom-one-dark";

    import BigImage from "../../../components/big-image.svelte"
    import List from "../../../components/list.svelte";
    import Paragraph from "../../../components/paragraph.svelte";
    import Quote from "../../../components/quote.svelte";

    let codeMain: string = `@EntryPoint(path_to_microservices_folder)
class Main {
    public async Start(): Promise<void> {
        //This function is executed when the application start
    }

    public static async CreateApplication(): Promise<void> {
        //create your application here
        const app: Main = new Main();
        await app.Start();
    }
}
`

    let codeLoad: string = `const luncher: ServiceLuncher = ServiceLuncher.GetInstance();
await luncher.LoadServices();
await luncher.StartService(service_name);
//or
await luncher.StartAllServices();
`

    let codeServicePath: string = `services_folder
        |
        |--> service1
            |
            |-->service.ts
        |
        |-->service2
            |
            |-->service.ts
    `

    let codeService: string = `@Service("test", "/test", "localhost", "8080")
export default class TestService extends ServiceClass {
    public override async OnStart(): Promise<void> {
        //Function executed before the http server of this service start
    }

    public override async OnShutdown(): Promise<void> {
        //Function executed before we shutdown the service
    }
}`

    let codeRoute: string = `@Get
@Route("/route_test")
public async GetServicesDesc(): Promise<Response> {
    return Response.Ok();
}
`

</script>

<svelte:head>
  {@html atomOneDark}
</svelte:head>

<BigImage 
    link="https://images.pexels.com/photos/1029604/pexels-photo-1029604.jpeg?auto=compress&cs=tinysrgb&w=1920&h=1280&dpr=1"
    title="Service Oriented Architecture"
/>

<div class="py-12 px-4 md:px-12 lg:px-48 xl:px-80">    
    <section>
        <h2 class="text-2xl py-2">Description</h2>
        <div class="py-2">
            <Quote>Service Oriented Architecture (SOA) is an architectural approach that encourages the creation of modular, flexible and interoperable software systems. A service, in this context, is a logical unit of functionality that is well-defined, self-sufficient and can be reused in various contexts within an application or between different applications.</Quote>
            <Paragraph>It offers a number of advantages that make it attractive for the design and development of software systems:</Paragraph>
            <List>
                <li><strong>Reusability:</strong> Individual services in an SOA are designed to be reusable.</li>
                <li><strong>Modularity:</strong> SOA promotes modularity by breaking down a system into distinct services.</li>
                <li><strong>Ease of integration:</strong> Facilitates the integration of disparate systems by enabling distinct services to communicate with each other via well-defined contracts.</li>
                <li><strong>Better resource management:</strong>Enables resources to be used efficiently by avoiding duplication of functionality and enabling it to be reused across different parts of the business.</li>
                <li><strong>Ease of maintenance:</strong>Modularity, updates and corrections can be carried out more easily on individual services without affecting the whole system</li>
            </List>
        </div>
    </section>

    <section>
        <h2 class="text-2xl py-2">Technical</h2>
        <div class="py-2">
            <Paragraph>My group and I, decided to work on the software architecture for our innovative project. The main problem of our project was the modularity of our sofware. For exemple, if we add a new sensor or decide to change one.</Paragraph>
            <Paragraph>The goal was to develop a sofware we can easily modify/configure. With SOA we can achieve this goal. The most modular solution we've found, is, for each sensor, to create a micro-service in the sofware.</Paragraph>
            <Paragraph>For the microservices, we decided to use NodeJs with TypeScript, because TypeScript offert a feature called "decorator" that can add medatadas in a class. With that, I created a library called <strong>Dolphin 🐬</strong> for microservices development.</Paragraph>
            <Paragraph>The fonctionnalities of my library was inspired by a Java library. To work, we have to split the code in two parts: </Paragraph>
            <List>
                <li>Entry Point</li>
                <li>Services</li>
            </List>

            <h3 class="text-md font-semibold py-4">Entry Point</h3>
            <Paragraph>I will strart with the entry point. The entry point is where the program will start and load the mircroservices. To define the entry point we just have to define a class with the decorator: </Paragraph>
            <Highlight language={ typescript }  code={ codeMain } /> 

            <Paragraph>Now we will have to load your microservice in the <strong>Start function</strong>: </Paragraph>
            <Highlight language={ typescript }  code={ codeLoad } /> 

            <Paragraph>The <strong>ServiceLuncher</strong> will look in the folder we have defined in <strong>@EntryPoint</strong> and load all the services.</Paragraph>

            <h3 class="text-md font-semibold py-4">Services</h3>
            <Paragraph>All your services must be named <strong>service.ts</strong> and can be in the root folder we want:</Paragraph>
            <Highlight language={ bash } code={ codeServicePath } />

            <Paragraph>Like the entry point, to define a service we first must create a class thath extends <strong>ServiceClass</strong> with the decorator <strong>@Service(service_name, service_base_route, service_ip, service_port)</strong>: </Paragraph>
            <Highlight language={ typescript }  code={ codeService } /> 

            <Paragraph>And now we can create a function for each route we want in this class: </Paragraph>
            <Highlight language={ typescript }  code={ codeRoute } /> 

            <Paragraph>As you can see we use multiple decorator. This function will be executed on a http GET request when the route is /test/route_test and will return a Response, in our case it will be a http response with code 200.</Paragraph>
            <Paragraph>My library support for now, just POST and GET requests but other request will be added in the future.</Paragraph>

            <Paragraph>Now we can create a microservice for each sensors, the next step is, to create the architecture for microservices communication and configuration.</Paragraph>
            <Paragraph>For that, we created a controller that can communicate with all the microservices and a web interface to configure them.</Paragraph>
            <Quote>Mettre une image de Tetras API</Quote>
            <Paragraph>Now with that, for each new sensor we add on our system, we just have to develop the micro-service associated and the sofware will take care of the new micro-service. You can find a more detail explanation in the report.</Paragraph>
        
            <h3 class="text-md font-semibold">The knowledge and skills mobilized</h3>
            <Paragraph>I already know about Rest api and how that work. I use my knowlege of Web technologies like TypeScript and Express to easily build an api and use some advanced JavaScript features, like hot reloading (reloading a file without having to restart the application).</Paragraph>
        </div>
    </section>
</div>