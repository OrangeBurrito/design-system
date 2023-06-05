<script>
	import Image from '$lib/components/content/Image.svelte'
	import List from '$lib/components/content/List.svelte'
	import ListItem from '$lib/components/content/ListItem.svelte'
	import Table from '$lib/components/content/Table.svelte'
	import Page from '$lib/components/layout/Page.svelte'
	import Section from '$lib/components/layout/Section.svelte'
	import Sidebar from '$lib/components/layout/ui_shell/Sidebar.svelte'
	import SideNav from '$lib/components/navigation/SideNav.svelte'
	import ColorSection from '$lib/components/styleguide/ColorSection.svelte'
	import ColorToken from '$lib/components/styleguide/ColorToken.svelte'
	import TextToken from '$lib/components/styleguide/TextToken.svelte'

	const baseSpacing = [
		['space-0', '4px'],
		['space-1', '8px'],
		['space-2', '16px'],
		['space-3', '32px']
	]

	const semanticSpacing = [
		['space-inset-1', 'space-1', '8px'],
		['space-inset-2', 'space-3', '32px'],
		['space-inset-3', 'space-2', '16px'],
		['space-inset-squish-1', 'space-1 space-2', '8px 16px'],
		['space-inset-squish-1', 'space-2 space-3', '16px 32px'],
		['space-stack-0', 'space-0', '4px'],
		['space-stack-1', 'space-1', '8px'],
		['space-stack-2', 'space-2', '16px'],
		['space-stack-3', 'space-3', '32px'],
		['space-inline-1', 'space-1', '8px'],
		['space-inline-2', 'space-2', '16px'],
		['space-inline-3', 'space-3', '32px']
	]

    const pageTypes = [
        ['Default', 'default', 'the default page type, has a Page Header and optional Sidebar'],
        ['List', 'list', 'for long lists of items in table format. Has Page Header, Table, Table Navigation and optional Table Filters'],
        ['Detailed View', 'detailed', 'for detailed views, such as individual table items. Has Page Header, Info View and optional Table'],
    ]
</script>

<Page title="Style Guide"
        description="How to use the Design System">
	<Sidebar slot="sidebar">
		<SideNav>
			<a href="#colors">Colors</a>
			<a href="#typography">Typography</a>
			<a href="#spacing">Spacing</a>
			<a href="#layout">Layout</a>
			<a href="#components">Components</a>
		</SideNav>
		<!-- <SideNav title="">
            <a href="#typography">Typography</a>
        </SideNav> -->
	</Sidebar>

    <a href="/style_guide/test">testpage</a>

	<Section title="Colors" id="colors">
		<p>
			Design tokens are the building blocks of the design system. There are two levels, core and
			semantic.
		</p>

		<ColorSection title="Text Colors">
			<ColorToken color="--color-text)" title="Text" description="used for body text" />
			<ColorToken
				color="--color-text-subtle)"
				title="Text Subtle"
				description="used for labels and fields"
			/>
			<ColorToken
				color="--color-heading)"
				title="Heading Text"
				description="used for all headings"
			/>
			<ColorToken
				color="--color-text-link)"
				title="Link Text"
				description="used for inline links"
			/>
			<ColorToken
				color="--color-text-inverted)"
				title="Inverted Text"
				description="used on primary buttons"
			/>
		</ColorSection>

		<ColorSection title="Layout Colors">
			<ColorToken
				color="--color-background)"
				title="Background"
				description="used for the base background color"
			/>
			<ColorToken
				color="--color-background-alt)"
				title="Background Alt"
				description="used for all surfaces"
			/>
			<ColorToken color="--color-border)" title="Border" description="used for all borders" />
		</ColorSection>
	</Section>

	<section title="Typography" id="typography">
		<p>
			Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam voluptates animi amet ullam
			laborum natus!
		</p>
		<h3 id="colors">Font Size Tokens</h3>
		<TextToken description="used for main page titles only">
			<h1>Heading 1</h1>
		</TextToken>
		<TextToken description="used for all section headings">
			<h2>Heading 2</h2>
		</TextToken>
		<TextToken description="used for section sub headings">
			<h3>Heading 3</h3>
		</TextToken>
		<TextToken description="used for all body text">
			<p>Paragraph</p>
		</TextToken>
		<TextToken description="used for labels and item descriptions">
			<figcaption>Label</figcaption>
		</TextToken>

		<Image
			src="https://images.unsplash.com/photo-1481349518771-20055b2a7b24?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NHx8cmFuZG9tfGVufDB8fDB8fHww&w=1000&q=80"
			alt="Text Token Usage Guide"
			caption="Text Token Usage Guide"
		/>
	</section>

	<Section title="Spacing" id="spacing">
		<p>Use spacing tokens for all paddings and margins.</p>

		<h3>Base Tokens</h3>
		<Table headers={['Token', 'Value']} data={baseSpacing} />

		<h3>Semantic Tokens</h3>
		<Table headers={['Token', 'Core Token', 'Value']} data={semanticSpacing} />

        <h3>Usage</h3>
        <p>Inset spacings are used for inner paddings. Inset-squish spacings are used for buttons and labels.</p>
        <p>Stack spacing is used for vertical gaps between items. Inline spacing is used for horizontal gaps.</p>

        <Image
            src=""
            alt=""
            caption="Spacing Token Usage Guide"
        />
	</Section>

	<Section title="Layout and Structure" id="layout">
        <h3>Pages</h3>
        <p>All pages are wrapped inside a UI Shell component, which contains a Header, Sidebar and Main.</p>
        <!-- picture of UI Shell Component -->
        <p>Each route must use a <code>Page</code> component, which contains a Page Header.</p>
        <p>The Page Header has the page title, an optional description and Sidebar.</p>
        <!-- picture of page component with label -->
        <p>Pages have multiple variants to suit whatever page you're designing.</p>
        <!-- picture of list of predefined pages -->
        <h4>Types of Pages</h4>
        <Table headers={['Name', 'Type', 'Description', 'Image']} data={pageTypes}/>

        <!-- <h3>Layout Components</h3>
        <p>Use these components to structure and layout your pages.</p> -->
    </Section>

    <Section title="Components" id="components">
        <h3>Layout</h3>
            <List>
                <ListItem>UI Shell</ListItem>
                <ListItem>Page</ListItem>
                <ListItem>Layout</ListItem>
                <ListItem>Sidebar</ListItem>
                <ListItem>Section</ListItem>
                <ListItem>Accordion</ListItem>
                <ListItem>Card</ListItem>
            </List>
            <h3>Actions and Inputs</h3>
            <List>
                <ListItem>Button</ListItem>
                <ListItem>Input - text, number, date</ListItem>
                <ListItem>Checkbox</ListItem>
                <ListItem>Select</ListItem>
                <ListItem>Form</ListItem>
            </List>
            <h3>Content</h3>
            <List>
                <ListItem>Table</ListItem>
                <ListItem>Badge/Chip</ListItem>
                <ListItem>Image</ListItem>
                <ListItem>List</ListItem>
                <ListItem>Form</ListItem>
            </List>
        <h3>Navigation</h3>
        <List>
            <ListItem>Link</ListItem>
            <ListItem>Breadcrumb</ListItem>
            <ListItem>Tab</ListItem>
            <ListItem>Side Nav - use inside sidebar</ListItem>
        </List>
    </Section>
</Page>
