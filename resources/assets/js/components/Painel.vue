<template>
    <div v-bind:class="defineCor">
        <div class="panel-heading">{{titulo}}</div>

        <div class="panel-body">
            <slot></slot>
        </div>
    </div>
</template>

<script>
    export default {
        props:['titulo','cor'],
        computed:{
        	defineCor: function(){
        		return "panel "+(this.cor || "panel-default");
        	}
        }
    }
</script>

<style>
	.blue {
	    border-color: #0d4a96;
	}
	.blue > .panel-heading {
	    color: #ffffff;
	    background-color: #0d4a96;
	    border-color: #0d4a96;
	}
	.orange {
	    border-color: #e85e0d;
	}
	.orange > .panel-heading {
	    color: #ffffff;
	    background-color: #e85e0d;
	    border-color: #e85e0d;
	}
	.small-box>.small-box-footer {
	    position: relative;
	    text-align: center;
	    padding: 3px 0;
	    color: #fff;
	    color: rgba(255,255,255,0.8);
	    display: block;
	    z-index: 10;
	    background: rgba(0,0,0,0.1);
	    text-decoration: none;
	}
	a {
	    color: #3c8dbc;
	}
</style>
