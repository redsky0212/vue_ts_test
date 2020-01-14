<template>
    <div>
        <div>component v-model 사용법</div>
        <child-component v-model="listData"></child-component>
    </div>
</template>

<script lang="ts">
import {Vue, Component} from 'vue-property-decorator';
import ChildComponent from './ChildComponent.vue';

interface List {
    value: string;
    text: string;
}

@Component({
    components: {
        ChildComponent,
    }
})
export default class ComponentVmodel extends Vue {
    private readonly listData: List[] = [
        {text:'첫번째', value:'1'},
        {text:'두번째', value:'2'},
        {text:'세번째', value:'3'},
    ]; 
}
</script>

<style>

</style>