# Load R packages
library(shiny)
library(shinythemes)

# Define UI
ui <- fluidPage(theme = shinytheme("cerulean"),
                navbarPage(
                  "Para Birimi Çevirici",
                  tabPanel("Döviz Çevirici",
                           sidebarPanel(
                             tags$h3("Para Birimi Çevirici"),
                             numericInput("tl_value", "Türk Lirası:", value = 0, min = 0),
                             actionButton("convert_btn", "Çevir")
                           ),
                           mainPanel(
                             h4("Sonuçlar:"),
                             verbatimTextOutput("result_text")
                           )
                  )
                )
)

# Define server function  
server <- function(input, output) {
  
  converted_values <- reactive({
    tl_amount <- input$tl_value
    
    # Döviz kurları (örnek değerler, gerçek zamanlı değil)
    usd_rate <- 0.033  # 1 TL kaç dolar
    eur_rate <- 0.026  # 1 TL kaç euro
    gbp_rate <- 0.030   # 1 TL kaç sterlin
    
    # Çevrim işlemleri
    usd_value <- tl_amount * usd_rate
    eur_value <- tl_amount * eur_rate
    gbp_value <- tl_amount * gbp_rate
    
    list(usd = usd_value, eur = eur_value, gbp = gbp_value)
  })
  
  output$result_text <- renderPrint({
    results <- converted_values()
    cat("Dolar:", round(results$usd, 2),
          "\nEuro:", round(results$eur, 2),
          "\nSterlin:", round(results$gbp, 2),
          sep = "\n")
  })
}

# Create Shiny object
shinyApp(ui = ui, server = server)
