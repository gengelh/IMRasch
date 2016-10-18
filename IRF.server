shinyServer(function(input, output) {
  output$IRF <- renderPlot({
    a=input$a
    b=input$b
    c=input$c
    theta<-seq(-4,4,by=.1)
    p<-c+(1-c)*(1/(1+exp(-a*(theta-b))))
    plot(theta,p,ylim=c(0,1),main="Item Response Function",type="l",xlab=expression(paste("Person Location ",theta)),ylab="Probability of Correct Responses")
  })
  
  output$IIF <- renderPlot({
    a=input$a
    b=input$b
    c=input$c
    theta<-seq(-4,4,by=.1)
    p<-c+(1-c)*(1/(1+exp(-a*(theta-b))))
    In=a^2*p*(1-p)
    plot(theta,In,main="Item Information Function",type="l",xlab=expression(paste("Person Location ",theta)),ylab="Information (Precision)")
  })
})

