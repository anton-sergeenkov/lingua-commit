<script setup>
import Col from '@/uikit/TableElements/Col.vue';
import ColAccent from '@/uikit/TableElements/ColAccent.vue';
import ColSentence from '@/uikit/TableElements/ColSentence.vue';
import ColVerb from '@/uikit/TableElements/ColVerb.vue';
import Row from '@/uikit/TableElements/Row.vue';
import Table from '@/uikit/TableElements/Table.vue';
import TableWrapper from '@/uikit/TableElements/TableWrapper.vue';
import TextComment from '@/uikit/TableElements/TextComment.vue';
import TextData from '@/uikit/TableElements/TextData.vue';

import Op from '@/uikit/Options.vue';
import Info from '@/uikit/Info.vue';

defineProps({
	details: { type: Boolean, required: false },
});
</script>

<template>
	<h2 v-if="details">Past Perfect Continuous</h2>

    <div class="table" :class="details && 'table-details'">
		<Table>
			<Row>
				<ColSentence>+</ColSentence>
				<ColAccent>*</ColAccent>
				<ColAccent>had <s>been</s></ColAccent>
				<ColVerb>V<sub>ing</sub></ColVerb>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>-</ColSentence>
				<Col>___</Col>
				<ColAccent>hadn't <s>been</s></ColAccent>
				<ColVerb>V<sub>ing</sub></ColVerb>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>?</ColSentence>
				<ColAccent>Had</ColAccent>
				<ColAccent>___ <s>been</s></ColAccent>
				<ColVerb>V<sub>ing</sub></ColVerb>
			</Row>
		</Table>
	
		<TextComment>
			Yesterday since 3 p.m.,
			For some time in the past
		</TextComment>
	</div>

<div v-if="details" class="data-details">

<hr />

</div>
</template>
