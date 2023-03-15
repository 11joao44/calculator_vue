<script>
export default {
    data() {
        return {
            numero1: '',
            numero2: '',
            operacao: '',
        };
    },
    computed: {
        resultado() {
            if (this.operacao === 'soma') {
                return Number(this.numero1) + Number(this.numero2);
            } else if (this.operacao === 'subtracao') {
                return Number(this.numero1) - Number(this.numero2);
            } else if (this.operacao === 'multiplicacao') {
                return Number(this.numero1) * Number(this.numero2);
            } else if (this.operacao === 'divisao') {
                return Number(this.numero1) / Number(this.numero2);
            }
        },
    },
};
</script>


<template>
    <div>
        <div class="d-flex justify-content-evenly">
            <input type="number" v-model="numero1" />
            <select v-model="operacao">
                <option value="soma">+</option>
                <option value="subtracao">-</option>
                <option value="multiplicacao">x</option>
                <option value="divisao">÷</option>
            </select>
            <input type="number" v-model="numero2" />
        </div>
        <div class="text-center mt-5">Resultado: {{ resultado }}</div>
    </div>
</template>