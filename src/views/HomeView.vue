<script setup>
import { ref } from 'vue'
import { RouterLink, RouterView } from 'vue-router'
import Navbar from '../components/Navbar.vue'
import Sidebar from '../components/Sidebar.vue'

// const is_expanded = ref(true)
const is_expanded = ref(localStorage.getItem("is_expanded") === "true")

// export default{

// 	data() {
// 		return {
// 			openSidebar: true
// 		}
// 	},
// }

const ToggleSidebar = () => {
	is_expanded.value = !is_expanded.value
	localStorage.setItem("is_expanded", is_expanded.value)
	// alert('Estoy desde el padre')
}
</script>

<template>
	<div class="w-full h-full flex ">
		<Sidebar :is_expanded="is_expanded" />
		<div class="w-full h-full">
			<Navbar :is_expanded="is_expanded" :ToggleSidebar="ToggleSidebar" />
			<div class="w-full h-[calc(100vh-50px)]">
				<RouterView />
			</div>
		</div>
	</div>
</template>
