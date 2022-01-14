<script>
    import {toString} from 'qrcode/lib/browser.js';

    export let code;
    export let options = {};
    export let width = '100%';

    let svg = '';
    async function updateQrCode(newQrCode) {
        try {
            svg = !newQrCode ? '' : await toString(newQrCode, options);
        } catch (e) {
            svg = '';
        }
    }

    $: updateQrCode(code);

</script>
<div style="--icon-width: {width};" class="container">{@html svg}</div>
<style>
    .container {
        width: var(--icon-width);
        height: auto;
        display: block;
        overflow: hidden;
        max-width: 100%;
        max-height: 100%;
    }
</style>