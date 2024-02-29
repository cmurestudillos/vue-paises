<template>
    <footer class="py-5">
        <div class="container px-4 px-lg-5">
            <p class="m-0 text-center text-white">
                Copyright © - Designed and Created by: <em><strong>Carlos Mur</strong></em>
            </p>
            <p class="m-0 text-center text-white">
                <small><em>Version: {{version}}</em></small>            
            </p>
        </div>
    </footer>
</template>

<script>
import packageInfo  from '../../package.json';

export default {
    name: 'Footer',
    data() {
        return {
            version: packageInfo.version
        }
    }
}
</script>