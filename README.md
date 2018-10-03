Single file vue component media player.  
Essentially just a front end to HTMLMediaElement.
You can bind an array of media files (name/src pair objects) and they will be listed as available
files to play when rendered. Demo at https://www.michaelcuccaro.com/

![alt text](https://github.com/mvcuccaro/vueamp/blob/master/vueampscreenshot.png)


Import the vueamp component into your vue app component and provide some audio source objects 
```javascript

import AudioPlayer from './vueamp.vue';

export default {
  components: {
    'audio-player': AudioPlayer  
  }
},

data () {
    	return {
    	  audio_sources: [{
    			src:'http://thirdpartyinterface.com/mp3/3pi.call_of_shinebox.2014-4-25.mp3',
    			name:'Call of Shinebox'
    		},{
    			src:'http://thirdpartyinterface.com/mp3/3pi.the_periss_correlation.2014-4-25.2.mp3',
    			name: 'The Periss Correlation'
    		}]
    	}
}
```

put the audio-player element in your html and bind the array of audio sources
```html
<audio-player :audio-sources="audio_sources"></audio-player>
```
