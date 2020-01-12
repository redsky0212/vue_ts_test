<template>
    <div>
        <h1>Slot 테스트</h1>
        <div>
            <slot-child>
            <template #[te]="data">
                <h1>h1 슬롯 헤더 연습!</h1>
                <p>{{data.val}}</p>
            </template>
            </slot-child>
        </div>
    </div>
</template>

<script lang="ts">
import {Vue, Component} from 'vue-property-decorator';
import SlotChild from './SlotChild.vue';

@Component({
    components: {
        SlotChild,
    },
})
export default class SlotTest extends Vue {
    private te: string = 'header';
}
</script>

<style>

</style>