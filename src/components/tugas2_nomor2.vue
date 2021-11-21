 <template>
    <div id="app">
        
        <!-- Alas -->
        <input type="text" placeholder="Masukan Alas" v-model="alas" />
        <button @click="handleInput">Alas</button>
        <br/>

        <!-- Tinggi -->
        <input type="text" placeholder="Masukan tinggi" v-model="tinggi" />
        <button @click="handleInput">Alas</button>


        <h2>Menghitung Luas Segitiga</h2>

        <h3>Alas: {{alas}}</h3>
        <h3>Tinggi: {{tinggi}}</h3>
        <h3>Luas Segitiga: {{(alas*tinggi) / 2}}</h3>


    </div>
</template>

<script>

export default {
    name: "tugas2_nomor2",
    data() {
        return {
        alas: "",
        tinggi: "",
        };
    },
    methods: {
        handleInput() {
        console.log(this.alas);
        console.log(this.tinggi);
        },
    },
}

</script>