<template>
	<v-app>
		<v-app-bar app class="gradient"

		 >
			<v-app-bar-nav-icon></v-app-bar-nav-icon>
			<v-toolbar-title>ezper</v-toolbar-title>
			<v-spacer></v-spacer>
			<v-btn icon>
				<v-icon>mdi-magnify</v-icon>
			</v-btn>
			<v-btn icon>
				<v-icon>mdi-heart</v-icon>
			</v-btn>
			<v-btn icon>
				<v-icon>mdi-dots-vertical</v-icon>
			</v-btn>
		</v-app-bar>
		<v-content>
			<!-- Login Module -->
			<v-card width="400" class="mx-auto mt-5">
				<v-card-title>
					<h1 class="display-1">Login</h1>
				</v-card-title>
				<v-card-text>
					<v-form>
						<v-text-field label="Username" prepend-icon="mdi-account-circle" />
						<v-text-field
							:type="showPassword ? 'text' : 'password'"
							label="Password"
							prepend-icon="mdi-lock"
							:append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
							@click:append="showPassword = !showPassword"
						/>
					</v-form>
				</v-card-text>
				<v-divider></v-divider>
				<v-card-actions>
					<v-btn color="success">Register</v-btn>
					<v-spacer></v-spacer>
					<v-btn class="gradient">Login</v-btn>
				</v-card-actions>
			</v-card>
		</v-content>
		<v-footer color="primary lighten-1" padless>
			<v-layout justify-center wrap>
				<v-btn
					v-for="link in links"
					:key="link"
					color="white"
					text
					rounded
					class="my-2"
				>
					{{ link }}
				</v-btn>
				<v-flex primary lighten-2 py-4 text-center white--text xs12>
					{{ new Date().getFullYear() }} — <strong>ezper Dashboard</strong>
				</v-flex>
			</v-layout>
		</v-footer>
	</v-app>
</template>

<script>
export default {
	name: 'App',
	data() {
		return {
			showPassword: false,
			links: ['Home', 'Login']
		}
	}
}
</script>

<style scoped>
.gradient2 {
	background: #3A1C71;
	background: -webkit-linear-gradient(to right, #FFAF7B, #D76D77, #3A1C71);
	background: linear-gradient(to right, #FFAF7B, #D76D77, #3A1C71);
}
.gradient{
	background: linear-gradient(90deg, #fcff9e 0%, #c67700 100%);
}


.gradient1 {
	background: rgb(131,58,180);
	background: linear-gradient(90deg, rgba(131,58,180,1) 0%, rgba(253,29,29,1) 50%, rgba(252,176,69,1) 100%);
}
</style>
