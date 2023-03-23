<script lang="ts">
    import Icon from './Icon.svelte'


    const telegram = {
        imgSrc: '/assets/telegram.png',
        alt: 'Telegram',
        href: "https://t.me/nodir_bobiev",
        id: "tg-link",
        iconSize: 40
    }

    const github = {
        imgSrc: '/assets/github.png',
        alt: 'Github',
        href: "https://github.com/NodirBobiev",
        id: "gh-link",
        iconSize: 40
    }

    const email = {
        imgSrc: '/assets/email.png',
        alt: 'Email',
        href: "mailto:n.bobiev@innopolis.university",
        id: "email",
        iconSize: 40
    }
</script>

<div style="display:inline">
    <div class="nav-links" style="width:140px;">
        <Icon {...telegram}/>
        <Icon {...github}/>
        <Icon {...email}/>
    </div>
</div>

<style>
    .nav-links{
        margin-top: 50px;
        margin-left: auto;
        margin-right: auto;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
    }
</style>