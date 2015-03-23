# Nightcharts

This class includes a drawing histogram, pies and pseudo 3D pies.  
It has very simple API and high level usability.  

Licensed under LGPL 2.1

Example :


    void MainWindow::paintEvent(QPaintEvent e*)
    {
        QWidget::paintEvent(e);
        QPainter painter;
        QFont font;
        painter.begin(this);
        Nightcharts PieChart;
        PieChart.setType(Nightcharts::DPie);//{Histogramm,Pie,DPie};
        PieChart.setLegendType(Nightcharts::Round);//{Round,Vertical}
        PieChart.setCords(100,100,this->width()/1.5,this->height()/1.5);
        PieChart.addPiece("Item1",QColor(200,10,50),34);
        PieChart.addPiece("Item2",Qt::green,27);
        PieChart.addPiece("Item3",Qt::cyan,14);
        PieChart.addPiece("Item4",Qt::yellow,7);
        PieChart.addPiece("Item5",Qt::blue,4);
        PieChart.draw(&painter);
        PieChart.drawLegend(&painter);
    }


