# Shiny-R: An Interactive Web Framework for R 🎉

Created by @jl33-ai 👦🏻

Shiny is an open-source R package that provides a powerful web framework for building interactive web applications using R. With Shiny, R users can turn analyses into interactive web applications without the need for HTML, CSS, or JavaScript knowledge.

## Features ⭐

- **Interactive:** You can easily transform static R graphics into interactive displays.
- **Customizable:** Shiny user-interfaces can be as simple or as sophisticated as you want. 
- **Reproducible:** Create reports that are fully reproducible and easily shareable.
- **R-powered:** Shiny leverages the power of R's extensible graphics system to provide highly flexible and powerful graphics.

## Installation 💻

To install the Shiny R package, you can use the following command:

```r
install.packages('shiny')
```

## Basic Usage 🖥️

- Load the shiny package in your R script:

```r
library(shiny)
```

- A Shiny app usually has two main components:
     - `UI` (User Interface)
     - `Server` function

A very basic shiny application can be set up using the code below:

```r
# Define UI
ui <- fluidPage(
  titlePanel("Hello Shiny!"),
  sidebarLayout(
    sidebarPanel(
      sliderInput("obs", "Number of observations:", min = 1, max = 1000, value = 500)
    ),
    mainPanel(
      plotOutput("distPlot")
    )
  )
)

# Define server logic
server <- function(input, output) {
  output$distPlot <- renderPlot({
    hist(runif(input$obs), col = 'darkgray', border = 'white')
  })
}

# Run the application
shinyApp(ui = ui, server = server)
```

## Widget Types 🚀

Shiny provides several widgets for user inputs:

- **ActionButton:** For defining action buttons.
- **CheckboxGroupInput:** Supports multiple selections.
- **CheckboxInput:** To be used for binary options.
- **DatePickerInput:** For selecting dates.
- **FileInput:** Allows user to upload files.
- **NumericInput:** Allows users to enter a number.
- **RadioButtons:** Allows single selection out of multiple options.
- **SelectInput:** Allows single selection out of multiple options in a dropdown.

## Resources to Learn 📚

- [Shiny Official Tutorial](https://shiny.rstudio.com/tutorial/)
- [Shiny Gallery](https://shiny.rstudio.com/gallery/)
- [Mastering Shiny](https://mastering-shiny.org/)

## Contributing 🤝

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License 📄

[MIT](https://choosealicense.com/licenses/mit/)