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
