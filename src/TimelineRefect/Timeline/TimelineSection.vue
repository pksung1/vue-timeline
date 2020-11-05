<template>
  <div class="timeline-section">
        <timeline-group
            v-for="group in timelineItems"
            :key="group.name"
            :name="group.name"
            :timelines="group.timelines"
        ></timeline-group>
  </div>
</template>

<script>
import {TimelineAlignTypes} from './code/code'

import TimelineGroup from './TimelineGroup'
export default {
    name: 'timeline-section',
    components: {
        TimelineGroup
    },
    props: {
        align: {
            type: String,
            default () {
                return TimelineAlignTypes.LEFT
            }
        },
        timelineItems: {
            type: Array,
            default () {
                return []
            }
        }
    },
    computed: {
        sectionAlignClass: () => {
            if (this.align === TimelineAlignTypes.LEFT) {
                return 
            }
        }
    }
}
</script>

<style>

</style>