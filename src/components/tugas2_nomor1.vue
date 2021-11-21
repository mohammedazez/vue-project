 <template>
    <div id="app">
        <h2>Hitung Luas Segitiga</h2>

        <h3>Alas: {{Alas}}</h3>
        <h3>Tinggi: {{Tinggi}}</h3>
        <h3>Setengah: {{Setengah}}</h3>
        <br/><br/>
        <h1>
            {{Alas}} x {{Tinggi}} / {{Setengah}} =
            {{(Alas*Tinggi) / Setengah}}
        </h1>
    </div>
</template>

<script>

export default {
    name: "tugas2_nomor1",
    props: {
        Alas: Number,
        Tinggi: Number,
        Setengah: Number,
    }
}

</script>