<template>
    <div>
        <div>자식 컴포넌트</div>
        <ul>
            <li v-for="item of listData" :key="item.value" @click="onChange">
                {{item.text}}
            </li>
        </ul>
    </div>
</template>

<script lang="ts">
import {Vue, Component, Prop, Model} from 'vue-property-decorator';

interface List {
    value: string;
    text: string;
}

@Component
export default class ChildComponent extends Vue {
    //@Prop() value!: List[];

    @Model('click') readonly listData!: List[];
    
    private onChange(){
        alert(1);
    }

}
</script>

<style>

</style>