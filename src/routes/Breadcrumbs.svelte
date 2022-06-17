<script>
	import {
		Page,
		Navbar,
		NavbarBackLink,
		BlockTitle,
		BlockHeader,
		Block,
		Breadcrumbs,
		BreadcrumbsItem,
		BreadcrumbsSeparator,
		BreadcrumbsCollapsed,
		Popover,
		List,
		ListItem,
		Link
	} from 'konsta/svelte';

	let popoverOpened = false;
</script>

<Page>
	<Navbar title="Breadcrumbs" />

	<BlockTitle>Basic</BlockTitle>
	<Block strong>
		<Breadcrumbs>
			<BreadcrumbsItem>
				<Link colors={{ text: 'text-inherit' }}>Home</Link>
			</BreadcrumbsItem>
			<BreadcrumbsSeparator />
			<BreadcrumbsItem>
				<Link colors={{ text: 'text-inherit' }}>Catalog</Link>
			</BreadcrumbsItem>
			<BreadcrumbsSeparator />
			<BreadcrumbsItem active>Phones</BreadcrumbsItem>
		</Breadcrumbs>
	</Block>
</Page>
