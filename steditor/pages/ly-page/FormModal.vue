<template>
	<el-dialog v-model="dialogVisible" title="模版编辑" width="500">
		123
	</el-dialog>
</template>

<script>
	export default {
		data() {
			return {
				dialogVisible: false
			}
		},
		methods: {
			onAdd() {
				this.onEdit()
			},
			onEdit() {
				this.dialogVisible = true
			}
		}
	}
</script>