# sky19890315.github.io
https://sky19890315.github.io/
 var dateOne = [];//init
            function getDatasbyDay() {
                $.ajax({
                    type: "POST",
                    async: false,
                    url: "pindex_home.shtml",
                    data: {
                        "day":1,
                        "getNew":1,
                    },
                    dataType: "json",
                    success: function (result) {
                        if(result){
                            for(var i=0; i < result.length; i++) {
                                var years = result[i].years;
                                var dates = result[i].dates;
                                dateOne.push([years,dates]);
                            }
                        }
                    }
                });
            }
