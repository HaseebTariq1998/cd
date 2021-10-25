    Canvas {
        id: mycanvas
        property string color: "red"
        anchors.fill:parent
        onPaint: {
            var ctx = getContext("2d");
            var x=185
            var y=189
            ctx.setLineDash([2, 1]);
            ctx.lineJoin = "round";
            ctx.beginPath();
            ctx.lineWidth = 3;
            ctx.strokeStyle = mycanvas.color; // Green path
            ctx.moveTo(x, y);
            ctx.lineTo(x, y+60);
            ctx.lineTo(x+84, y+60);

            //ctx.lineTo(x+200, y+200);
            ctx.stroke();


            x=276
            y=360
            ctx.moveTo(x, y);
            ctx.lineTo(x+60, y);
            ctx.lineTo(x+60, y-76);
            ctx.moveTo(x+60, y);
            ctx.lineTo(x+60+60, y);

            //ctx.lineTo(x+200, y+200);
            ctx.stroke();


            x=400
            y=249
            ctx.moveTo(x, y);
            ctx.lineTo(x+100, y);
            ctx.lineTo(x+100, y-76);
            ctx.moveTo(x+100, y);
            ctx.lineTo(x+100+100, y);

            //ctx.lineTo(x+200, y+200);
            ctx.stroke();
        }
    }
