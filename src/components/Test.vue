<template>
	<div class="test">
		<!--<div v-text="title"></div>
		<div v-if="showName">
			<p>{{ user.firstName }}</p>
		</div>
		<div v-else>
			<p>No puedo mostrar el nombre</p>
		</div>
		<hr>
		<ul>
			<li v-for="task in tasks">
				{{ task.title }}
			</li>
		</ul>
		<br>-->
		<!--<input type="text" v-on:keyup.enter="typedEnter">-->
		{{ msg }}
	</div>
</template>

<script>
	export default{
		data() {
			return {
				title: 'Hola VueJs',
				user : {
					firstName: 'Fabian',
					lastName: 'Orellana'
				},
				myHtml: '<h3>Hola vue</h3>',
				showName: false,
				tasks: [
					{title: 'eat'},
					{title: 'dinner'},
					{title: 'play'},
					{title: 'task'}
				]
			}
		},
		methods: {
			saludar(name) {
				alert('Wena ' + name)
			},
			typedEnter(e) {
				console.log('DIO UN ENTER');
			}
		},
		computed: {
			fullName() {
				return this.user.firstName + ' ' + this.user.lastName;
			}
		},
		props: {
			msg: {
				type: String,
				default: 'Mensaje por defecto'
			}
		}
	}
</script>

<style media="screen">
	.test{
		background-color: #eee;
	}
</style>