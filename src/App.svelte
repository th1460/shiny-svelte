<script>import {
            Header,
            HeaderNav,
            HeaderNavItem,
            HeaderNavMenu,
            SkipToContent,
            Content,
            Grid,
            Row,
            Column,
            Toggle
} from 'carbon-components-svelte';

let isSideNavOpen = false;
let toggled = false;
            </script>
<main>
  <Header company="IBM" platformName="Carbon Svelte" bind:isSideNavOpen>
    <svelte:fragment slot="skip-to-content"></svelte:fragment>
  </Header>
  <Content>
    <Grid>
      <Row>
        <Column>
          <h1>Welcome</h1>
          <br/>
          <Toggle labelText='Toggle' bind:toggled/>
        </Column>
      </Row>
    </Grid>
  </Content>
</main>
