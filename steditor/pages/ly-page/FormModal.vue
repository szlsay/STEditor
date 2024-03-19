<template>
	<el-dialog v-model="dialogVisible" title="模版编辑" width="50%">
		{{formData}}
		<el-form :model="formData" label-width="auto" style="max-width: 600px">
			<el-form-item label="标题">
				<el-input v-model="formData.title" />
			</el-form-item>
			<el-form-item label="JSON数据字符串">
				<el-input v-model="formData.json" />
			</el-form-item>
			<el-form-item label="自定义组件">
				<el-input v-model="formData.component" />
			</el-form-item>
			<el-form-item label="创建时间">
				<el-date-picker v-model="formData.create_time" type="datetime" value-format="x" />
			</el-form-item>
			<el-form-item label="更新时间">
				<el-date-picker v-model="formData.update_time" type="datetime" value-format="x" />
			</el-form-item>
		</el-form>
	</el-dialog>
</template>

<script>
	export default {
		data() {
			return {
				dialogVisible: false,
				formData: {
					"title": null,
					"json": null,
					"component": null,
					"create_time": null,
					"update_time": null
				}
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