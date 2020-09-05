<template>
    <div
        id="player-voice-icon"
        :style="'opacity: ' + (talking ? '1;' : '0.5;')"
        @mouseover="hovering = true"
        @mouseleave="hovering = false"
    >
        <b-avatar :src="hovering ? player_icon : character_icon" :size="icon_size" />
        <transition
            :duration="130"
            name="custom-classes-transition"
            enter-active-class="animated fadeIn"
            leave-active-class="animated fadeOut"
            mode="out-in"
        >
            <div id="name" :key="name_displayed">{{name_displayed}}</div>
        </transition>
    </div>
</template>

<script>
    export default {
        name: "player-voice-icon",
        data() {
            return {
                icon_size: "36px",
                talking: false,
                hovering: false
            }
        },
        props: {
            character_icon: String,
            character_name: String,
            player_icon: String,
            player_name: String
        },
        computed: {
            name_displayed() {
                return this.hovering ? this.player_name : this.character_name;
            }
        }
    }
</script>

<style scoped>
    #player-voice-icon {
        display: flex;
        flex-direction: row;
    }

    #name {
        font-size: 18px;
        margin-top: auto;
        margin-bottom: auto;
        margin-left: 5px;
        cursor: default;
    }

</style>
