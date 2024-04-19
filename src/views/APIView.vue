<script setup lang="ts">
import { ref, inject, getCurrentInstance } from "vue"
import { useUserPiniaStore } from "../stores/users"
import '@mdi/font/css/materialdesignicons.css'
import { log, fail, getNames } from "../components/MyConsoleUtil"
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
/* -------------------------------------------------------------------------- */

/* %%%%%%  On Page Load %%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%% */

async function fetchData() {
	// return await fetch('https://o8p0r20xo5.execute-api.us-east-1.amazonaws.com/default/GetSecretLambda-03')
	// return await fetch('https://o8p0r20xo5.execute-api.us-east-1.amazonaws.com/default/GetSecretLambda-03/name')
	// return await fetch('https://o8p0r20xo5.execute-api.us-east-1.amazonaws.com/default/GetSecretLambda-03/webhook-secret-01')
	// return await fetch('https://o8p0r20xo5.execute-api.us-east-1.amazonaws.com/default/GetSecretLambda-03/secret-key-test-01')
	return await fetch('https://o8p0r20xo5.execute-api.us-east-1.amazonaws.com/default/GetSecretLambda-03/findme')
	// return await fetch('')
	.then(resp => {
		if (!resp.ok) {
			throw `Server error: [${resp.status}] [${resp.statusText}] [${resp.url}]`;
		}
		// console.log("ONE")
		return resp.text();
		// resp.json();
		// return resp.json();
	})
	.then(receivedJson => {
		// your code with json here...
		// console.log("TWO")
		console.log(receivedJson)
	})
	.catch(err => {
		console.debug("Error in fetch", err);
	});
}
fetchData()

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