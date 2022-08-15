#' Render Svelte Application
#'
#' @export
app_svelte <- function() {
    
    app <- tagList(
        tags$script(
            "import {
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
            "
        ),
        tags$main(tag("Header", 
                      list(company = "IBM",
                           platformName = "Carbon Svelte",
                           `bind:isSideNavOpen` = NA,
                           tag("svelte:fragment", 
                               list(slot = "skip-to-content")))),
                  tag("Content", 
                      list(tag("Grid", 
                               list(tag("Row", 
                                        list(tag("Column", 
                                                 list(
                                                     tagList(
                                                         tags$h1("Welcome"),
                                                         tags$br(),
                                                         HTML("<Toggle labelText='Toggle' bind:toggled/>")
                                                     )
                                                 )))))))))) |> 
        htmltools::renderTags()
    
    write(app$html, "src/App.svelte")
    
    
}