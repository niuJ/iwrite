<template>
    <div class="carousel">
        <transition-group tag='ul' class="clearfix slide" name='image'>
            <li v-for='(image,index) in img' :key='index' v-show='index===mark'>
                <a><img :src="image"></a>
            </li>
        </transition-group>
        <div class="bullet">
            <span v-for='(item,index) in img.length' :class="{'active':index===mark}" @click='change(index)'></span>
        </div>
    </div>
</template>

<script>
     export default {
       el: '.carousel',
       data: {
         mark: 0,
         timer: null,
         img: ['http://upload-images.jianshu.io/upload_images/3360875-5625658440cb542d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240',
           'http://upload-images.jianshu.io/upload_images/3360875-b70e9d81d26e2a27.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240',
           'http://upload-images.jianshu.io/upload_images/3360875-dc724649454c2ddc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240',
           'http://upload-images.jianshu.io/upload_images/3360875-d2148a1bb7ea9d21.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240'
         ]
  },
  created () {
         this.play()
  },
  methods: {
         change (i) {
           this.mark = i
         },
         autoPlay () {
           this.mark++
           if (this.mark === 4) {
             this.mark = 0
             return
           }
         },
         play () {
           setInterval(this.autoPlay, 3000)
         }
  }
}
// http://www.jianshu.com/p/56fb1513a28a
</script>

