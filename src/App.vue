<template>
  <div>
      <h1>Mis Productos</h1>
      <ul>
          <li v-for="producto in productos" :key="producto.id">
              {{ producto.nombre }} 
          </li>
      </ul>
  </div>

</template>

<script>
import firebaseApp from '../../firebaseConfig.js'
import { getFirestore, collection, getDocs } from 'firebase/firestore'
export default {
  name: 'FirebaseComponent',
  data() {
      return {
          productos: [],
      }
  },
  async mounted(){
      try {
          const db = getFirestore(firebaseApp)
          const querySnapshot = await getDocs(collection(db,'productos'))
          querySnapshot.forEach((doc) => {
               this.productos.push({id:doc.id, ...doc.data()}) 
               //this.productos.push({id:doc.id, nombre, tamaño,}) 
          })
      } catch (err) {
          console.error(err)
      }
  }
}
</script>