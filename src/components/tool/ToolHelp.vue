<template>
    <m-dialog @close="doClose">
        <template #header>
            {{ i18n('help') }}
        </template>
            
        <div />
    </m-dialog>
</template>

<script setup lang="ts">

import { render } from 'vue';

import MDialog from '~/components/MDialog.vue';
import { i18n } from '~/utils';

const props = defineProps<{
    confirm: (lang: string, code: string) => void,
    container: HTMLDivElement
}>();

function doClose(){
    render(null, props.container);
}

</script>