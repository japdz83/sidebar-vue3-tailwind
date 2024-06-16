<script setup>
import { RouterLink } from 'vue-router'

// export default{


// }
defineProps({
        is_expanded: {
            type: Boolean
        }
    })
</script>

<template>
	<aside class="h-screen w-[300px] bg-gray-800 " id="side-bar" :class="is_expanded === true ? 'side-bar-visible' : 'side-bar-close' ">
		<div class="bg-gray-700 h-[50px]">
			<div
				class="text-xl font-bold text-center flex items-center text-white justify-center h-full"
			>
				APP DEV
			</div>
		</div>
		<div
			class="flex flex-col justify-between h-[calc(100vh-3rem)] bg-gray-900 py-5"
		>
			<div class="menu-man text-left px-2 whitespace-nowrap">
				<div
					class="p-3 rounded-sm cursor-pointer text-gray-300 hover:text-white"
				>
					<router-link
						:to="{name: 'dashboard'}"
						class="px-2 flex space-x-2 items-center"
					>
						<span class="pi pi-microsoft"></span>
						<span class="">Dashboard</span>
					</router-link>
				</div>

				<div
					class="p-3 rounded-sm cursor-pointer text-gray-300 hover:text-white"
				>
					<router-link
						:to="{name: 'producto'}"
						class="px-2 flex space-x-2 items-center"
					>
						<span class="pi pi-microsoft"></span>
						<span class="">Producto</span>
					</router-link>
				</div>
			</div>
		</div>
	</aside>
</template>

<style>
#side-bar{
	overflow: hidden;
	transition: 300ms;
}

.side-bar-visible{
	width: 300px !important;
}

.side-bar-close{
	width: 50px !important;
}
</style>
