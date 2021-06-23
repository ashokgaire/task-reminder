<template>
	<header>
        <h1> Task Tracker </h1>

        <Button @showhide-task="$emit('showhide-task')" :text= "showAddTask ? 'Close':'Add Task'"
:color="showAddTask ? 'Red': 'Green'" />
	</header>

</template>


<script>

import Button from './Button'
export  default {
	name: 'Header',
	props: {
		title: {
			type: String,
			default: "Hello ",
		},
		showAddTask: {
			type: Boolean,
			default: false
		}
	},
	components:
	{
		Button,
	},
	emits:['showhide-task'],
}
</script>

<style scoped>

header{

	display: flex;
	justify-content: space-between;
	align-items: center;
	margin-bottom: 20px;
}

</style>