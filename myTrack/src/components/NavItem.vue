<script>
export default{
    inheritAttrs: false
}
</script>
<template>
    <li class="flex-1">
    <a v-bind="$attrs" class="flex flex-col items-center p-2 text-xs capitalize"> <!-- $attrs наследуется от TheNav.vue через <NavItem :href="`#${page}`-->
        <slot></slot>
    </a>
    </li>
</template>