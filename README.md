# chord-diagram
This package provides a basic Typescript class for drawing chord diagrams on HTML DOM canvasses within given parent elements.
It may be used in conjunction with @authentrics/ngx-chord-diagram for Angular applications.

This is the first npm package I have created, so patience and constructive suggestions are very welcome.

The basic usage is shown in the demo index.html file:

```<div id="chordArea"></div>
<script>const exports = {"__esModule": true};</script>
<script src="../dist/ChordDiagram.js"></script>
<script>
	const parentEl = document.getElementById('chordArea');
	const chords = [
		{parentElement:parentEl, name: 'C', positions: [1,2,3,0,0,1]},
		{parentElement:parentEl, name: 'D', positions: [0,1,3,0,0,1], color: 'navy', dotColor: '#AAA'},
		{parentElement:parentEl, name: 'D', positions: [0,1,3,0,0,1], dotColor: 'orange'},
	];
	const diagrammer = new ChordDiagram();
	for (const chord of chords) {
		diagrammer.draw(chord);
	}
</script>
```
