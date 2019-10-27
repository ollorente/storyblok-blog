<template>
	<section id="posts">
		<PostPreview
			v-for="post in posts"
			:key="post.id"
			:title="post.title"
			:excerpt="post.previewText"
			:thumbnailImage="post.thumbnailUrl"
			:id="post.id" />
	</section>
</template>

<script>
	import PostPreview from '@/components/Blog/PostPreview.vue'

	export default {
		components: {
			PostPreview
		},
		data () {
			return {
				posts: [
					{
						title: 'A new beginning',
						previewText: 'This will be awesome, dont miss it!.',
						thumbnailUrl: 'https://res.cloudinary.com/dbszizqh4/image/upload/v1571710286/gastronomia/oy9ux1kimcfbaolt54fi.jpg',
						id: 'a-new-beginning'
					},
					{
						title: 'A Second beginning',
						previewText: 'This will be awesome, dont miss it!.',
						thumbnailUrl: 'https://res.cloudinary.com/dbszizqh4/image/upload/v1571669152/noticias/p0rgtienlksh9h5r7oba.jpg',
						id: 'a-second-beginning'
					}
				]
			}
	}
	}
</script>

<style scoped>
	#posts {
		padding-top: 2rem;
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
	}

	@media (min-width: 35rem) {
		#posts {
			flex-direction: row;
		}
	}
</style>
