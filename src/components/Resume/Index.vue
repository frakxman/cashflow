<!-- *********** HTML *********** -->
<template>
    <main>
        <p>{{ label }}</p>
        <h1>{{ amountVisual }}</h1>
    </main>
</template>

<!-- *********** JavaScript *********** -->
<script>
    export default {
        props: {
            totalLabel: {
                type: String,
            },
            label: {
                type: String,
                default: null,
            },
            totalAmount: {
                type: Number,
            },
            amount: {
                type: Number,
                required: true,
                default: null
            }
        },
        computed: {
            labelVisual() {
                return this.label !== null ? this.label : this.totalLabel;
            },
            amountVisual() {
                return this.amount !== null ? this.amount : this.totalAmount;
            },
            amountCurrency() {
                return currencyFormatter.format(this.amountVisual);
            },
        }
    }
</script>

<!-- *********** CSS *********** -->
<style scoped>
    main {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        width: 100%;
    }

    h1,
    p {
        margin: 0;
        text-align: center;
    }

    h1 {
        margin-top: 14px;
        color: var(--brand-green);
    }

    .graphic {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        padding: 48px 24px;
        box-sizing: border-box;
    }
</style>