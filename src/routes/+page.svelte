<script>
	import 'carbon-components-svelte/css/g10.css';

	import {
		Header,
		HeaderNav,
		HeaderNavItem,
		HeaderNavMenu,
		SideNav,
		SideNavItems,
		SideNavMenu,
		SideNavMenuItem,
		SideNavLink,
		SideNavDivider,
		SkipToContent,
		Content,
		Grid,
		Row,
		Column
	} from 'carbon-components-svelte';

	let isSideNavOpen = false;
	import CopenhagenSnekkja from 'carbon-pictograms-svelte/lib/CopenhagenSnekkja.svelte';
</script>

<svelte:head>
	<title>Afritech</title>
	<meta name="description" content="Your gateway into Africa's tech ecosystem" />
</svelte:head>

<Header company="Afritech" bind:isSideNavOpen persistentHamburgerMenu={true}>
	<svelte:fragment slot="skip-to-content">
		<SkipToContent />
	</svelte:fragment>
	<HeaderNav>
		<!-- <HeaderNavItem href="/" text="Link 1" />
        <HeaderNavItem href="/" text="Link 2" />
        <HeaderNavItem href="/" text="Link 3" />
        <HeaderNavMenu text="Menu">
        <HeaderNavItem href="/" text="Link 1" />
        <HeaderNavItem href="/" text="Link 2" />
        <HeaderNavItem href="/" text="Link 3" />
        </HeaderNavMenu>
        <HeaderNavItem href="/" text="Link 4" /> -->
	</HeaderNav>
</Header>

<SideNav bind:isOpen={isSideNavOpen}>
	<SideNavItems>
		<!-- <SideNavLink text="Link 1" />
    <SideNavLink text="Link 2" />
    <SideNavLink text="Link 3" />
    <SideNavMenu text="Menu">
    <SideNavMenuItem href="/" text="Link 1" />
    <SideNavMenuItem href="/" text="Link 2" />
    <SideNavMenuItem href="/" text="Link 3" />
    </SideNavMenu>
    <SideNavDivider />
    <SideNavLink text="Link 4" /> -->
	</SideNavItems>
</SideNav>

<Content style="display: flex;">
	<Grid style="display: flex; flex-direction: column; gap: 1rem; justify-content: center; align-items: center;"> 
		<Row>
			<Column>
				<h1>Welcome to AfriTech</h1>
				<p style="text-align: center;">Your gateway into the tech industry in Africa</p>
			</Column>
		</Row>
		<Row>
			<Column>
				<CopenhagenSnekkja />
			</Column>
		</Row>
        <Row>
            <a href="https://bsky.app/profile/afritech.fyi" target="_blank" style="display: flex; gap: 0.25rem;">
                Follow us on Bluesky<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" width="16" height="16">
                    <!--!Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.-->
                    <path fill="#1285FE" d="M111.8 62.2C170.2 105.9 233 194.7 256 242.4c23-47.6 85.8-136.4 144.2-180.2c42.1-31.6 110.3-56 110.3 21.8c0 15.5-8.9 130.5-14.1 149.2C478.2 298 412 314.6 353.1 304.5c102.9 17.5 129.1 75.5 72.5 133.5c-107.4 110.2-154.3-27.6-166.3-62.9l0 0c-1.7-4.9-2.6-7.8-3.3-7.8s-1.6 3-3.3 7.8l0 0c-12 35.3-59 173.1-166.3 62.9c-56.5-58-30.4-116 72.5-133.5C100 314.6 33.8 298 15.7 233.1C10.4 214.4 1.5 99.4 1.5 83.9c0-77.8 68.2-53.4 110.3-21.8z"/>
                </svg>
            </a>
        </Row>
	</Grid>
</Content>

