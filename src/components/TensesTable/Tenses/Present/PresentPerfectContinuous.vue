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
    <h2 v-if="details">Present Perfect Continuous</h2>

    <div class="table" :class="details && 'table-details'">
		<Table>
			<Row>
				<ColSentence rowspan="2">+</ColSentence>
				<Col>I / You / We / They</Col>
				<ColAccent>have <s>been</s></ColAccent>
				<ColVerb rowspan="3">V<sub>ing</sub></ColVerb>
			</Row>
			<Row>
				<Col>He / She / It</Col>
				<ColAccent>has <s>been</s></ColAccent>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>-</ColSentence>
				<Col>___</Col>
				<ColAccent>haven't <s>been</s> / <br/> hasn't <s>been</s></ColAccent>
				<ColVerb>V<sub>ing</sub></ColVerb>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>?</ColSentence>
				<ColAccent>Have / Has</ColAccent>
				<Col>___ <s>been</s></Col>
				<ColVerb>V<sub>ing</sub></ColVerb>
			</Row>
		</Table>

		<TextComment>
			Since 3 p.m.,
			For a long time,
			For a month
		</TextComment>
	</div>

<div v-if="details" class="data-details">

<hr />

</div>
</template>
