<template>
    <div id="preview-character-icon">
        <div id="player-icon">
            <b-avatar
                v-if="!(typeof player_icon === 'undefined')"
                :src="player_icon"
                :size="player_icon_size"
            />
            <b-icon
                id="player-placeholder"
                v-if="typeof player_icon === 'undefined'"
                @mouseover="hovering_player = true"
                @mouseleave="hovering_player = false"
                :icon="hovering_player ? 'plus-circle-fill' : 'plus-circle' "
                :font-size="player_icon_size"
            />
            <div id="player-name">asd</div>
        </div>
        <div>
            <b-avatar :src="char_icon" :size="char_icon_size" />
            <div id="char-name">{{char_name}}</div>
            <div id="char-desc">{{char_desc}}</div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "preview-character-icon",
        data() {
            return {
                player_icon_size: "47px",
                char_icon_size: "72px",
                hovering_player: false
            }
        },
        props: {
            player_icon: String,
            player_name: String,
            char_icon: String,
            char_name: String,
            char_desc: String
        },
        computed: {

        }
    }
</script>

<style scoped>
    #preview-character-icon {
        display: flex;
        flex-direction: row;
        text-align: center;
    }

    #player-icon {
        margin-top: 20px;
        padding-right: 22px;
    }

    #player-placeholder {
        cursor: pointer;
    }

    #player-name {
        margin-left: auto;
        margin-right: auto;
        width: 96px;
    }

    #char-name {
        width: 72px;
        margin-top: 5px;
        margin-left: auto;
        margin-right: auto;
        font-size: 24px;
    }

    #char-desc {
        width: 112px;
        margin-left: auto;
        margin-right: auto;
        margin-top: -5px;
        font-size: 12px;
    }

</style>
