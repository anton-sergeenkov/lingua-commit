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

import Continuous from '../Continuous.vue';

defineProps({
	details: { type: Boolean, required: false },
});
</script>

<template>
	<h2 v-if="details">Past Continuous</h2>

	<div class="table" :class="details && 'table-details'">
		<Table>
			<Row>
				<ColSentence rowspan="2">+</ColSentence>
				<Col>I / He / She / It </Col>
				<ColAccent>was</ColAccent>
				<ColVerb rowspan="2">V<sub>ing</sub></ColVerb>
			</Row>
			<Row>
				<Col>You / We / They </Col>
				<ColAccent>were</ColAccent>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>-</ColSentence>
				<Col>___</Col>
				<ColAccent>wasn't / weren't</ColAccent>
				<ColVerb>V<sub>ing</sub></ColVerb>
			</Row>
		</Table>

		<Table>
			<Row>
				<ColSentence>?</ColSentence>
				<ColAccent>Was / Were</ColAccent>
				<Col>___</Col>
				<ColVerb>V<sub>ing</sub></ColVerb>
			</Row>
		</Table>
		<TextComment>
			Yesterday at 3 p.m.,
			Yesterday from 6 till 7,
			When you came
		</TextComment>
	</div>

<div v-if="details" class="data-details">

<hr />

<!------------------------------------------------------------->
<h4>Виды вопросов</h4>
<!------------------------------------------------------------->
<ul>
    <li><Op>+</Op> <i>I <s>was</s> eat<s>ing</s> from 5 to 6 yesterday</i></li>
    <li><Op>-</Op> <i>I <s>wasn’t</s> eat<s>ing</s> from 5 to 6 yesterday</i></li>
    <li><Op>?</Op> <i><s>Was</s> I eat<s>ing</s> from 5 to 6 yesterday?</i></li>
</ul>

<!------------------------------------------------------------->
<h4>Вариантивность</h4>
<!------------------------------------------------------------->
<ul>
	<li><i>I <s>was</s> eat<s>ing</s> from 5 to 6 yesterday</i></li>
	<li><i>Yesterday I <s>was</s> eat<s>ing</s> from 5 to 6</i></li>
	<li><i>I <s>was</s> eat<s>ing</s> yesterday from 5 to 6</i></li>
</ul>

<Continuous />

</div>
</template>
