---
title: "RGeo — Support for geo and databases in Ruby and Rails"
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
---

Support for geo and databases in Ruby and Rails

```ruby
require "open-uri"
require "json"
require "rgeo"
require "rgeo-geojson"

my_lat, my_lng = [45, 5]
my_position = RGeo::Cartesian.
              factory.
              point(my_lng, my_lat)

geojson = URI.
    	  open("https://git.io/rhone-alpes.geojson").
    	  read
rhone_alpes = RGeo::GeoJSON.decode(geojson).geometry

if rhone_alpes.contains?(my_position)
  puts "Let's ski ⛷"
end
```

## Resources

- [Documentation](https://rubydoc.info/gems/rgeo)
- [Sources](https://github.com/rgeo/rgeo)
- [activerecord-postgis-adapter](https://github.com/rgeo/activerecord-postgis-adapter)
- [RGeo::GeoJSON](https://github.com/rgeo/rgeo-geojson)
- And many more on [our organisation page](https://github.com/rgeo)

## Sponsors

<a>
	<img alt="Goldfish Ads" src="images/goldfish-ads.png">
</a>
<a href="https://github.com/klaxit">
	<img alt="Klaxit" src="images/klaxit.svg" />
</a>


## Credits

Thanks to @dazuma, author of RGeo. And to every contributors of the various
projects.
