
const moment = require('moment'); 
function getDate(){
  console.log
  only needing core
define(['moment'], function (moment) {
    console.log(moment().format('LLLL'));  
});

define(['moment', 'moment/locale/de'], function (moment) {
    moment.locale('de');
    console.log(moment().format('LLLL')); 
});

define(['moment/min/moment-with-locales'], function (moment) {
    moment.locale('de');
    console.log(moment().format('LLLL')); 
});


define(['require', 'moment'], function(require, moment) {
  require(['moment/locale/de'], function(localeModule) {

    console.log(moment().format('LLLL'));  

    moment.locale('de');
    
    console.log(moment().format('LLLL')); 
  })
});
}
require.config({
    config: {
        moment: {
            noGlobal: true
        }
    }
});
