<template>
    <div>
        <table :class="clases">
            <thead :class="clases">
                <tr>
                    <th v-for="(item, i) in titulos" :key="i" scope="col">{{ item }}</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(item, i) in registros" :key="i">
                    <th :class="clases">{{ i + 1 }}</th>
                    <td v-for="(reg, r) in item" :key="r">{{ reg }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
export default ({
    props: {
        titulos: {
            type: Array,
            required: true,
        },
        registros: {
            type: Array,
            required: true,
        },
        clases: {
            type: String,
        }
    }
})
</script>
