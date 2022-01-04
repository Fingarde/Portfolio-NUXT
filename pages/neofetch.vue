<template>
    <div id="loading">
        <div>
            <span class="text green">root@fingarde.fr</span>
            <span class="text white">:</span>
            <span class="text blue">~</span>
            <span class="text white">#</span>
            <span class="text">&nbsp;</span>
            <span class="text white">./neofetch</span>
        </div>


        <div class="flex" id="neofetch">
            <pre class="text lime">{{ logo }}</pre>
            <div class="text green column">
                <div class="clear"></div>
                <div>
                    <span class="text green">root</span>
                    <span class="text white">@</span>
                    <span class="text green">fingarde.fr</span>
                </div>
                <div>
                    <span class="text white">----------------</span>
                </div>
                <div>
                    <span class="text green">OS</span>
                    <span class="text white">:&nbsp;</span>
                    <span class="text white">Nuxt 2.15.8</span>
                </div>
                 <div>
                    <span class="text green">Host</span>
                    <span class="text white">:&nbsp;</span>
                    <span class="text white">81LK IdeaPad L340-15IRH Gaming </span>
                </div>
                 <div>
                    <span class="text green">Kernel</span>
                    <span class="text white">:&nbsp;</span>
                    <span class="text white">5.13.0-22-generic</span>
                </div>
                <div>
                    <span class="text green">Uptime</span>
                    <span class="text white">:&nbsp;</span>
                    <span class="text white">8 hours, 56 mins</span>
                </div>
                <div>
                    <span class="text green">Packages</span>
                    <span class="text white">:&nbsp;</span>
                    <span class="text white">2184 (dpkg) </span>
                </div>
                <div>
                    <span class="text green">Shell</span>
                    <span class="text white">:&nbsp;</span>
                    <span class="text white">bash 5.1.8</span>
                </div>
                <div>
                    <span class="text green">Resolution</span>
                    <span class="text white">:&nbsp;</span>
                    <span class="text white">1920x1080</span>
                </div>
                <div>
                    <span class="text green">DE</span>
                    <span class="text white">:&nbsp;</span>
                    <span class="text white">Plasma 5.22.5</span>
                </div>
                 <div>
                    <span class="text green">WM</span>
                    <span class="text white">:&nbsp;</span>
                    <span class="text white">KWin</span>
                </div>
            </div>
        </div>


        <div>
            <span class="text green">root@fingarde.fr</span>
            <span class="text white">:</span>
            <span class="text blue">~</span>
            <span class="text white">#</span>
            <span class="text">&nbsp;</span>
            <span class="text white">cd portfolio</span>
        </div>


        <div>
            <span class="text green">root@fingarde.fr</span>
            <span class="text white">:</span>
            <span class="text blue">~/portfolio</span>
            <span class="text white">#</span>
            <span class="text">&nbsp;</span>
            <span class="text white">yarn serve</span>
            <span class="text flash" style="line-height: 10px">{{ cursor[index] }}</span>
        </div>
        
    </div>
</template>

<script>
export default {
    data() {
        return {
            index: 0,
            cursor: [ '█', ' ' ],
            logo: 
`********########         #######********
  ********#######       #######******** 
   ********########   ########********  
     ********####### #######********    
      ********#############********     
        ********#########********       
         ********#######********        
          ********####********          
            ********#********           
             ***************            
               ***********              
                *********               
                  *****                 
                   ***`                  
        }
    },
    mounted() {
        setInterval(() => {
            this.$data.index = (this.$data.index + 1) % 2
            
        }, 500)
    }
}
</script>


<style>
@import url('https://fonts.googleapis.com/css2?family=Ubuntu+Mono&display=swap');



#loading {
  background-color: black;

  width: 100vw;
  height: 100vh;
}

.clear {
    clear: both;
}

.column > * {
    display: flex;
}

#neofetch .column:not(:first-child) {
    padding-left: 100px;
}

.text {
    font-family: 'Ubuntu Mono', monospace;
    font-weight: bold;
    font-size: 20px;
}

.lime {
    color: #55CC80
}

.green {
    color: #1CDC9A;
}

.white {
    color: #FCFCFC;
}

.blue {
    color: #1D99F3;
}

.flex {
    display: flex;
    flex-direction: row;
}

.flash {
    color: #FCFCFC
}
</style>