<template>
	<ul class="timeline-group">
		<timeline-item
			v-for="item in timelines"
			:key="item.id"
			:item="item"
		></timeline-item>
	</ul>
</template>

<script>
import TimelineItem from './TimelineItem'
export default {
	name: 'timeline-group',
	components: {
		TimelineItem
	},
	props: {
		name: {
			type: String,
			default: () => {
				return ''
			}
		},
		timelines: {
			type: Array,
			default: () => {
				return []
			}
		}
	}
}
</script>

<style>

</style>