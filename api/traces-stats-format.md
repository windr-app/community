
The WindR database and API use the following format.


```json
{
   "_id":"xx00xx00xx00xx",      // unique ID, generated when save in WindR database
   "version":1,                 // Schema version
   "status":"validated",        // status of the trace: new | processing | validated
   "traceDate":{                // date of the session, day and time extracted from the first GPX point
      "$date":{                 //
         "$numberLong":".."     // 
      }                         //
   },                           //
   "date":{                     // date extracted from traceDate as day - month - year (facilitator for aggregration)
      "day":2,                  //
      "month":7,                //
      "year":2022               //
   },                           //
   "file_name":"...",           // Location of the file in windr app : created during trace upload
   "type":"foil",               // activity : 'slalom', 'speed','freeride', 'foil', 'wingfoil', 'kitefoil', 'kite'
   "gps":"Garmin Fenix 5",      // GPS used
   "rider":{                    // Rider information, set automatically during upload
      "id":"xxxxxx",            //
      "displayName":"jdoe",     //
      "profile_picture":".."    //
   },                           //
   "board":{                    // Board Information, manually selected by the user during upload/configuration
      "quiver_id":null,         //
      "catalog_id":null,        //
      "brand":"Starboard",      //
      "model":"Foil Freeride",  //
      "volume":"150",           //
      "year":"2020"             //
   },                           //
   "sail":{                     // Sail Information, manually selected by the user during upload/configuration
      "quiver_id":null,         //
      "catalog_id":null,        //
      "brand":"Severne",        //
      "model":"Foilglide",      //
      "size":"7",               //
      "year":"2020"             //
   },                           //
   "fin":{                      // Fin/Foil, manually selected by the user during upload/configuration
      "quiver_id":null,         //
      "catalog_id":null,        //
      "brand":"..",             //
      "model":".",              //
      "size":".",               //
      "year":"."                //
   },                           //
   "maxSpeed":23.25,            // VMax extracted from GPX
   "maxSpeedRead":23.25         // VMAx read by the rider, if not we use the extracted one from the GPX
   "source":{                   // Information about the parser used to analyze the data
      "type":"speedResults",    //
      "version":"2.0",          //
      "creator":"",             //
      "integration":"trapeze",  //
      "computation":"po..al",   //
      "software":{              //
         "name":"GpsarPro",     //
         "version":"5.31"       //
      }                         //
   },                           //
   "location":{                 // Location, extracted from the first point of the GPX
      "latitude":47.56,         //      
      "longitude":-3.1          //
   },                           //
   "windDirection":"268",       // Wind direction: if possible calculated from the GPX data
   "totalLength":61403.51,      // Session distance calculated from GPX
   "averageSpeed":11.586,       // Average speed in knots
   "duration":10302,            // Duration in seconds
   "run_1_s_avg":22.6598,       // Top 5 1s average (knots)
   "runs_1_s":[                 // List of top 5 1s speed (knots)
      23.254,                   //
      22.921,                   //
      22.795,                   //
      22.209,                   //
      22.12                     //
   ],                           //
   "run_2_s_avg":22.5748,       // Top 5 2s average (knots)
   "runs_2_s":[                 // List of top 5 2s speed (knots)
      23.141,                   //
      22.921,                   //
      22.795,                   //
      22.07,                    //
      21.947                    //
   ],                           //
   "run_10_s_avg":22.1324,      // Top 5 10s average (knots)
   "runs_10_s":[                // List of top 5 10s speed (knots)
      22.541,                   //
      22.353,                   //
      22.16,                    //
      21.972,                   //
      21.636                    //
   ],                           //
   "run_20_s_avg":21.7818,      // Top 5 20s average (knots)
   "runs_20_s":[                // List of top 5 20s speed (knots)
      22.168,                   //
      21.949,                   //
      21.759,                   //
      21.687,                   //
      21.346                    //
   ],                           //
   "run_1800_s_avg":9.9958,     // Top 5 30mn average (knots)
   "runs_1800_s":[              // List of top 5 30mn speed (knots)
      16.675,                   //
      14.078,                   //
      12.499,                   //
      6.727,                    //
      0                         //
   ],                           //
   "run_3600_s_avg":4.2934,     // Top 5 60mn average (knots)
   "runs_3600_s":[              // List of top 5 60mn speed (knots)
      11.289,                   //
      10.178,                   //
      0,                        //
      0,                        //
      0                         //
   ],                           //
   "run_100_m_avg":22.178,      // Top 5 100m average (knots)
   "runs_100_m":[               // List of top 5 100m speed (knots)
      22.697,                   //
      22.426,                   //
      22.16,                    //
      21.972,                   //
      21.636                    //
   ],                           //
   "run_250_m_avg":21.6838,     // Top 5 250m average (knots)
   "runs_250_m":[               // List of top 5 250m speed (knots)
      22.161,                   //
      21.843,                   //
      21.605,                   //
      21.578,                   //
      21.232                    //
   ],                           //
   "run_500_m_avg":21.2134,     // Top 5 250m average (knots)
   "runs_500_m":[               // List of top 5 500m speed (knots)
      21.915,                   //
      21.489,                   //
      21.297,                   //
      20.686,                   //
      20.68                     //
   ],                           //
   "run_1852_m_avg":19.63,      // Top 5 1852m average (knots)
   "runs_1852_m":[              // List of top 5 1852m speed (knots)
      20.351,                   //
      20.049,                   //
      19.579,                   //
      19.118,                   //
      19.079                    //
   ],                           //
   "alpha_250_avg":14.9482,     // Top 5 Alpha250m average (knots)
   "alpha_250_runs":[           // List of top 5 Alpha250m speed (knots)
      16.013,                   //
      15.567,                   //
      14.593,                   //
      14.302,                   //
      14.266                    //
   ],                           //
   "alpha_500_avg":16.5542,     // Top 5 Alpha500m average (knots)
   "alpha_500_runs":[           // List of top 5 Alpha250m speed (knots)
      17.687,                   //
      16.824,                   //
      16.526,                   //
      16.324,                   //
      15.41                     //
   ],                           //
   "spot":{                     // Spot info, automatically set when selected by the user
      "id":"france_carnac_saint_colomban"
      "label":"Saint-Colomban", //
      "country":"France",       //
      "area":"Morbihan",        //
      "city":"Carnac",          //
      "location":{              //
         "type":"Point",        //
         "coordinates":[        //
            47.5693924,         //
            -3.0984503          //
         ]                      //
      },                        //
   },
}
```