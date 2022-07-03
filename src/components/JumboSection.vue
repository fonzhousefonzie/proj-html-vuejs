<template>
    <div class="section">
        <JumboBanner class="scale-y" :img-right="image" :start-text="true"
            :starth1="'Complete Your Dreams in JavaS Programming'"
            :start-p="`Learn any coding program in distance and for a reasonable fee. You don't have to struggle alone, you've got our assistance and help.`"
            :start-button="'Download free E-book'" :start-btn-icon="'fa fa-solid fa-download'" />
    </div>
</template>

<script>
import JumboBanner from './JumboBanner.vue'
import { state } from '@/state';

export default {
    components: { JumboBanner },
    computed: {
        image() {
            const image = state.image1;

            return image
        }
    }

}
</script>

<style lang="scss" scoped>
.section {
    padding: 3rem 0;
    transform: scaleY(-1);
    background: url("../assets/img/jumbo-overlay.svg"), var(--main-bg);
    background-position: top, center;
    background-repeat: no-repeat;
    background-size: 100% 60%, cover;

    .scale-y {
        transform: scaleY(-1);

    }
}
</style>