<script setup lang="ts">
</script>

<template>
	<main>
		<div class="cover">
			<img src="../src/assets/forest-road-1.jpeg" alt="cover-image">
			<b>Ameryu716`s Portforio</b>
		</div>
		<div class="skills">
			<p>スキル</p>
			<div class="row">

				<div class="column skill">
					<div class="tag skill-category">
						<b>ウェブ</b>
					</div>
					<div class="card">
						<div class="step">
							<div class="row">
								<div class="skill-word">
									<b>HTML</b>
								</div>
								<span>5年</span>
								<span>/</span>

								<span>実務経験あり</span>
							</div>
						</div>
						<div class="step">
							<div class="row">
								<div class="skill-word">
									<b>CSS</b>
								</div>
								<span>5年</span>
								<span>/</span>
								<span>実務経験あり</span>
							</div>
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

			.skill-category {
				display: inline;
				border-color: rgb(22, 111, 174);
				color: rgb(22, 111, 174);
				border-radius: 0.5rem 0.5rem 0 0;
				background-color: #eee;
			}

			.card {
				width: 400px;

				.step {
					background-color: #eee;
					border-radius: 0.3rem;
					margin-bottom: 1rem;
					padding: 0.5rem;

					.row {
						gap: 5px;

						.skill-word {
							width: 50%;
						}
					}

				}
			}
		}

	}

}
</style>
