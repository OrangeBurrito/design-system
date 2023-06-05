<script lang="ts">
	import Button from "$lib/components/actions/Button.svelte";
	import ButtonGroup from "$lib/components/actions/ButtonGroup.svelte";
	import Form from "$lib/components/actions/Form.svelte";
	import Input from "$lib/components/actions/Input.svelte";
	import Select from "$lib/components/actions/Select.svelte";
import Page from "$lib/components/layout/Page.svelte";
</script>

<Page title="Homepage"
    description="the repository for the OrangeSystem design system">
    <a href="/style_guide">Style Guide</a>

    <Form title="Bee Questionnaire">
        <Input label="Enter Favorite Bees" placeholder="input something"/>

        <Select>
            <option value="1">first</option>
            <option value="2">second</option>
            <option value="3">third</option>
        </Select>
        
        <ButtonGroup>
            <Button type="primary" icon="alert-triangle">Click Here</Button>
            <Button type="secondary">Or not...</Button>
        </ButtonGroup>
    </Form>
</Page>