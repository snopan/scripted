<template>
    <div id="game-screen">
        <div id="hot-bar">
            <div
                class="bar-item"
                v-for="item in bar_items"
                @click="selected_section = item"
                :style="selected_section == item ?
                'background-color: black; position: relative; height 51px; top: -1px; border-bottom: none' : ''"
            >{{item}}</div>
        </div>
        <div id="game-section">
            <text-section id="text-section" title="Wowww" text="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Sit amet nisl purus in mollis. Fringilla ut morbi tincidunt augue interdum velit euismod. Tempus quam pellentesque nec nam aliquam sem et. Imperdiet dui accumsan sit amet nulla facilisi morbi tempus. Eu consequat ac felis donec et. Elementum integer enim neque volutpat ac. Adipiscing enim eu turpis egestas pretium. Elementum sagittis vitae et leo duis ut diam quam nulla. Sem nulla pharetra diam sit amet. Dolor sit amet consectetur adipiscing elit pellentesque. Sagittis vitae et leo duis ut diam quam nulla porttitor. Egestas erat imperdiet sed euismod nisi porta lorem mollis. Turpis massa sed elementum tempus egestas. At ultrices mi tempus imperdiet nulla.Risus in hendrerit gravida rutrum quisque non tellus orci ac. Commodo elit at imperdiet dui accumsan sit amet nulla. Cras adipiscing enim eu turpis egestas. Scelerisque in dictum non consectetur a. Etiam tempor orci eu lobortis elementum. Commodo ullamcorper a lacus vestibulum sed arcu non odio euismod. Vitae congue eu consequat ac felis donec et. Malesuada fames ac turpis egestas maecenas pharetra. Aliquam nulla facilisi cras fermentum odio eu feugiat pretium nibh. Nec ultrices dui sapien eget mi. Odio ut sem nulla pharetra. Iaculis nunc sed augue lacus viverra vitae. Nunc eget lorem dolor sed. Fringilla est ullamcorper eget nulla facilisi etiam dignissim. Risus quis varius quam quisque id diam vel quam elementum.Arcu felis bibendum ut tristique. Enim neque volutpat ac tincidunt vitae semper quis lectus nulla. Velit scelerisque in dictum non consectetur a. Amet justo donec enim diam vulputate ut pharetra sit. Feugiat vivamus at augue eget arcu dictum varius duis. Sit amet facilisis magna etiam tempor. Ac turpis egestas integer eget aliquet nibh. Sed risus ultricies tristique nulla aliquet enim tortor. Vitae nunc sed velit dignissim sodales ut eu. Augue eget arcu dictum varius duis at consectetur lorem donec. Neque aliquam vestibulum morbi blandit cursus. Tempus egestas sed sed risus pretium quam vulputate dignissim suspendisse. Venenatis cras sed felis eget velit. Nullam vehicula ipsum a arcu cursus vitae congue mauris. Gravida cum sociis natoque penatibus et magnis dis. Orci sagittis eu volutpat odio facilisis mauris sit.Nunc mattis enim ut tellus. Quisque sagittis purus sit amet volutpat. Id neque aliquam vestibulum morbi blandit cursus. Sed augue lacus viverra vitae congue eu. Ultricies mi eget mauris pharetra et. Mauris nunc congue nisi vitae. Sed turpis tincidunt id aliquet risus feugiat in ante. Sed risus pretium quam vulputate dignissim. Id diam vel quam elementum pulvinar etiam non quam lacus. Sagittis purus sit amet volutpat. Proin sed libero enim sed faucibus.Bibendum neque egestas congue quisque egestas diam in arcu. Scelerisque eleifend donec pretium vulputate sapien nec sagittis. In massa tempor nec feugiat. Vitae auctor eu augue ut lectus. Nibh tortor id aliquet lectus proin. Eget aliquet nibh praesent tristique. At augue eget arcu dictum. Pulvinar pellentesque habitant morbi tristique. Rhoncus urna neque viverra justo nec ultrices dui sapien. Mattis molestie a iaculis at. Pellentesque habitant morbi tristique senectus et netus et. Id ornare arcu odio ut sem nulla pharetra diam. Imperdiet sed euismod nisi porta lorem mollis aliquam ut porttitor. At in tellus integer feugiat scelerisque. Diam sollicitudin tempor id eu nisl nunc mi ipsum faucibus. Pretium nibh ipsum consequat nisl vel pretium. Leo vel fringilla est ullamcorper eget nulla facilisi etiam dignissim. Nunc sed augue lacus viverra vitae congue. Integer eget aliquet nibh praesent. Pulvinar elementum integer enim neque volutpat ac tincidunt vitae.\n\nrna neque viverra justo nec ultrices dui sapien eget mi. Sagittis eu volutpat odio facilisis mauris sit amet massa. Nunc pulvinar sapien et ligula ullamcorper. Massa eget egestas purus viverra accumsan in nisl nisi. Arcu dui vivamus arcu felis bibendum ut tristique et egestas. Vel risus commodo viverra maecenas. Enim tortor at auctor urna nunc id cursus metus. Donec et odio pellentesque diam volutpat commodo sed egestas egestas. Ut diam quam nulla porttitor massa. Nunc id cursus metus aliquam eleifend mi in nulla posuere. Fermentum leo vel orci porta non. Ut sem nulla pharetra diam sit. Lectus mauris ultrices eros in cursus. Habitant morbi tristique senectus et netus et. Eu mi bibendum neque egestas congue quisque egestas. Arcu non sodales neque sodales ut etiam sit amet. Libero enim sed faucibus turpis in. Amet consectetur adipiscing elit duis tristique Mattis ullamcorper velit sed ullamcorper morbi tincidunt ornare massa eget. Urna cursus eget nunc scelerisque viverra mauris in. Et tortor at risus viverra. Feugiat in ante metus dictum at tempor. Rhoncus est pellentesque elit ullamcorper. Cras ornare arcu dui vivamus arcu felis bibendum ut tristique. Sit amet aliquam id diam maecenas ultricies mi. Magna ac placerat vestibulum lectus mauris ultrices eros in cursus. Sagittis aliquam malesuada bibendum arcu vitae elementum curabitur vitae nunc. Tincidunt eget nullam non nisi est sit amet facilisis. Ac auctor augue mauris augue neque gravida in."/>
            <div id="voice-wrapper">
                <player-voice-icon player_name="testt" character_name="idk"/>
            </div>
            <div id="icon-wrapper">
                <misc-icons />
            </div>
        </div>
    </div>
</template>

<script>
    import PlayerVoiceIcon from "./PlayerVoiceIcon";
    import MiscIcons from "./MiscIcons";
    import TextSection from "./TextSection";
    export default {
        name: "game-screen",
        components: {
            PlayerVoiceIcon,
            MiscIcons,
            TextSection
        },
        data() {
            return  {
                selected_section: false,
                bar_items: ["Summary", "Character Introduction","teettst", "trstas", "trstas"]
            }
        },
        methods: {
        }
    }
</script>

<style scoped>
    #game-screen {
        width: 100%;
        height: 100%;
        position: relative;
        display: flex;
        flex-direction: row;
    }

    #hot-bar {
        width: 181px;
        height: 100%;
        overflow-y: auto;
        background-color: rgba(255, 255, 255, 0.1);
    }

    .bar-item {
        min-width: 181px;
        min-height: 50px;
        text-align: center;
        padding-top: 10px;
        border-bottom: 1px solid rgba(255, 255, 255, 0.5);
        cursor: pointer;
    }

    .bar-item:hover {
        background-color: rgba(255, 255, 255, 0.2);
    }

    #game-section {
        width: calc(100% - 181px);
        height: 100%;
    }

    #voice-wrapper {
        position: absolute;
        left: calc(181px + 40px);
        top: 40px;
    }

    #icon-wrapper {
        position: absolute;
        right: 40px;
        top: 40px;
    }

    #text-section {
        width: calc(100% - (2*50px) - 200px);
        height: calc(100% - (2*50px));
        margin-left: auto;
        margin-right: auto;
        margin-top: 50px;
    }

    @media screen and (max-width: 700px) {
        #game-screen {
            flex-direction: column-reverse;
        }

        #hot-bar {
            width: 100%;
            height: 50px;
            display: flex;
            flex-direction: row;
            overflow-x: auto;
            overflow-y: hidden;
        }

        #game-section {
            width: 100%;
            height: calc(100% - 50px);
        }

        #voice-wrapper {
            left: 20px;
            top: 20px;
        }

        #icon-wrapper {
            right: 20px;
            top: 20px;
        }

        #text-section {
            width: calc(100% - (2*20px) - 10px);
            height: calc(100% - (2*30px));
            margin-left: auto;
            margin-right: auto;
            margin-top: 30px;
        }
    }
</style>
