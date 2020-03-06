<script>
import { LMap, LTileLayer } from 'vue2-leaflet'
import 'leaflet/dist/leaflet.css'
export default {
  props: {},
  mounted() {
  },
  data() {
    return {
      url: 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
      zoom: 17,
      center: [24.165348479759157, 120.6325650215149],
      bounds: null
    }
  },
  methods: {
    zoomUpdated (zoom) {
      this.zoom = zoom;
    },
    centerUpdated (center) {
      this.center = center;
    }
  },
  render(){
    return (
        <div style="height: 100%; width: 100%;">
          <LMap
            style="height: 80%"
            zoom={this.zoom}
            center={this.center}
          >
            <LTileLayer url={this.url}></LTileLayer>
          </LMap>
        </div>

    )
  }
}
</script>

<style lang="scss" scoped>
</style>
