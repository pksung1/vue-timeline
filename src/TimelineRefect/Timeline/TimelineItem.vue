<template>
	<timeline-item-transition>
		<li :class="{'timeline-item': true, [alignClass]: true}">
			<div class="timeline-item-date">
				<div class="time-date" v-if="item.date && alignClass !== 'center'">
					{{item.date}}
				</div>
			</div>
			<div class="timeline-item-content">
				<timeline-badge :badge="badgeClass"></timeline-badge>
				<div :class="{'content-box': true, [contentBoxClass]: contentBoxClass}">
					<div class="timeline-title">
						<h4>{{item.title}}</h4>
					</div>
					<div class="timeline-content">
						{{item.content}}
					</div>
					<div class="time-date" v-if="item.date">
						{{item.date}}
					</div>
				</div>
			</div>
		</li>
	</timeline-item-transition>
</template>

<script>
import TimelineBadge from './TimelineBadge'
import {TimelineAlignTypes} from './code/code'
import TimelineItemTransition from './components/TimelineItemTransition'
export default {
	name: 'timeline-item',
	components: {
		TimelineBadge,
		TimelineItemTransition
	},
	props: {
		item: {
			type: Object,
			default () {
				return {}
			}
		}
	},
	computed: {
		alignClass () {
			if (this.item && this.item.align) {
				return this.item.align
			}
			return TimelineAlignTypes.LEFT
		},
		badgeClass () {
			if (this.item && this.item.badge) {
				return this.item.badge
			}
			return {}
		},
		contentBoxClass () {
			if (this.item && this.item.color) {
				return this.item.color
			}
			return false
		}
	}
}
</script>

<style>

</style>