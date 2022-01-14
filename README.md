# svelte-simple-qrcode

Superbly simple svelte-wrapper for the great [qrcode-library](https://www.npmjs.com/package/qrcode)


## Install this thingy-bob
```bash
npm install --save svelte-simple-qrcode
```

## Usage
```html
<script>
    import QrCode from 'svelte-simple-qrcode';
    let qrcode = '';
</script>
<div>
    <input type="text" placeholder="qrcode"  bind:value={qrcode} />
    <QrCode width='150px' code="{qrcode}" />
</div>

```

