<script>
	import BigImage from "../../../components/big-image.svelte";
    import List from "../../../components/list.svelte";
    import Paragraph from "../../../components/paragraph.svelte";
    import Quote from "../../../components/quote.svelte";
</script>

<BigImage 
    link="https://images.pexels.com/photos/17485678/pexels-photo-17485678/free-photo-of-climat-abstrait-technologie-rechercher.png?auto=compress&cs=tinysrgb&w=1920&h=1080&dpr=1"
    title="Embedded AI"
/>

<div class="py-12 px-4 md:px-12 lg:px-48 xl:px-80"> 
    <section>
        <h2 class="text-2xl py-2">Description</h2>
        <div class="py-2">
            <Paragraph>Embedded AI, is a general-purpose framework system for AI functions. It is built into network devices and provides common model management, data obtaining, and data preprocessing functions for AI algorithm-based functions for these devices.</Paragraph>
            <Paragraph>As an IR, we already have courses on AI, but not on embedded ia, even if the principles remain the same. This was very useful in the case of our innovative project. In fact, in our project we had to do image recognition at node level with AI, but with the courses we saw last year, the models obtained would have been too heavy and too energy-consuming.We therefore need to apply what we have seen in this course in order to be able to run an embedded AI on our system.</Paragraph>
        </div>
    </section>

    <section>
        <h2 class="text-2xl py-2">Technical</h2>
        <div class="py-2">
            <Paragraph>The aim of our system is to detect the capercaillie in the photos it takes. However, our system is installed in the mountains and is supposed to be able to run all winter on battery power. Running a large AI model would have consumed too much energy for image recognition.</Paragraph>
            
            <div class="py-4 flex items-center justify-center gap-4">
                <div class="w-96">
                    <img src="https://pyrenees-parcnational.fr/sites/pyrenees-parcnational.fr/files/styles/slide_1500_1000/public/tetras3.jpg?itok=ZB33C0tm" alt="Grand Tetras">
                    <p class="italic font-thin text-center py-2">
                        <a href="pyrenees-parcnational.fr/sites/pyrenees-parcnational.fr/files/styles/slide_1500_1000/public/tetras3.jpg?itok=ZB33C0tm">Grand Tetras</a>
                    </p>
                </div>
            </div>
            
            <Paragraph>That's why we've applied the various techniques we've seen in this course to reduce the size and calculation time of our model as much as possible. Unfortunately, due to a lack of time and the fact that this course comes quite late in the year, we haven't had time to really implement AI on the system, but here are the different stages we've thought of.</Paragraph>
            <Paragraph>The first step would have been to find a dataset to be able to recognise the capercaillie, but unfortunately for us, we didn't find any dataset that met our needs. One of the solutions we could have used to create our dataset would have been to scrape google image to create our own dataset. However, this solution would have required the dataset to be manually cleaned and labelled.</Paragraph>
            <Paragraph>To reduce the size of the images, we also thought about reducing the resolution and just taking the contours of the image. And then train a model with these images.</Paragraph>
            <Paragraph>Once our model has been trained to a success rate that suits us. The next step we should have taken was pruning to reduce the size of our model.</Paragraph>
        
            <div class="py-4 flex items-center justify-center gap-4">
                <div class="w-96">
                    <img src="https://www.quantmetry.com/wp-content/uploads/2021/02/illusatration-methodes.png" alt="Grand Tetras">
                    <p class="italic font-thin text-center py-2">
                        <a href="https://www.quantmetry.com/wp-content/uploads/2021/02/illusatration-methodes.png">Pruning</a>
                    </p>
                </div>
            </div>

            <Paragraph>And finally, the last stage would have been to test our model on our on-board system and measure energy consumption.</Paragraph>
        </div>
    </section>
    <section>
        <h2 class="text-2xl py-2">The knowledge and skills mobilized</h2>
        <div>
            <Paragraph>I didn't work on this part of our project, as my part was more centred on the development of the project.</Paragraph>
            <Paragraph>However, I enjoyed the AI course more because it was more practical than theoretical. In fact, I discovered how to do image recognition and also saw some algorithms (DTW) that could be useful for certain projects.</Paragraph>
        </div>
    </section>
</div>