<template>
    <nav class="navbar navbar-expand-md navbar-light bg-white shadow-sm fixed-top px-5">
        <div class="container-fluid">
            <router-link :to="{ name: 'home' }" class="navbar-brand font-weight-bold"
                >TW Record Management</router-link
            >
            <button
                class="navbar-toggler"
                data-bs-toggle="collapse"
                data-bs-target="#navbarCollapse"
            >
                <span class="navbar-toggler-icon"></span>
            </button>
            <div id="navbarCollapse" class="collapse navbar-collapse">
                <ul class="navbar-nav">
                <li class="nav-item">
                    <router-link
                    class="nav-link"
                    data-bs-toggle="collapse"
                    data-bs-target=".navbar-collapse.show"
                    :to="{ name: 'home' }"
                    >
                    Home
                    </router-link>
                </li>

                <li class="nav-item">
                    <router-link
                    class="nav-link"
                    data-bs-toggle="collapse"
                    data-bs-target=".navbar-collapse.show"
                    :to="{ name: 'about' }"
                    >
                    About
                    </router-link>
                </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
    $(window).scroll(function(){
        if($(window).scrollTop() <= 40) {
            $('.navbar').removeClass('scroll_nav');
        }
        else {
            $('.navbar').addClass('scroll_nav');
        }
    })
</script>