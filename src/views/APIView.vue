<script setup lang="ts">
import { ref, inject, getCurrentInstance } from "vue"
import { useUserPiniaStore } from "../stores/users"
import '@mdi/font/css/materialdesignicons.css'
import { fail } from "../components/MyConsoleUtil"
/* -------------------------------------------------------------------------- */
const piniaStore = useUserPiniaStore()		// Leave this for now
const cb = ref()
const cbLbl = ref("Unchecked")
const btnTxt = ref("Hello-Start")
const SelCb = () => {
	cbLbl.value = cb.value ? "Unchecked" : "Checked"
	cb.value = !cb.value
}
const SelBtn = () => {
	btnTxt.value = btnTxt.value === "Hello" ? "Goodbye" : "Hello"
}
/* %%%%%%  On Page Load %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%% */

/* %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%% */
</script>

<template>
		<div>
			<h5 class="d-flex justify-center" >( APIView )</h5>
			<v-checkbox class="d-flex justify-center" :label="cbLbl" @click="SelCb" />
			<div class="d-flex justify-center">
				<v-btn :text="btnTxt" @click="SelBtn" />
			</div>
		</div>
</template>