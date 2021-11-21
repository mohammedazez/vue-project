<template>
  <div >
    <!-- Angka -->
     <b-button @click="append('5')" variant="outline-primary">5</b-button>
     <b-button @click="append('6')" variant="outline-primary">6</b-button>   
     <br/><br/>

    <!-- Operator -->
    <b-button @click="ditambah" variant="secondary">Tambah</b-button>
    <b-button @click="dikali" variant="success">Kali</b-button>
    <b-button @click="dikurangi" variant="danger">Kurangi</b-button>
    <b-button @click="dibagi" variant="warning">Bagi</b-button>
    <br/><br/>
 
    <b-button @click="cekHasil" pill>Hasil</b-button>
    <b-button @click="hapus" pill>Hapus</b-button>
    <h1>{{terbaru || '0'}}</h1>
    
  </div>
</template>

<script>
export default {
  data() {
    return {
      sebelumnya: null,
      terbaru: '',
      operator: null,
      operatorDiklik: false,
    }
  },
  methods: {
    hapus() {
      this.terbaru = '';
    },
    append(number) {
      if (this.operatorDiklik) {
        this.terbaru = '';
        this.operatorDiklik = false;
      }
      this.terbaru = `${this.terbaru}${number}`;
    },
    setSebelumnya() {
      this.sebelumnya = this.terbaru;
      this.operatorDiklik = true;
    },
    dibagi() {
      this.operator = (a, b) => a / b;
      this.setSebelumnya();
    },
    dikali() {
      this.operator = (a, b) => a * b;
      this.setSebelumnya();
    },
    dikurangi() {
      this.operator = (a, b) => a - b;
      this.setSebelumnya();
    },
    ditambah() {
      this.operator = (a, b) => a + b;
      this.setSebelumnya();
    },
    cekHasil() {
      this.terbaru = `${this.operator(
        parseFloat(this.terbaru), 
        parseFloat(this.sebelumnya)
      )}`;
      this.sebelumnya = null;
    }
  }
}

</script>


