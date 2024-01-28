<script>
	import { faChevronRight } from "@fortawesome/free-solid-svg-icons";
	import List from "../components/list.svelte";
import Paragraph from "../components/paragraph.svelte";
	import Fa from "svelte-fa";

</script>
<div class="py-12">
    <div class="flex gap-16 flex-col sm:flex-row">
        <div class="sm:w-1/4">
            <div class="py-4 border-b border-neutral-400">
                <h3 class="text-2xl">About me</h3>
                <div class="font-thin text-sm">
                    <Paragraph>I'm passionate about IT and web web development, I'm an inquisitive curious nature.</Paragraph>
                    <Paragraph>This allows me to develop my own projects.</Paragraph>
                </div>
                <div class="py-2 font-bold">
                    <p>Serious - Curious - Autonomous</p>
                </div>
            </div>
            <div class="py-4 border-b border-neutral-400">
                <h3 class="text-2xl">Programming Skills</h3>
                <div class="py-2">
                    <List>
                        <li class="py-2">HTML / CSS / JS</li>
                        <li class="py-2">C / C++ / C#</li>
                        <li class="py-2">Java</li>
                        <li class="py-2">Python</li>
                        <li class="py-2">Bash</li>
                    </List>
                </div>
            </div>
            <div class="py-4 border-b border-neutral-400">
                <h3 class="text-2xl">Web Technologies</h3>
                <div class="py-2">
                    <List>
                        <li class="py-2">NodeJs</li>
                        <li class="py-2">TypeScript</li>
                        <li class="py-2">NextJs / Svelte</li>
                        <li class="py-2">Tailwind</li>
                        <li class="py-2">Electron / Tauri</li>
                    </List>
                </div>
            </div>
            <div class="py-4 border-b border-neutral-400">
                <h3 class="text-2xl">Leisure</h3>
                <Paragraph>
                    <strong>High-level athlete</strong>
                </Paragraph>
                <div class="font-thin">
                    <Paragraph>Former high-level athlete in track and field, specialising in the 400m.</Paragraph>
                </div>
            </div>
        </div>
        <div class="flex-1">
            <div class="py-4 border-b border-neutral-400">
                <div class="flex items-baseline gap-2">
                    <Fa icon={ faChevronRight } />
                    <h3 class="text-2xl">Professional experience</h3>
                </div>
                <div class="py-2">
                    <div class="flex gap-8">
                        <div>
                            <span><strong>2021</strong></span>
                            <p>12 weeks</p>
                        </div>
                        <div class="flex-1">
                            <h3 class="text-xl">Internship at Orange Réunion</h3>
                            <div class="font-thin text-sm">
                                <Paragraph>Installation and maintenance of copper and fibre networks, installation telephony over IP and maintenance of the cellular network.</Paragraph>
                            </div>
                        </div>
                    </div>
                    <div class="flex gap-8">
                        <div>
                            <span><strong>2023</strong></span>
                            <p>12 weeks</p>
                        </div>
                        <div class="flex-1">
                            <h3 class="text-xl">Full Stack development</h3>
                            <div class="font-thin text-sm">
                                <Paragraph>Full stack development of an application with NexJs for the and NodeJs for the backend to certify an ISO 27001.</Paragraph>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="py-4 border-b border-neutral-400">
                <div class="flex items-baseline gap-2">
                    <Fa icon={ faChevronRight } />
                    <h3 class="text-2xl">Personal Experience</h3>
                </div>
                <div class="py-2">
                    <div class="display-grid">
                        <div>
                            <span><strong>2017-2024</strong></span>
                            <p>7 years</p>
                        </div>
                        <div class="flex-1">
                            <h3 class="text-xl">Game Developer</h3>
                            <div class="font-thin text-sm">
                                <Paragraph>With the help of my friends, we've already been able to create a number of games. This group initiative has enabled me to develop as a self-taught in this field. In fact, I continue to develop games in my spare time.</Paragraph>
                            </div>
                        </div>

                        <div>
                            <span><strong>2021</strong></span>
                            <p>6 months</p>
                        </div>
                        <div class="flex-1">
                            <h3 class="text-xl">Project Manager</h3>
                            <div class="font-thin text-sm">
                                <Paragraph>During my final year of the DUT, I was project manager for a team of of 9 people for 6 months. The aim of the project was to set up a cybersecurity laboratory for the Networks and Networks and Telecommunications department at my IUT.</Paragraph>
                            </div>
                        </div>

                        <div>
                            <span><strong>2022</strong></span>
                            <p>3 months</p>
                        </div>
                        <div class="flex-1">
                            <h3 class="text-xl">Creating a decentralised chat room</h3>
                            <div class="font-thin text-sm">
                                <Paragraph>Development of a fully decentralised Java chat application.</Paragraph>
                            </div>
                        </div>

                        <div>
                            <span><strong>2024</strong></span>
                        </div>
                        <div class="flex-1">
                            <h3 class="text-xl">Server management application</h3>
                            <div class="font-thin text-sm">
                                <Paragraph>Development of an application to manage my servers in the cloud in Svelte, NodeJs and Tauri.</Paragraph>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="py-4 border-b border-neutral-400">
                <div class="flex items-baseline gap-2">
                    <Fa icon={ faChevronRight } />
                    <h3 class="text-2xl">Formations</h3>
                </div>
                <div class="display-grid py-2">
                    <div>
                        <span><strong>2022-2024</strong></span>
                        <p>3 years</p>
                    </div>
                    <div class="flex-1">
                        <h3 class="text-xl">Institut National des Sciences Appliquées de Toulouse (INSA)</h3>
                        <div class="font-thin text-sm">
                            <Paragraph>Master 2 in Computer Science and Networks.</Paragraph>
                        </div>
                    </div>
                    
                    <div>
                        <span><strong>2019-2021</strong></span>
                        <p>2 years</p>
                    </div>
                    <div class="flex-1">
                        <h3 class="text-xl">Institut Universitaire de Technologie de la Réunion (IUT)</h3>
                        <div class="font-thin text-sm">
                            <Paragraph>DUT spécialité Networks et Telecommunication.</Paragraph>
                        </div>
                    </div>

                    <div>
                        <span><strong>2019</strong></span>
                    </div>
                    <div class="flex-1">
                        <h3 class="text-xl">Baccalauréat S lycée la salle Saint Charles</h3>
                        <div class="font-thin text-sm">
                            <Paragraph>Speciality SVT options Informatique et Science du Numérique.</Paragraph>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<style>
    .display-grid {
        display: grid;
        grid-template-columns: max-content 1fr;
        gap: 1rem;
    }
</style>