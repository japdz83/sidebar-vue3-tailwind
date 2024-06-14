<script setup>
import { ref } from vue
import { RouterLink, RouterView } from 'vue-router'
import Navbar from '../components/Navbar.vue'
import Sidebar from '../components/Sidebar.vue'

const openSidebar = ref(true)

// export default{

// 	data() {
// 		return {
// 			openSidebar: true
// 		}
// 	},
// }
</script>

<template>
	<div class="w-full h-full flex ">
		<Sidebar :dataOpenSideBar="openSidebar" />
		<div class="w-full h-full">
			<Navbar :dataOpenSideBar="openSidebar" />
			<div class="w-full h-[calc(100vh-50px)]">
				<RouterView />
			</div>
		</div>
	</div>
</template>
