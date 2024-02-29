<script>
import AppNav from './components/AppNav.vue';
import AppContent from './components/AppContent.vue';
import AppIcon from './components/AppIcon.vue';
import AppFooter from './components/AppFooter.vue';


export default {
    components: {
        AppNav,
        AppContent,
        AppIcon,
        AppFooter,
    }
}
</script>

<template>
    <AppNav></AppNav>
    <AppContent></AppContent>
    <AppIcon></AppIcon>
    <AppFooter></AppFooter>
</template>

<style></style>