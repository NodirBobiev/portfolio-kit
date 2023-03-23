<script lang="ts">
    import Icon from './Icon.svelte'
    import {base} from "$app/paths"
    import {page} from "$app/stores"

    $: pageId = $page.route.id;

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

<header>
    <nav class="nav-bar">
        <div class="nav-links">
            <a class="nav-link" href="{base}/" class:active={pageId==='/'}>About Me</a>
            <a class="nav-link" href="{base}/comic" class:active={pageId==='/comic'}>Comic</a>
        </div>
        <div class="nav-links" style="width:140px;">
            <Icon {...telegram}/>
            <Icon {...github}/>
            <Icon {...email}/>
        </div>
    </nav>
</header>


<style>
    .nav-link{
        display: block;
        padding: 0.5rem 1rem;
        margin: auto 0.5rem;
        text-decoration: none;
        color: rgb(25, 76, 169);
        border-radius: 5px;
        background-color: rgb(255, 255, 255);
        font-weight: bold;
        border: 1px solid rgb(192, 192, 192);
    }
    .active{
        background-color: rgb(25, 76, 169);
        color: white;
        border: 1px solid rgb(25, 76, 169);
    }
    .nav-links{
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
    }
    .nav-bar{
        display: flex;
        flex-direction: row;
        height: 70px;
        align-items: center;
        justify-content: space-between;

    }
</style>
