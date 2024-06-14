<script setup>
import InputGroup from 'primevue/inputgroup';
import InputGroupAddon from 'primevue/inputgroupaddon';
import Button from 'primevue/button';
import Avatar from 'primevue/avatar';

// export default{
// props:{
// 		dataOpenSideBar: Boolean
// 	},

// }

defineProps({
        openSidebar: {
            type: Boolean
        }
    })
</script>

<template>
	<header class="w-full bg-gray-100 mb-3 shadow-md">
		<div class="flex justify-between items-center h-[60px]">
			<div class="p-3 hover:bg-gray-50 cursor-pointer">
				<i class="pi pi-bars"></i>
			</div>

			<div class="py-2">
				{{ openSidebar }}
				<input
					type="text"
					placeholder="Buscar..."
					class="p-2 border-black"
				/>
			</div>

			<div class="p-3 flex gap-3">
				<span class="text-md">Admin</span>
				<Avatar
					icon="pi pi-user"
					class="mr-3"
					size="xlarge"
					shape="circle"
				/>
			</div>
		</div>
	</header>
</template>

<style scoped>
header{
    width: 100% !important;
}
</style>
