<script lang="ts">
    import Icon from './Icon.svelte'
    import {base} from "$app/paths"

    const telegram = {
        imgSrc: `${base}/assets/telegram.png`,
        alt: 'Telegram',
        href: "https://t.me/nodir_bobiev",
        id: "tg-link",
        iconSize: 40
    }

    const github = {
        imgSrc: `${base}/assets/github.png`,
        alt: 'Github',
        href: "https://github.com/NodirBobiev",
        id: "gh-link",
        iconSize: 40
    }

    const email = {
        imgSrc: `${base}/assets/email.png`,
        alt: 'Email',
        href: "mailto:n.bobiev@innopolis.university",
        id: "email",
        iconSize: 40
    }
</script>

<div class="nav-links" style="width:140px;">
    <Icon {...telegram}/>
    <Icon {...github}/>
    <Icon {...email}/>
</div>


<style>
    .nav-links{
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
    }
</style>