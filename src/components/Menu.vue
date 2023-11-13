
<template>
    <nav class="menu">
        <ul class="menu__list">
            <li class="menu__item" v-for="(item, index) in menuItems" :key="index" >
                <a class="menu__link" href="#">
                    <span class="menu__active"> {{ item.text }}</span>
                    <span class="menu__hover"> {{ item.text }}</span>
                </a>
            </li>
        </ul>
    </nav>
</template>
/template>

<script>
export default {
  data() {
    return {
        menuItems: [
            { text: 'о конференции' },
            { text: 'спикеры'},
            { text: 'программа'},
            { text: 'фотогалерея'},
            { text: 'организаторы'}
        ]}
    }
}
</script>
