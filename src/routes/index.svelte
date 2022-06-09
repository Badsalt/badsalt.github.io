<svelte:head>
	<title>Research Overview</title>
</svelte:head>

<script>
    import { fade } from "svelte/transition";
    import { currentPage } from "$lib/components/stores"
    $currentPage = "index"
</script>

<div class="container w-11/12 lg:3/4">

    <div class="w-full mb-6 h-auto bg-base border test border-slate-500 rounded-">
        <div class="flex flex-row mx-20 self-center">
            <div class="basis-1/4 self-center"><img class="aspect-[4/3] h-28" src="/pic/icon.PNG" alt="Icon"></div>
            <div class="basis-3/4 h-auto text-left self-center">
                <h1 class="font-bold text-3xl tracking-wider ">DEGERMAN LAB</h1>
                <h3 class="text-2xl tracking-wide italic ">-Epigenetics and telomere biology</h3>
            </div>
        </div>
    </div>    


    <div class="flex flex-col items-start lg:flex-row">
        <div in:fade="{{ duration: 1000, delay: 200 }}" class="basis-1/3">
            <!-- [4/3] -->
            <div class="avatar w-full aspect-[4/3] rounded-lg border-4 border-black">
                <!-- svelte-ignore a11y-img-redundant-alt -->
                <img src="/pic/gruppbild.JPG" alt="Group Picture Lab Members">
              </div>
        </div>
        <div in:fade="{{ duration: 1000, delay: 200 }}" class="basis-2/3">
            <div class="text-left w-11/12  mx-auto my-auto lg:ml-6 lg:w-10/12 text-md lg:text-lg">
                <p class="mb-6">Sofie Degerman’s research team holds expertsise in the fields of epigenetics, telomere biology, and hematopathology, and aims to improve diagnostics, risk stratification, and treatment of hematological malignancies with a special focus on T-cell acute lymphoblastic leukemia (T-ALL). The research is carried out in the Translational Research Centre at Umeå University, which is an excellent translational research environment equipped with modern molecular biology technologies.
                </p>
                <h1 class="font-bold text-lg my-4">Sofie Degerman’s research is currently granted by:</h1>
                <div class="grid grid-cols-3 gap-2 items-center justify-center justify-items-center" >
                    <a href="https://www.barncancerfonden.se/en/" target="_blank"><img src="/pic/founders/Barncancer_fonden.jpg" alt="Barncancer Fonden"></a>
                    <a href="https://www.cancerfonden.se/" target="_blank"><img src="/pic/founders/Cancerfonden.jpg" alt="Cancerfonden"></a>
                    <a href="https://cancerforskningsfonden.se/" target="_blank"><img src="/pic/founders/Cancerforskningsfonden_i_Norrland.jpg" alt="Cancerforskningsfonden_i_Norrland"></a>
                    <a href="https://www.kempe.com/" target="_blank"><img src="/pic/founders/Kempestiftelserna.jpg" alt=""></a>
                    <a href="https://stodforskning.umu.se/" target="_blank"><img src="/pic/founders/Medicinsk_forskning.jpg" alt=""></a>
                    <a href="https://www.regionvasterbotten.se/" target="_blank"><img src="/pic/founders/Region_Västerbotten.jpg" alt=""></a>
                    <!-- Center last element -->
                    <span />
                    <a href="https://www.umu.se/en/" target="_blank"><img src="/pic/founders/Umeå_University.jpg" alt=""></a>
                </div>      
            </div>
        </div>
        
    </div>
</div>

<style>
    .container {
        margin-bottom: 75px;
        margin-top: 90px;
        text-align: center;
    }
    .avatar {
        margin: 0 auto;
    }

    .test {
        border-radius: 100px / 50px;
        box-shadow: 2px 2px 2px 2px grey;
    }

</style>