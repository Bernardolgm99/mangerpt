<template>
    <div class="d-flex">
        <v-container class="test d-flex flex-column align-center py-16">
            <h3 class="mb-2">CONTACT US</h3>
            <div class="d-flex flex-wrap">
                <span>TEL:+351 900 000 000 /</span><span class="mb-10">EMAIL: contact@mange.pt</span>
            </div>
            <div class="w-100 d-flex flex-column align-start mb-8">
                <span class="mb-2">Name*</span>
                <input type="text" name="name" placeholder="" />
            </div>
            <div class="w-100 d-flex flex-column align-start mb-8">
                <span class="mb-2">Email*</span>
                <input type="text" name="name" placeholder="" />
            </div>
            <div class="w-100 d-flex flex-column align-start mb-8">
                <span class="mb-2">Message*</span>
                <textarea></textarea>
            </div>
            <div class="w-100 d-flex justify-space-around">
                <button class="py-2 px-8">Reset</button>
                <button class="py-2 px-8">Submit</button>
            </div>
        </v-container>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>

.test{
    max-width: 600px;
}

div {
    font-size: 20px;
}

span {
    color: #333;
}

h3 {
    font-size: 40px;
    letter-spacing: 16px;
}

input, textarea {
    padding: 5px;
    border: 1px solid #333;
    width: 100%;
}

textarea {
    height: 180px;
}

button:hover {
    background-color: #e3e3e3;
}
</style>