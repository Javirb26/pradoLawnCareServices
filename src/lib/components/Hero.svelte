<script>
    let { 
        src, 
        alt
    } = $props();
</script>

<header>
    <div class="relative h-180 w-full bg-cover bg-center" style={`background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0)), url('${src}');`}>
        <div class="flex flex-col justify-center items-center pb-10 px-4 lg:pb-0 lg:px-10 lg:flex-row lg:justify-between h-full mx-auto max-w-325 transition-all duration-300 transform ease-in-out">
            <div class="lg:flex lg:flex-col lg:justify-center text-center lg:text-left text-white pb-16 lg:pb-40">
                <h1 class=" text-white text-4xl lg:text-5xl">Your Lawncare Provider</h1>
                <h3 class="pl-2 text-lg lg:text-xl">We get the job done and surpass your expecations</h3>
                <p class="pl-2 text-amber-300">Fill out our contact form to get a free quote today!</p>
            </div>
            <div class="lg:flex lg:flex-col lg:justify-center">
                <form 
                    name="contact" 
                    method="post" 
                    data-netlify="true"
                    data-netlify-honeypot="bot-field"
                    class="flex flex-col w-100">

                    <input type="hidden" name="form-name" value="contact"/>
                    <input type="hidden" name="bot-field" />

                    <label class="text-white" for="name" >add name</label>
                    <input type="text" name="name">
                    <label class="text-white" for="email">email</label>
                    <input type="email" name="email">
                    <label class="text-white" for="phone">phone number</label>
                    <input type="tel" name="phone">


                    <button class="bg-green-600 rounded-md max-w-1/2 px-4 py-2 mt-5 hover:brightness-90 cursor-pointer hover:text-white" type="submit">Get your Free Quote</button>
                </form>
            </div>
        </div>
        
        <div class="custom-shape-divider-bottom">
            <svg class="block relative" data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                <path d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z" opacity=".25" class="shape-fill" fill="white"></path>
                <path d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z" opacity=".5" class="shape-fill" fill="white"></path>
                <path d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z" class="shape-fill" fill="white"></path>
            </svg>
        </div>
    </div>
    
</header>


<style>
    .custom-shape-divider-bottom {
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        overflow: hidden;
        line-height: 0;
        transform: rotate(180deg);
    }
</style>
