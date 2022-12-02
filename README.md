<h1>5 Kawan Terbaik</h1>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.1/jquery.min.js" integrity="sha512-aVKKRRi/Q/YV+4mjoKBsE4x3H+BkegoM/em46NNlCqNTmUYADjBbeNefNxYV7giUp0VxICtqdrbqU7iVaeZNXA==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>

<style>
	td{
		background: yellow;
		cursor: pointer;
		transition: .2s;
	}
	td:hover{
		background: white;
	}
	.tabelku {
		width: 100%;
		max-width: 400px;
	}
</style>


<table class="tabelku">
	<tr>
		<td>No</td>
		<td>Nama</td>
		<td>Alamat</td>
		<td>Aksi</td>
	</tr>

	<tr>
		<td>1</td>
		<td class="nama_mhs">Rizal</td>
		<td>Alamat</td>
		<td class="hapus"id="hapus_1">Hapus</td>
	</tr>

	<tr>
		<td>2</td>
		<td class="nama_mhs">johana</td>
		<td>Alamat</td>
		<td class="hapus"id="hapus_2">Hapus</td>
	</tr>

	<tr>
		<td>3</td>
		<td class="nama_mhs">Riziq</td>
		<td>Alamat</td>
		<td class="hapus"id="hapus_3">Hapus</td>
	</tr>

	<tr>
		<td>4</td>
		<td class="nama_mhs">Mail</td>
		<td>Alamat</td>
		<td class="hapus"id="hapus_4">Hapus</td>
	</tr>

	<tr>
		<td>5</td>
		<td class="nama_mhs">Imam</td>
		<td>Alamat</td>
		<td class="hapus"id="hapus_5">Hapus</td>
	</tr>


</table>


<script>
	$(document).ready(function(){
  $('.top').click(function(){
      let isi = $(this).text();
      let tid = $(this).prop('id');
      let rid = tid.split('__');
      let id_baris = rid[1];
      let nama = $('#nama__'+id_baris).text();

      if(isi=='Hapus'){
          let konfirmasi = confirm(`Ente Yakin ingin menghapus..! ${nama} ??`);
          if(!konfirmasi) return;

          $('#fade__'+id_baris).fadeOut();

      }else{
          alert("Ente milih : " + $(this).html() + "!");
      }
  })
})
</script>
