<template>
    <div id="misc-icons">
        <b-icon
            class="icons"
            @mouseover="hovering_help = true"
            @mouseleave="hovering_help = false"
            v-b-tooltip.hover.left="{ variant: 'light' }"
            title= "This is how u play the game scrub"
            :icon="hovering_help ? 'question-circle-fill' : 'question-circle'"
            :font-size="icon_size"
        />
        <b-icon
            class="icons"
            @mouseover="hovering_mute = true"
            @mouseleave="hovering_mute = false"
            @click="muted = !muted"
            :icon="mute_icon"
            :font-size="icon_size"
        />
    </div>
</template>

<script>
    export default {
        name: "misc-icons",
        data() {
            return {
                hovering_help: false,
                hovering_mute: false,
                muted: false,
                icon_size: "20px"
            }
        },
        computed: {
            mute_icon() {
                if (this.muted) {
                    return this.hovering_mute ? "mic-mute-fill" : "mic-mute"
                }
                else {
                    return this.hovering_mute ? "mic-fill" : "mic"
                }
            }
        }
    }
</script>

<style scoped>
    #misc-icons {
        display: flex;
        flex-direction: column;
    }

    .icons {
        margin-top: 5px;
        margin-bottom: 5px;
    }
</style>
