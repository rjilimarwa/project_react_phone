<template>
    <div class="folder-navbar">
        <div class="container">
            <ul class="nav navbar-nav">
                <li :class="{active: checkRoute('informations')}">
                    <a :href="'folders/' + folder + '/myproject/project/informations'">Informations</a>
                </li>
                <li :class="{active: checkRoute('leader')}">
                    <a :href="'folders/' + folder + '/myproject/project/leader'">Responsable</a>
                </li>
                <li :class="{active: checkRoute('period')}">
                    <a :href="'folders/' + folder + '/myproject/project/period'">Période</a>
                </li>
                <li :class="{active: checkRoute('contact')}">
                    <a :href="'folders/' + folder + '/myproject/project/contact'">Coordonnées</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
        name: "ProjectHeader",
        props: ['folder'],
        data() {
            return {
                urlRoute: window.location.pathname.split('/').slice(1)
            }
        },
        mounted() {
            this.urlRoute.splice(1, 1);
            this.urlRoute = this.urlRoute.join('.');
        },
        methods: {
            checkRoute(value) {
                let url = this.urlRoute.toString();
                return url.substr(value.length * -1) === value;
            }
        }
    }
</script>

<style scoped>

</style>