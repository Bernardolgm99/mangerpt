<template>
    <v-row class="ma-0">
        <v-col v-for="picture in pictures" class="v-col-4 v-col-lg-3 pa-0">
            <v-img v-if="picture.type" aspect-ratio="1" cover :src="picture.src" :alt="picture.alt" @click="viewIn(picture)"></v-img>
            <div v-else class="video-preview">
                <img src="../assets/icons/player.svg" class="btn-close">
                <video :src="picture.src" :alt="picture.alt" @click="viewIn(picture)"></video>
            </div>
        </v-col>
    </v-row>
    <div v-if="viewing_picture" id="view-img" class="d-flex justify-center align-center">
        <div>
            <v-img v-if="viewing_picture.type" :src="viewing_picture.src" :alt="viewing_picture.alt"></v-img>
            <div v-else class="video-wrapper">
                <video controls :src="viewing_picture.src" :alt="viewing_picture.alt"></video>
            </div>
            <button @click="viewOut"><img src="../assets/icons/close.svg" class="btn-close"></button>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        pictures: {
            type: Array,
            required: false,
            default: [
                {
                    src: "./src/assets/icons/bola-de-presunto.jpg",
                    alt: "Bola de Presunto",
                    type: 1,
                },
                {
                    src: "./src/assets/icons/bolo-de-tamara.jpg",
                    alt: "Bolo de Tamara",
                    type: 1,
                },
                {
                    src: "./src/assets/icons/brownie.jpg",
                    alt: "Brownie",
                    type: 1,
                },
                {
                    src: "./src/assets/icons/charlote-pistachio-chocolate.jpg",
                    alt: "Charlote Pistachio Chocolate",
                    type: 1,
                },
                {
                    src: "./src/assets/icons/chef.jpg",
                    alt: "Chef",
                    type: 1,
                },
                {
                    src: "./src/assets/icons/cheesecake.mp4",
                    alt: "Cheesecake",
                    type: 0,
                },
                {
                    src: "./src/assets/icons/chocolate-cremeux.jpg",
                    alt: "Chocolate Cremeux",
                    type: 1,
                },
                {
                    src: "./src/assets/icons/salt-cramel.jpg",
                    alt: "Salt Cramel",
                    type: 1,
                },
                {
                    src: "./src/assets/icons/tiramissu.jpg",
                    alt: "Tiramissu",
                    type: 1,
                },
            ],
        }
    },
    data() {
        return {
            viewing_picture: false,
        }
    },
    methods: {
        viewIn(picture) {
            this.viewing_picture = picture
        },
        viewOut() {
            this.viewing_picture = false;
        }
    },
}

</script>

<style scoped>
#view-img {
    background-color: #000d;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 1;
    width: 100vw;
    height: 100vh;
}

#view-img div {
    height: 80vh;
    width: 80vw;

}

#view-img video {
    width: 100%;
    height: 100%;
}

#view-img button {
    position: fixed;
    top: 50px;
    right: 50px;
    color: #fff;
}

.video-preview {
    position: relative;
    height: 100%;
    width: 100%;
}

.video-preview img {
    pointer-events: none;
    position: absolute;
    z-index: 1;
    top: 35%;
    left: 35%;
    width: 30%;
    height: 30%;
}

.video-preview video {
    position: absolute;
    object-fit: cover;
    width: 100%;
    height: 100%;
}

.btn-close {
    filter: invert(99%) sepia(6%) saturate(642%) hue-rotate(104deg) brightness(121%) contrast(97%);
}
</style>
