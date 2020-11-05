<template>
	<div :class="{
		'badge': true,
		[badge.color]: badge.color,
		[badge.size]: badge.size
	}">
		<!-- <i class="fas fa-address-card"></i> -->
	</div>
</template>

<script>
export default {
	name: 'timeline-badge',
	props: {
		badge: {
			type: Object,
			default () {
				return {
					color: 'blue',
					size: 'regular',
					icon: ''
				}
			}
		}
	}
}
</script>

<style>

</style>