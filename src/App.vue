<script setup lang="ts">
const skill_categorys = [
	{
		title: 'ウェブ',
		theme_color: '#62b6ea',
		skills: [
			{
				name: 'HTML',
				year: 5,
				description: '実務経験あり'
			},
			{
				name: 'CSS',
				year: 5,
				description: '実務経験あり'
			},
			{
				name: 'JavaScript',
				year: 5,
				description: '実務経験あり'
			},
			{
				name: 'SCSS',
				year: 3,
				description: '実務経験あり'
			},
			{
				name: 'TypeScript',
				year: 2,
				description: '実務経験あり'
			},

		],
	},
	{
		title: 'アプリ',
		theme_color: '#6fba4f',
		skills: [
			{
				name: 'Kotlin',
				year: 0.5,
				description: '独学'
			},
			{
				name: 'Java',
				year: 0.5,
				description: '独学'
			},
		]
	},
	{
		title: 'デザイン',
		theme_color: '#ba564f',
		skills: [
			{
				name: 'Adobe Photoshop',
				year: 2,
				description: '実務経験あり'
			},
			{
				name: 'Adobe Illustrator',
				year: 2,
				description: '実務経験あり'
			},
			{
				name: 'Adobe XD',
				year: 2,
				description: '実務経験あり'
			},
			{
				name: 'Adobe XD',
				year: 2,
				description: '実務経験あり'
			},
			{
				name: 'Figma',
				year: 2,
				description: '実務経験あり'
			},

		]
	}
]

</script>

<template>
	<main>
		<div class="cover">
			<img src="../src/assets/forest-road-1.jpeg" alt="cover-image">
			<b>Ameryu716`s Portforio</b>
		</div>
		<div class="skills">
			<p>スキル</p>
			<div class="row wrap g-5">

				<div class="column skill" v-for="category in skill_categorys">
					<div class="tag skill-category ml-2" :style="{
						'border-color': category.theme_color,
						'color': '#fff',
						'background-color': category.theme_color,
					}">
						<b>{{ category.title }}</b>
					</div>
					<div class="card">

						<div class="step row" v-for="skill in category.skills">
							<div class="skill-word">
								<b>{{ skill.name }}</b>
							</div>
							<span class="ml-auto">{{ skill.year }}年</span>
							<span>/</span>

							<span>{{ skill.description }}</span>
						</div>
					</div>
				</div>
			</div>

		</div>
	</main>
</template>

<style scoped lang="scss">
main {
	&>* {
		margin-bottom: 1rem;
	}



	.cover {
		position: relative;
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100vw;
		height: 80vh;


		img {
			position: absolute;
			object-fit: cover;
			height: 100%;
			width: 100%;
		}

		b {
			font-size: 4rem;
			z-index: 1;
			color: rgba($color: #fff, $alpha: 0.8);
		}
	}

	.skills {
		margin: 1rem auto;
		width: 900px;

		.skill {
			width: 40%;

			.skill-category {
				display: inline;
				// border-color: rgb(22, 111, 174);
				// color: rgb(22, 111, 174);
				border-width: 2px;
				border-radius: 0.5rem 0.5rem 0 0;
				border-bottom: none;
				background-color: #fff;
			}

			.card {
				// margin-top: 1px;
				width: 400px;

				.step {
					// background-color: #eee;
					border: solid 1px;
					border-radius: 0.3rem;
					margin-bottom: 1rem;
					padding: 0.5rem;
					width: auto;
					gap: 5px;

					.skill-word {
						width: 50%;
					}

				}
			}
		}

	}

}
</style>
