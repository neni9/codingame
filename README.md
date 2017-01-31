# codingame
codingame


jAVASCRIPT
++++++++++++++

// declaration variable
var N = parseInt(readline());
var Q = parseInt(readline());

var mimeTypeTable = {};

for (var i = 0; i < N; i++) {
	var inputs = readline().split(' ');
	mimeTypeTable[inputs[0].toLowerCase()] = inputs[1];
}

for (var i = 0; i < Q; i++) {
	var ext = readline().toLowerCase().split('.');
	
	if (ext.length > 1 && mimeTypeTable[ext[ext.length - 1]]) {
		print(mimeTypeTable[ext[ext.length - 1]]);
	} else {
		print('UNKNOWN');
	}
}
