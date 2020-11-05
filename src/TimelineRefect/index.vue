<template>
	<div>
		<h1>Timeline Refect</h1>
		<button @click="appendData()">Append</button>
		<div class="timeline-section">
			<timeline :timeline-items="timelineItems">
				<template v-slot:title>
					<h3>~~차량 타임라인</h3>
				</template>
			</timeline>
		</div>
	</div>
</template>

<script>
import Timeline from './Timeline/Timeline'
export default {
	components: {
		Timeline
	},
	data () {
		return {
			timelineItems: [
				{
					groupName: 'groupName-1',
					template: '',
					timelines: [
						{
							id: 1,
							title: 'title',
							content: 'content',
							date: '2020-11-10',
							align: 'right',
							badge: {
								icon: '',
								color: 'red',
								size: 'regular'
							}
						},
						{
							id: 2,
							title: 'title1',
							content: 'content',
							date: '2020-11-10',
							align: 'left',
							badge: {
								icon: '',
								color: 'red',
								size: 'large'
							}
						},
						{
							id: 3,
							title: 'title2',
							content: 'content',
							date: '2020-11-10',
							align: 'center',
							badge: {
								icon: '',
								color: 'blue',
								size: 'small'
							}
						},
						{
							id: 4,
							title: 'title3',
							content: 'content',
							date: '2020-11-10',
							align: 'left',
							color: 'orange',
							badge: {
								icon: '',
								color: 'orange',
								size: 'small'
							}
						},
						{
							id: 5,
							title: 'title4',
							content: 'content',
							date: '2020-11-10',
							align: 'right',
							badge: {
								icon: '',
								color: 'sky',
								size: 'small'
							}
						},
						{
							id: 6,
							title: 'title4',
							content: 'content',
							date: '2020-11-10',
							align: 'right',
							color: 'red',
							badge: {
								icon: '',
								color: 'blue',
								size: 'large'
							}
						}
					]
				}
			]
		}
	},
	methods: {
		appendData () {
			console.log('appendData')
			this.timelineItems[0].timelines.push(
				{
					id: Date.now(),
					title: `title ${Date.now()}`,
					content: 'content',
					date: '2020-11-10',
					align: 'right',
					color: 'red',
					badge: {
						icon: '',
						color: 'blue',
						size: 'large'
					}
				}
			)
		}
	}
}
</script>

<style lang="scss" scoped>
</style>