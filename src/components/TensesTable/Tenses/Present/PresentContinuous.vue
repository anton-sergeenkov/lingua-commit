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
    <h2 v-if="details">Present Continuous</h2>

    <div class="table" :class="details && 'table-details'">
        <Table>
            <Row>
                <ColSentence rowspan="3">+</ColSentence>
                <Col>I</Col>
                <ColAccent>am</ColAccent>
                <ColVerb rowspan="3">V<sub>ing</sub></ColVerb>
            </Row>
            <Row>
                <Col>He / She / It</Col>
                <ColAccent>is</ColAccent>
            </Row>
            <Row>
                <Col>You / We / They</Col>
                <ColAccent>are</ColAccent>
            </Row>
        </Table>

        <Table>
            <Row>
                <ColSentence>-</ColSentence>
                <Col>___</Col>
                <ColAccent>'m not / isn't / aren't</ColAccent>
                <ColVerb>V<sub>ing</sub></ColVerb>
            </Row>
        </Table>

        <Table>
            <Row>
                <ColSentence>?</ColSentence>
                <ColAccent>Am / Is / Are</ColAccent>
                <Col>___</Col>
                <ColVerb>V<sub>ing</sub></ColVerb>
            </Row>
        </Table>

        <TextComment>
            Now,
            At the moment
        </TextComment>
    </div>

<div v-if="details" class="data-details">

<hr />

<!------------------------------------------------------------->
<h4>Виды вопросов</h4>
<!------------------------------------------------------------->
<ul>
    <li><Op>+</Op> <i>He <s>is</s> eat<s>ing</s> now</i></li>
    <li><Op>-</Op> <i>He <s>isn't</s> eat<s>ing</s> now</i></li>
    <li><Op>?</Op> <i><s>Is</s> he eat<s>ing</s> now?</i></li>
</ul>

<Continuous />

</div>
</template>
