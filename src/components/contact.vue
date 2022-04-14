<template>
    <div id="contact" class="flex justify-center items-center h-full pt-60 pb-28">
        <div class="flex justify-center items-center flex-wrap 
        smm:w-3/4 md:w-7/12 lg:w-6/12 w-4/5 rounded-30px contact pt-6 pb-20">
           <div class="block">
            <h2 class="text-center text-3xl font-serif mb-3
            text-green-400" >Contact Me</h2>
            <form action="" class="block">
                <div class="">
                <input type="text" name="name" placeholder="Full Name" class=" 
                rounded-40px">
                </div>
                <div>
                <input type="email" name="email" placeholder="Email" class="
                rounded-40px"></div>
                <div class="">
                <textarea name="message" id="" cols="25" rows="7"
                placeholder="How May I Be Of Service" class=""></textarea>
                </div>
            </form>
            <button class=" sm:ml-24 ml-12
         bg-green-400 p-4 rounded-30px w-32 text-gray-600">SEND
         </button>
        </div>
        </div>
    </div>
</template>
<script>
export default {
    
}
</script>
<style>
input, textarea{
    margin-bottom: 30px;
}
input{
    padding: 10.5px;
    width: 14rem;
}
input:focus{
    outline: none;
}
textarea{
    border-radius: 10px;
    outline: none;
    
}
button:focus{
    outline: none;
}
.contact{
    background: rgba(255, 255, 255, 0.15);
  padding-bottom: 2rem;
  border-radius: 20px;
}
@media screen and (min-width:990px) {
    .contact{
    background: rgba(255, 255, 255, 0.15);
  padding-bottom: 33rem;
  border-radius: 20px;
}
}
@media screen and (min-width:500px) {

input, textarea{
    margin-bottom: 30px;
}
input{
    padding: 10.5px;
    width: 20rem;
}
input:focus{
    outline: none;
}
textarea{
    border-radius: 10px;
    outline: none;
    width: 20rem;
}
.contact{
    background: rgba(255, 255, 255, 0.15);
  padding-bottom: 2rem;
  border-radius: 20px;
}
}
</style>