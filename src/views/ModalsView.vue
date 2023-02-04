<template>
	<div class="modals">
		<h1>Modals</h1>
		<div>
			<label>
				Show dark modals?
				<input v-model="showDarkModals" type="checkbox" />
			</label>
		</div>
		<button @click="showModal = true">Show modal</button>
		<component 
			v-model="showModal" 
			:is="showDarkModals ? ModalDark : Modal"			
			title="My modal title (via prop)"
		>
			<template #title>My new Title</template>
			<p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Provident illum nostrum dolore unde tempore amet quidem molestiae similique facilis voluptates asperiores voluptatibus culpa numquam laborum, totam sapiente quod nisi quo?</p>
		</component>
	</div>
</template>

<script setup>
	// imports 
	import { ref } from 'vue'
	import Modal from '@/components/Modal.vue'
	import ModalDark from '@/components/ModalDark.vue'

	// modals
	const showModal = ref(false)
	const showDarkModals = ref(false)
</script>

