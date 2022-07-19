<template>

    <section class="section-4-container">
        <div class="container">
            <!-- title -->
            <h2 class="title-container">
               <span class="light-weight">Whant to work with us? Send us a </span> 
               <span class="italic"> a message! </span>
            </h2>
            <!-- text -->
            <p class="text"> 
               Lorem, ipsum dolor sit amet consectetur adipisicing elit. Explicabo modi sunt, veritatis magnam quas dolores nobis, magni nesciunt tempora ratione odit adipisci accusamus neque doloribus est aperiam ipsam velit eius.
            </p>
            <!-- button -->
            <button>CONTACT</button>
        </div>
    </section>
    
</template>

<script>
export default {
    name:'SectionFor'
}
</script>

<style lang="scss" scoped>
@import '../style/common';
@import '../style/variables';

.section-4-container{
    background-image: url('data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBw8SEBUQDw8PDxUVFRUVDw8PDw8PDw8PFRcXFhUVFRUYHSggGBolGxUVITEhJSkrLi4uFx8zODMtNygtLisBCgoKDQ0NDw0NDysZFRkrLSsrNy0rKys3LSstKy0tLSsrLTcrLSs3Ny0rLSsrLTcrKysrKysrLSsrKysrKysrK//AABEIAMEBBQMBIgACEQEDEQH/xAAYAAEBAQEBAAAAAAAAAAAAAAAAAQIDB//EABwQAQEBAQACAwAAAAAAAAAAAAABEQIh8AMxof/EABcBAQEBAQAAAAAAAAAAAAAAAAABBAP/xAAUEQEAAAAAAAAAAAAAAAAAAAAA/9oADAMBAAIRAxEAPwD13AgzOq4igiLEORVRaAgGAshYqWgzFxIugFgloEjTMagiUACRYlWKIFXUEFTVBFiUAxQVOomLRBiwW0BsRQFqQBFjKwBUAUhFoqVKVBFAwAKoIsrNTVGxI0gysQBehFoFZWoCkRYopREEooDNVOgG6hQFgIAQi4ABgKlqsgVIpijUiKlQQgsBKzWmao0sZjUAAQRSQqiVFwwBUXlARpkAqpQZ6CwBqxQRQoAC1FRYEKCUsIoIkWgKACYCiJWcapiqzjSCA1GWoAlVAEqgEixIAIqAYqAJRKA2FSIrSQtKC1IALE6pE3yqLGqzF0EIigogCwSmgUABCAKJCCtIaACaAoCAhaioaGFBKJQG6RKqKlVJ9miLoiwVUhqRUUoCgi6ICGgoigFTQFE00FQgCppqAsBAaEEUIkKqLqakiyAzodANVQRUXBYqJQVBAXFCI1WaigQVCgoIQAAoCEVAVGkBBYAGFAKgAC4UEVNJQce75F7oDtFADCAAC0EsBYCVFoBIYpAEWpAAAMAARQBKoCKEAqVqs0EVYASJWkBlGqyDj8nCt0FdaQIIqUS+/oLFZigKgC1KVFFWJFQKhUoCooBUAVAiigIIsKAVFqAsKFAqCWgtLyc1egYCgNVQigigJILABUqwEBAU0KgIqAQIKAQAWIsAFRAABEVFGgkEEphQCLUkUGKFAbSqKACBCCqiKCKlSLSRQFAQMEEKtgogogEXABKqSAikUGRRQKCCEiqAy1UwHPoXqKDUGZV0F0rOqCkZ1dUa0Z00GkQ0F1ZWLV0Fis6uoGqxasoKM2rKDWlZNBRJU1RtNTTUFE01RRNTQa01k1BoZ1dBnoKKEAESgCgoCQgCLEAUICgoIIQAF5AEWACQgAUgAqABSAAABFgAzQBH/9k=');
    padding: $padding_section;

    & .container{
        width: 70%;
        margin: 0 auto;
        text-align: center;

        & .title-container{
            font-size: 45px;
            padding: $padding_section;
        }

         & .text{
            margin-bottom: 30px;
        }

        & button{
            padding: 15px 40px;
            background-color: $color_green;
            border: none;
            font-size: 10px;
            font-weight: 600;
            margin-bottom: 40px;
            cursor: pointer;

            &:hover{
                color: white;
                border: 2px solid black;
            }
        }
    }
}

</style>