<script>
    import {hasVat} from './store'
    export let title, description, price=0
    let hasVatValue;
    hasVat.subscribe(value => {
        hasVatValue = value;
    })
</script>

<div class="card">
    <h2>{title}</h2>
    <p>{description}</p>
    <span>$ {hasVatValue ? price*1.2 : price}</span>
</div>

<style>
    .card {
        border: 1px solid tomato;
        width: 500px;
    }
    h2 {
        font-size: 30px;
        font-weight: var(--font-weight-8);
    }
    p {
        font-weight: var(--font-weight-4);
    }
</style>