Use this reusable snippet to add telephone + whatsapp sticky icons in the bottom-right corner of the display. All you need is to include the following code in your css and javascript, changing the parameters in the call to the `initStickyContact(phone, iconWidth, iconHeight)` method as needed.

```css
.icon-container {
  border-radius: 25px;
  background: green;
  overflow: auto;
  position: -webkit-sticky;
  position: sticky;
  bottom: 10px;
  float: right;
  margin: 10px;
}
.icon-container path {
  fill: white;
}
.wa-icon, .tel-icon {
  padding: 10px;
}
```

```javascript
document.addEventListener('DOMContentLoaded', initStickyContact('+1234567890', 64, 64));
function initStickyContact(phone, iconWidth, iconHeight) {
  let iconContainer = document.createElement('div');
  iconContainer.classList.add('icon-container');
  iconContainer.appendChild(
      linkFor(
	    icon(
	          {
                 'width': iconWidth,
                 'height': iconHeight,
	  		     'version': '1.1',
                 'x': '0px',
                 'y': '0px',
                 'style': 'enable-background:new 0 0 122.88 122.27',
                 'xml:space': 'preserve',
                 'viewBox': '0 0 122.88 122.27'
	  		 },
	  		 'M33.84,50.25c4.13,7.45,8.89,14.6,15.07,21.12c6.2,6.56,13.91,12.53,23.89,17.63c0.74,0.36,1.44,0.36,2.07,0.11 c0.95-0.36,1.92-1.15,2.87-2.1c0.74-0.74,1.66-1.92,2.62-3.21c3.84-5.05,8.59-11.32,15.3-8.18c0.15,0.07,0.26,0.15,0.41,0.21 l22.38,12.87c0.07,0.04,0.15,0.11,0.21,0.15c2.95,2.03,4.17,5.16,4.2,8.71c0,3.61-1.33,7.67-3.28,11.1 c-2.58,4.53-6.38,7.53-10.76,9.51c-4.17,1.92-8.81,2.95-13.27,3.61c-7,1.03-13.56,0.37-20.27-1.69 c-6.56-2.03-13.17-5.38-20.39-9.84l-0.53-0.34c-3.31-2.07-6.89-4.28-10.4-6.89C31.12,93.32,18.03,79.31,9.5,63.89 C2.35,50.95-1.55,36.98,0.58,23.67c1.18-7.3,4.31-13.94,9.77-18.32c4.76-3.84,11.17-5.94,19.47-5.2c0.95,0.07,1.8,0.62,2.25,1.44 l14.35,24.26c2.1,2.72,2.36,5.42,1.21,8.12c-0.95,2.21-2.87,4.25-5.49,6.15c-0.77,0.66-1.69,1.33-2.66,2.03 c-3.21,2.33-6.86,5.02-5.61,8.18L33.84,50.25L33.84,50.25L33.84,50.25z',
			 'tel-icon'
	    
	    ), 
	    'tel:' + phone, 
		'tel'));
    iconContainer.appendChild(
      linkFor(
	    icon(
	          {  
                'width': iconWidth,
                'height': iconHeight,
                'shape-rendering': 'geometricPrecision',
                'text-rendering': 'geometricPrecision',
                'image-rendering': 'optimizePrecision',
                'fill-rule': 'evenodd',
                'clip-rule': 'evenodd',
                'viewBox': '0 0 640 640'
              },
              'M546.704 91.89C486.526 31.584 406.482-1.582 321.229-1.582 145.609-1.583 2.67 141.368 2.67 317.118c0 56.139 14.705 111.05 42.567 159.297L.001 641.595l168.959-44.34c46.595 25.382 99.013 38.835 152.222 38.835h.13C496.944 636.09 640 493.14 640 317.401c0-85.182-33.166-165.179-93.344-225.463l.047-.047zM321.323 582.315c-47.599 0-94.218-12.827-134.895-36.957l-9.697-5.788-100.265 26.257 26.776-97.726-6.272-10.04C70.312 415.965 56.4 367.244 56.4 317.13c0-146.082 118.832-264.96 265.066-264.96 70.713 0 137.328 27.65 187.302 77.622 49.996 50.127 77.493 116.588 77.493 187.42-.118 146.187-118.95 265.066-264.96 265.066l.024.036zM466.541 383.85c-7.913-4.028-47.115-23.233-54.39-25.89-7.276-2.658-12.58-4.028-17.977 4.027-5.268 7.914-20.587 25.89-25.252 31.265-4.666 5.28-9.284 6.035-17.197 2.008-7.914-4.028-33.674-12.426-64.064-39.568-23.634-21.095-39.662-47.221-44.328-55.134-4.665-7.914-.52-12.308 3.532-16.193 3.661-3.544 7.925-9.284 11.941-13.95 4.028-4.665 5.28-7.925 7.925-13.31 2.658-5.28 1.359-9.946-.637-13.95-2.008-4.015-17.977-43.217-24.485-59.185-6.39-15.603-13.063-13.43-17.965-13.701-4.665-.237-9.945-.237-15.2-.237-5.257 0-13.95 1.996-21.225 9.933-7.276 7.914-27.898 27.26-27.898 66.45 0 39.201 28.512 77.009 32.516 82.407 4.027 5.267 56.162 85.784 136.029 120.238 18.98 8.161 33.803 13.063 45.355 16.854 19.098 6.024 36.425 5.15 50.126 3.13 15.32-2.256 47.115-19.229 53.788-37.831 6.662-18.615 6.662-34.536 4.666-37.831-1.89-3.544-7.158-5.504-15.201-9.58l-.06.048z',
			  'wa-icon'
	    ), 
	    'https://api.whatsapp.com/send?phone=' + phone,
		'wa'));
  document.querySelector('body').appendChild(iconContainer);
}

function linkFor(node, url, clazz) {
  let link = document.createElement('a');
  link.appendChild(node);
  link.classList.add(clazz);
  link.href = url;
  return link;
}

function icon(attributes, svgPath, clazz) {
  let container = document.createElement('span');
  let svg = document.createElementNS('http://www.w3.org/2000/svg', 'svg');
  let path = document.createElementNS('http://www.w3.org/2000/svg', 'path');
  Object.entries(attributes).forEach(kv => svg.setAttribute(kv[0], kv[1]));
  path.setAttribute('d', svgPath);
  svg.appendChild(path);
  svg.classList.add(clazz);
  container.appendChild(svg);
  return container;
}
```