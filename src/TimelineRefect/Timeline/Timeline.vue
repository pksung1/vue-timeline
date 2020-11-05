<template>
	<div>
		<div>
			<slot name="title"></slot>
		</div>
		<div class="timeline">
			<timeline-section :timelineItems="timelineItems"></timeline-section>
		</div>
  </div>
</template>

<script>
import TimelineSection from './TimelineSection'
import './style/style.scss'
export default {
	components: {
		TimelineSection
	},
	props: {
		timelineItems: {
			type: [Array],
			default: () => {
				return []
			}
		}
	},
	mounted () {
		console.log(this.timelineItems)
	}
}
</script>

<style lang="scss" scoped></style>