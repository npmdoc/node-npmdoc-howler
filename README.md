# api documentation for  [howler (v2.0.3)](https://howlerjs.com)  [![npm package](https://img.shields.io/npm/v/npmdoc-howler.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-howler) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-howler.svg)](https://travis-ci.org/npmdoc/node-npmdoc-howler)
#### Javascript audio library for the modern web.

[![NPM](https://nodei.co/npm/howler.png?downloads=true)](https://www.npmjs.com/package/howler)

[![apidoc](https://npmdoc.github.io/node-npmdoc-howler/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-howler_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-howler/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-howler/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-howler/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "James Simpson",
        "email": "james@goldfirestudios.com",
        "url": "http://goldfirestudios.com"
    },
    "bugs": {
        "url": "https://github.com/goldfire/howler.js/issues"
    },
    "dependencies": {},
    "description": "Javascript audio library for the modern web.",
    "devDependencies": {
        "uglify-js": "2.x"
    },
    "directories": {},
    "dist": {
        "shasum": "a76ab5a37ae5cc1e4a5a0f3ce279ca2c72b5efc7",
        "tarball": "https://registry.npmjs.org/howler/-/howler-2.0.3.tgz"
    },
    "files": [
        "src",
        "dist/howler.js",
        "dist/howler.min.js",
        "dist/howler.core.min.js",
        "dist/howler.spatial.min.js",
        "LICENSE.md"
    ],
    "gitHead": "4ebd1897b6c425befde7970c583999db663d2093",
    "homepage": "https://howlerjs.com",
    "keywords": [
        "howler",
        "howler.js",
        "audio",
        "sound",
        "web audio",
        "webaudio",
        "browser",
        "html5",
        "html5 audio",
        "audio sprite",
        "audiosprite"
    ],
    "license": {
        "type": "MIT",
        "url": "https://raw.githubusercontent.com/goldfire/howler.js/master/LICENSE.md"
    },
    "main": "dist/howler.js",
    "maintainers": [
        {
            "name": "goldfire",
            "email": "james@goldfirestudios.com"
        }
    ],
    "name": "howler",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/goldfire/howler.js.git"
    },
    "scripts": {
        "build": "VERSION='printf 'v' && node -e 'console.log(require(\"./package.json\").version)'' && sed -i '' '2s/.*/ *  howler.js '\"$VERSION\"'/' src/howler.core.js && sed -i '' '4s/.*/ *  howler.js '\"$VERSION\"'/' src/plugins/howler.spatial.js && uglifyjs --preamble \"/*! howler.js $VERSION | (c) 2013-2017, James Simpson of GoldFire Studios | MIT License | howlerjs.com */\" src/howler.core.js -c -m --screw-ie8 -o dist/howler.core.min.js && uglifyjs --preamble \"/*! howler.js $VERSION | Spatial Plugin | (c) 2013-2017, James Simpson of GoldFire Studios | MIT License | howlerjs.com */\" src/plugins/howler.spatial.js -c -m --screw-ie8 -o dist/howler.spatial.min.js && awk 'FNR==1{echo \"\"}1' dist/howler.core.min.js dist/howler.spatial.min.js | sed '3s~.*~/*! Spatial Plugin */~' | perl -pe 'chomp if eof' > dist/howler.min.js && awk '(NR>1 && FNR==1){printf (\"\\n\\n\")};1' src/howler.core.js src/plugins/howler.spatial.js > dist/howler.js",
        "release": "VERSION='printf 'v' && node -e 'console.log(require(\"./package.json\").version)'' && git tag $VERSION && git push && git push origin $VERSION && npm publish"
    },
    "version": "2.0.3"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module howler](#apidoc.module.howler)
1.  [function <span class="apidocSignatureSpan">howler.</span>Howl (o)](#apidoc.element.howler.Howl)
1.  object <span class="apidocSignatureSpan">howler.</span>Howl.prototype
1.  object <span class="apidocSignatureSpan">howler.</span>Howler
1.  object <span class="apidocSignatureSpan">howler.</span>howler_core

#### [module howler.Howl](#apidoc.module.howler.Howl)
1.  [function <span class="apidocSignatureSpan">howler.</span>Howl (o)](#apidoc.element.howler.Howl.Howl)

#### [module howler.Howl.prototype](#apidoc.module.howler.Howl.prototype)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_cleanBuffer (node)](#apidoc.element.howler.Howl.prototype._cleanBuffer)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_clearTimer (id)](#apidoc.element.howler.Howl.prototype._clearTimer)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_drain ()](#apidoc.element.howler.Howl.prototype._drain)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_emit (event, id, msg)](#apidoc.element.howler.Howl.prototype._emit)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_ended (sound)](#apidoc.element.howler.Howl.prototype._ended)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_getSoundIds (id)](#apidoc.element.howler.Howl.prototype._getSoundIds)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_inactiveSound ()](#apidoc.element.howler.Howl.prototype._inactiveSound)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_loadQueue ()](#apidoc.element.howler.Howl.prototype._loadQueue)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_refreshBuffer (sound)](#apidoc.element.howler.Howl.prototype._refreshBuffer)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_soundById (id)](#apidoc.element.howler.Howl.prototype._soundById)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_stopFade (id)](#apidoc.element.howler.Howl.prototype._stopFade)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>duration (id)](#apidoc.element.howler.Howl.prototype.duration)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>fade (from, to, len, id)](#apidoc.element.howler.Howl.prototype.fade)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>init (o)](#apidoc.element.howler.Howl.prototype.init)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>load ()](#apidoc.element.howler.Howl.prototype.load)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>loop ()](#apidoc.element.howler.Howl.prototype.loop)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>mute (muted, id)](#apidoc.element.howler.Howl.prototype.mute)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>off (event, fn, id)](#apidoc.element.howler.Howl.prototype.off)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>on (event, fn, id, once)](#apidoc.element.howler.Howl.prototype.on)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>once (event, fn, id)](#apidoc.element.howler.Howl.prototype.once)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>orientation (x, y, z, id)](#apidoc.element.howler.Howl.prototype.orientation)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>pannerAttr ()](#apidoc.element.howler.Howl.prototype.pannerAttr)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>pause (id)](#apidoc.element.howler.Howl.prototype.pause)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>play (sprite, internal)](#apidoc.element.howler.Howl.prototype.play)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>playing (id)](#apidoc.element.howler.Howl.prototype.playing)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>pos (x, y, z, id)](#apidoc.element.howler.Howl.prototype.pos)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>rate ()](#apidoc.element.howler.Howl.prototype.rate)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>seek ()](#apidoc.element.howler.Howl.prototype.seek)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>state ()](#apidoc.element.howler.Howl.prototype.state)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>stereo (pan, id)](#apidoc.element.howler.Howl.prototype.stereo)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>stop (id, internal)](#apidoc.element.howler.Howl.prototype.stop)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>unload ()](#apidoc.element.howler.Howl.prototype.unload)
1.  [function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>volume ()](#apidoc.element.howler.Howl.prototype.volume)

#### [module howler.howler_core](#apidoc.module.howler.howler_core)
1.  [function <span class="apidocSignatureSpan">howler.howler_core.</span>Howl (o)](#apidoc.element.howler.howler_core.Howl)
1.  object <span class="apidocSignatureSpan">howler.howler_core.</span>Howler



# <a name="apidoc.module.howler"></a>[module howler](#apidoc.module.howler)

#### <a name="apidoc.element.howler.Howl"></a>[function <span class="apidocSignatureSpan">howler.</span>Howl (o)](#apidoc.element.howler.Howl)
- description and source-code
```javascript
Howl = function (o) {
  var self = this;

  // Throw an error if no source is provided.
  if (!o.src || o.src.length === 0) {
    console.error('An array of source files must be passed with any new Howl.');
    return;
  }

  self.init(o);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.howler.Howl"></a>[module howler.Howl](#apidoc.module.howler.Howl)

#### <a name="apidoc.element.howler.Howl.Howl"></a>[function <span class="apidocSignatureSpan">howler.</span>Howl (o)](#apidoc.element.howler.Howl.Howl)
- description and source-code
```javascript
Howl = function (o) {
  var self = this;

  // Throw an error if no source is provided.
  if (!o.src || o.src.length === 0) {
    console.error('An array of source files must be passed with any new Howl.');
    return;
  }

  self.init(o);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.howler.Howl.prototype"></a>[module howler.Howl.prototype](#apidoc.module.howler.Howl.prototype)

#### <a name="apidoc.element.howler.Howl.prototype._cleanBuffer"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_cleanBuffer (node)](#apidoc.element.howler.Howl.prototype._cleanBuffer)
- description and source-code
```javascript
_cleanBuffer = function (node) {
  var self = this;

  if (self._scratchBuffer) {
    node.bufferSource.onended = null;
    node.bufferSource.disconnect(0);
    try { node.bufferSource.buffer = self._scratchBuffer; } catch(e) {}
  }
  node.bufferSource = null;

  return self;
}
```
- example usage
```shell
...
      if (typeof sound._node.bufferSource.stop === 'undefined') {
        sound._node.bufferSource.noteOff(0);
      } else {
        sound._node.bufferSource.stop(0);
      }

      // Clean up the buffer source.
      self._cleanBuffer(sound._node);
    } else if (!isNaN(sound._node.duration) || sound._node.duration === Infinity) {
      sound._node.pause();
    }
  }
}

// Fire the pause event, unless 'true' is passed as the 2nd argument.
...
```

#### <a name="apidoc.element.howler.Howl.prototype._clearTimer"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_clearTimer (id)](#apidoc.element.howler.Howl.prototype._clearTimer)
- description and source-code
```javascript
_clearTimer = function (id) {
  var self = this;

  if (self._endTimers[id]) {
    clearTimeout(self._endTimers[id]);
    delete self._endTimers[id];
  }

  return self;
}
```
- example usage
```shell
...
    playWebAudio();
  } else {
    // Wait for the audio to load and then begin playback.
    var event = !isRunning && self._state === 'loaded' ? 'resume' : 'load';
    self.once(event, playWebAudio, isRunning ? sound._id : null);

    // Cancel the end timer.
    self._clearTimer(sound._id);
  }
} else {
  // Fire this when the sound is ready to play to begin HTML5 Audio playback.
  var playHtml5 = function() {
    node.currentTime = seek;
    node.muted = sound._muted || self._muted || Howler._muted || node.muted;
    node.volume = sound._volume * Howler.volume();
...
```

#### <a name="apidoc.element.howler.Howl.prototype._drain"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_drain ()](#apidoc.element.howler.Howl.prototype._drain)
- description and source-code
```javascript
_drain = function () {
  var self = this;
  var limit = self._pool;
  var cnt = 0;
  var i = 0;

  // If there are less sounds than the max pool size, we are done.
  if (self._sounds.length < limit) {
    return;
  }

  // Count the number of inactive sounds.
  for (i=0; i<self._sounds.length; i++) {
    if (self._sounds[i]._ended) {
      cnt++;
    }
  }

  // Remove excess inactive sounds, going in reverse order.
  for (i=self._sounds.length - 1; i>=0; i--) {
    if (cnt <= limit) {
      return;
    }

    if (self._sounds[i]._ended) {
      // Disconnect the audio source when using Web Audio.
      if (self._webAudio && self._sounds[i]._node) {
        self._sounds[i]._node.disconnect(0);
      }

      // Remove sounds until we have the pool size.
      self._sounds.splice(i, 1);
      cnt--;
    }
  }
}
```
- example usage
```shell
...
    /**
     * Return an inactive sound from the pool or create a new one.
     * @return {Sound} Sound playback object.
     */
    _inactiveSound: function() {
var self = this;

self._drain();

// Find the first inactive node to recycle.
for (var i=0; i<self._sounds.length; i++) {
  if (self._sounds[i]._ended) {
    return self._sounds[i].reset();
  }
}
...
```

#### <a name="apidoc.element.howler.Howl.prototype._emit"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_emit (event, id, msg)](#apidoc.element.howler.Howl.prototype._emit)
- description and source-code
```javascript
_emit = function (event, id, msg) {
  var self = this;
  var events = self['_on' + event];

  // Loop through event store and fire all functions.
  for (var i=events.length-1; i>=0; i--) {
    if (!events[i].id || events[i].id === id || event === 'load') {
      setTimeout(function(fn) {
        fn.call(this, id, msg);
      }.bind(self, events[i].fn), 0);

      // If this event was setup with 'once', remove it.
      if (events[i].once) {
        self.off(event, events[i].fn, events[i].id);
      }
    }
  }

  return self;
}
```
- example usage
```shell
...
      } else if (self.state === 'suspended') {
self.state = 'resuming';
self.ctx.resume().then(function() {
  self.state = 'running';

  // Emit to all Howls that the audio has resumed.
  for (var i=0; i<self._howls.length; i++) {
    self._howls[i]._emit('resume');
  }
});

if (self._suspendTimer) {
  clearTimeout(self._suspendTimer);
  self._suspendTimer = null;
}
...
```

#### <a name="apidoc.element.howler.Howl.prototype._ended"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_ended (sound)](#apidoc.element.howler.Howl.prototype._ended)
- description and source-code
```javascript
_ended = function (sound) {
  var self = this;
  var sprite = sound._sprite;

  // Should this sound loop?
  var loop = !!(sound._loop || self._sprite[sprite][2]);

  // Fire the ended event.
  self._emit('end', sound._id);

  // Restart the playback for HTML5 Audio loop.
  if (!self._webAudio && loop) {
    self.stop(sound._id, true).play(sound._id);
  }

  // Restart this timer if on a Web Audio loop.
  if (self._webAudio && loop) {
    self._emit('play', sound._id);
    sound._seek = sound._start || 0;
    sound._rateSeek = 0;
    sound._playStart = Howler.ctx.currentTime;

    var timeout = ((sound._stop - sound._start) * 1000) / Math.abs(sound._rate);
    self._endTimers[sound._id] = setTimeout(self._ended.bind(self, sound), timeout);
  }

  // Mark the node as paused.
  if (self._webAudio && !loop) {
    sound._paused = true;
    sound._ended = true;
    sound._seek = sound._start || 0;
    sound._rateSeek = 0;
    self._clearTimer(sound._id);

    // Clean up the buffer source.
    self._cleanBuffer(sound._node);

    // Attempt to auto-suspend AudioContext if no sounds are still playing.
    Howler._autoSuspend();
  }

  // When using a sprite, end the track.
  if (!self._webAudio && !loop) {
    self.stop(sound._id);
  }

  return self;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.howler.Howl.prototype._getSoundIds"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_getSoundIds (id)](#apidoc.element.howler.Howl.prototype._getSoundIds)
- description and source-code
```javascript
_getSoundIds = function (id) {
  var self = this;

  if (typeof id === 'undefined') {
    var ids = [];
    for (var i=0; i<self._sounds.length; i++) {
      ids.push(self._sounds[i]._id);
    }

    return ids;
  } else {
    return [id];
  }
}
```
- example usage
```shell
...
          self.masterGain.gain.value = vol;
        }

        // Loop through and change volume for all HTML5 audio nodes.
        for (var i=0; i<self._howls.length; i++) {
          if (!self._howls[i]._webAudio) {
            // Get all of the sounds in this Howl group.
            var ids = self._howls[i]._getSoundIds();

            // Loop through all sounds and change the volumes.
            for (var j=0; j<ids.length; j++) {
var sound = self._howls[i]._soundById(ids[j]);

if (sound && sound._node) {
  sound._node.volume = sound._volume * vol;
...
```

#### <a name="apidoc.element.howler.Howl.prototype._inactiveSound"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_inactiveSound ()](#apidoc.element.howler.Howl.prototype._inactiveSound)
- description and source-code
```javascript
_inactiveSound = function () {
  var self = this;

  self._drain();

  // Find the first inactive node to recycle.
  for (var i=0; i<self._sounds.length; i++) {
    if (self._sounds[i]._ended) {
      return self._sounds[i].reset();
    }
  }

  // If no inactive node was found, create a new one.
  return new Sound(self);
}
```
- example usage
```shell
...
    sprite = null;
  } else {
    id = null;
  }
}

// Get the selected node, or get one from the pool.
var sound = id ? self._soundById(id) : self._inactiveSound();

// If the sound doesn't exist, do nothing.
if (!sound) {
  return null;
}

// Select the sprite definition.
...
```

#### <a name="apidoc.element.howler.Howl.prototype._loadQueue"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_loadQueue ()](#apidoc.element.howler.Howl.prototype._loadQueue)
- description and source-code
```javascript
_loadQueue = function () {
  var self = this;

  if (self._queue.length > 0) {
    var task = self._queue[0];

    // don't move onto the next task until this one is done
    self.once(task.event, function() {
      self._queue.shift();
      self._loadQueue();
    });

    task.action();
  }

  return self;
}
```
- example usage
```shell
...

  if (self._queue.length > 0) {
    var task = self._queue[0];

    // don't move onto the next task until this one is done
    self.once(task.event, function() {
      self._queue.shift();
      self._loadQueue();
    });

    task.action();
  }

  return self;
},
...
```

#### <a name="apidoc.element.howler.Howl.prototype._refreshBuffer"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_refreshBuffer (sound)](#apidoc.element.howler.Howl.prototype._refreshBuffer)
- description and source-code
```javascript
_refreshBuffer = function (sound) {
  var self = this;

  // Setup the buffer source for playback.
  sound._node.bufferSource = Howler.ctx.createBufferSource();
  sound._node.bufferSource.buffer = cache[self._src];

  // Connect to the correct node.
  if (sound._panner) {
    sound._node.bufferSource.connect(sound._panner);
  } else {
    sound._node.bufferSource.connect(sound._node);
  }

  // Setup looping and playback rate.
  sound._node.bufferSource.loop = sound._loop;
  if (sound._loop) {
    sound._node.bufferSource.loopStart = sound._start || 0;
    sound._node.bufferSource.loopEnd = sound._stop;
  }
  sound._node.bufferSource.playbackRate.value = sound._rate;

  return self;
}
```
- example usage
```shell
...
      sound._loop = !!(sound._loop || self._sprite[sprite][2]);

      // Begin the actual playback.
      var node = sound._node;
      if (self._webAudio) {
        // Fire this when the sound is ready to play to begin Web Audio playback.
        var playWebAudio = function() {
self._refreshBuffer(sound);

// Setup the playback params.
var vol = (sound._muted || self._muted) ? 0 : sound._volume;
node.gain.setValueAtTime(vol, Howler.ctx.currentTime);
sound._playStart = Howler.ctx.currentTime;

// Play the sound using the supported method.
...
```

#### <a name="apidoc.element.howler.Howl.prototype._soundById"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_soundById (id)](#apidoc.element.howler.Howl.prototype._soundById)
- description and source-code
```javascript
_soundById = function (id) {
  var self = this;

  // Loop through all sounds and find the one with this ID.
  for (var i=0; i<self._sounds.length; i++) {
    if (id === self._sounds[i]._id) {
      return self._sounds[i];
    }
  }

  return null;
}
```
- example usage
```shell
...
for (var i=0; i<self._howls.length; i++) {
  if (!self._howls[i]._webAudio) {
    // Get all of the sounds in this Howl group.
    var ids = self._howls[i]._getSoundIds();

    // Loop through all sounds and change the volumes.
    for (var j=0; j<ids.length; j++) {
      var sound = self._howls[i]._soundById(ids[j]);

      if (sound && sound._node) {
        sound._node.volume = sound._volume * vol;
      }
    }
  }
}
...
```

#### <a name="apidoc.element.howler.Howl.prototype._stopFade"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>_stopFade (id)](#apidoc.element.howler.Howl.prototype._stopFade)
- description and source-code
```javascript
_stopFade = function (id) {
  var self = this;
  var sound = self._soundById(id);

  if (sound && sound._interval) {
    if (self._webAudio) {
      sound._node.gain.cancelScheduledValues(Howler.ctx.currentTime);
    }

    clearInterval(sound._interval);
    sound._interval = null;
    self._emit('fade', id);
  }

  return self;
}
```
- example usage
```shell
...
        if (sound && !sound._paused) {
// Reset the seek position.
sound._seek = self.seek(ids[i]);
sound._rateSeek = 0;
sound._paused = true;

// Stop currently running fades.
self._stopFade(ids[i]);

if (sound._node) {
  if (self._webAudio) {
    // make sure the sound has been created
    if (!sound._node.bufferSource) {
      return self;
    }
...
```

#### <a name="apidoc.element.howler.Howl.prototype.duration"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>duration (id)](#apidoc.element.howler.Howl.prototype.duration)
- description and source-code
```javascript
duration = function (id) {
  var self = this;
  var duration = self._duration;

  // If we pass an ID, get the sound and return the sprite length.
  var sound = self._soundById(id);
  if (sound) {
    duration = self._sprite[sound._sprite][1] / 1000;
  }

  return duration;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.howler.Howl.prototype.fade"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>fade (from, to, len, id)](#apidoc.element.howler.Howl.prototype.fade)
- description and source-code
```javascript
fade = function (from, to, len, id) {
  var self = this;
  var diff = Math.abs(from - to);
  var dir = from > to ? 'out' : 'in';
  var steps = diff / 0.01;
  var stepLen = (steps > 0) ? len / steps : len;

  // Since browsers clamp timeouts to 4ms, we need to clamp our steps to that too.
  if (stepLen < 4) {
    steps = Math.ceil(steps / (4 / stepLen));
    stepLen = 4;
  }

  // If the sound hasn't loaded, add it to the load queue to fade when capable.
  if (self._state !== 'loaded') {
    self._queue.push({
      event: 'fade',
      action: function() {
        self.fade(from, to, len, id);
      }
    });

    return self;
  }

  // Set the volume to the start position.
  self.volume(from, id);

  // Fade the volume of one or all sounds.
  var ids = self._getSoundIds(id);
  for (var i=0; i<ids.length; i++) {
    // Get the sound.
    var sound = self._soundById(ids[i]);

    // Create a linear fade or fall back to timeouts with HTML5 Audio.
    if (sound) {
      // Stop the previous fade if no sprite is being used (otherwise, volume handles this).
      if (!id) {
        self._stopFade(ids[i]);
      }

      // If we are using Web Audio, let the native methods do the actual fade.
      if (self._webAudio && !sound._muted) {
        var currentTime = Howler.ctx.currentTime;
        var end = currentTime + (len / 1000);
        sound._volume = from;
        sound._node.gain.setValueAtTime(from, currentTime);
        sound._node.gain.linearRampToValueAtTime(to, end);
      }

      var vol = from;
      sound._interval = setInterval(function(soundId, sound) {
        // Update the volume amount, but only if the volume should change.
        if (steps > 0) {
          vol += (dir === 'in' ? 0.01 : -0.01);
        }

        // Make sure the volume is in the right bounds.
        vol = Math.max(0, vol);
        vol = Math.min(1, vol);

        // Round to within 2 decimal points.
        vol = Math.round(vol * 100) / 100;

        // Change the volume.
        if (self._webAudio) {
          if (typeof id === 'undefined') {
            self._volume = vol;
          }

          sound._volume = vol;
        } else {
          self.volume(vol, soundId, true);
        }

        // When the fade is complete, stop it and fire event.
        if ((to < from && vol <= to) || (to > from && vol >= to)) {
          clearInterval(sound._interval);
          sound._interval = null;
          self.volume(to, soundId);
          self._emit('fade', soundId);
        }
      }.bind(self, ids[i], sound), stepLen);
    }
  }

  return self;
}
```
- example usage
```shell
...

// Play returns a uniqe Sound ID that can be passed
// into any method on Howl to control that specific sound.
var id1 = sound.play();
var id2 = sound.play();

// Fade out the first sound and speed up the second.
sound.fade(1, 0, 1000, id1);
sound.rate(1.5, id2);
'''

More in-depth examples (with accompanying live demos) can be found in the [examples directory](https://github.com/goldfire/howler
.js/tree/master/examples).


## Core
...
```

#### <a name="apidoc.element.howler.Howl.prototype.init"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>init (o)](#apidoc.element.howler.Howl.prototype.init)
- description and source-code
```javascript
init = function (o) {
  var self = this;

  // Setup user-defined default properties.
  self._orientation = o.orientation || [1, 0, 0];
  self._stereo = o.stereo || null;
  self._pos = o.pos || null;
  self._pannerAttr = {
    coneInnerAngle: typeof o.coneInnerAngle !== 'undefined' ? o.coneInnerAngle : 360,
    coneOuterAngle: typeof o.coneOuterAngle !== 'undefined' ? o.coneOuterAngle : 360,
    coneOuterGain: typeof o.coneOuterGain !== 'undefined' ? o.coneOuterGain : 0,
    distanceModel: typeof o.distanceModel !== 'undefined' ? o.distanceModel : 'inverse',
    maxDistance: typeof o.maxDistance !== 'undefined' ? o.maxDistance : 10000,
    panningModel: typeof o.panningModel !== 'undefined' ? o.panningModel : 'HRTF',
    refDistance: typeof o.refDistance !== 'undefined' ? o.refDistance : 1,
    rolloffFactor: typeof o.rolloffFactor !== 'undefined' ? o.rolloffFactor : 1
  };

  // Setup event listeners.
  self._onstereo = o.onstereo ? [{fn: o.onstereo}] : [];
  self._onpos = o.onpos ? [{fn: o.onpos}] : [];
  self._onorientation = o.onorientation ? [{fn: o.onorientation}] : [];

  // Complete initilization with howler.js core's init function.
  return _super.call(this, o);
}
```
- example usage
```shell
...
/***************************************************************************/

/**
 * Create the global controller. All contained methods and properties apply
 * to all sounds that are currently playing or will be in the future.
 */
var HowlerGlobal = function() {
  this.init();
};
HowlerGlobal.prototype = {
  /**
   * Initialize the global Howler object.
   * @return {Howler}
   */
  init: function() {
...
```

#### <a name="apidoc.element.howler.Howl.prototype.load"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>load ()](#apidoc.element.howler.Howl.prototype.load)
- description and source-code
```javascript
load = function () {
  var self = this;
  var url = null;

  // If no audio is available, quit immediately.
  if (Howler.noAudio) {
    self._emit('loaderror', null, 'No audio support.');
    return;
  }

  // Make sure our source is in an array.
  if (typeof self._src === 'string') {
    self._src = [self._src];
  }

  // Loop through the sources and pick the first one that is compatible.
  for (var i=0; i<self._src.length; i++) {
    var ext, str;

    if (self._format && self._format[i]) {
      // If an extension was specified, use that instead.
      ext = self._format[i];
    } else {
      // Make sure the source is a string.
      str = self._src[i];
      if (typeof str !== 'string') {
        self._emit('loaderror', null, 'Non-string found in selected audio sources - ignoring.');
        continue;
      }

      // Extract the file extension from the URL or base64 data URI.
      ext = /^data:audio\/([^;,]+);/i.exec(str);
      if (!ext) {
        ext = /\.([^.]+)$/.exec(str.split('?', 1)[0]);
      }

      if (ext) {
        ext = ext[1].toLowerCase();
      }
    }

    // Log a warning if no extension was found.
    if (!ext) {
      console.warn('No file extension was found. Consider using the "format" property or specify an extension.');
    }

    // Check if this extension is available.
    if (ext && Howler.codecs(ext)) {
      url = self._src[i];
      break;
    }
  }

  if (!url) {
    self._emit('loaderror', null, 'No codec support for selected audio sources.');
    return;
  }

  self._src = url;
  self._state = 'loading';

  // If the hosting page is HTTPS and the source isn't,
  // drop down to HTML5 Audio to avoid Mixed Content errors.
  if (window.location.protocol === 'https:' && url.slice(0, 5) === 'http:') {
    self._html5 = true;
    self._webAudio = false;
  }

  // Create a new sound object and add it to the pool.
  new Sound(self);

  // Load and decode the audio data for playback.
  if (self._webAudio) {
    loadBuffer(self);
  }

  return self;
}
```
- example usage
```shell
...
        self.play();
      }
    });
  }

  // Load the source file unless otherwise specified.
  if (self._preload) {
    self.load();
  }

  return self;
},

/**
 * Load the audio file.
...
```

#### <a name="apidoc.element.howler.Howl.prototype.loop"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>loop ()](#apidoc.element.howler.Howl.prototype.loop)
- description and source-code
```javascript
loop = function () {
  var self = this;
  var args = arguments;
  var loop, id, sound;

  // Determine the values for loop and id.
  if (args.length === 0) {
    // Return the grou's loop value.
    return self._loop;
  } else if (args.length === 1) {
    if (typeof args[0] === 'boolean') {
      loop = args[0];
      self._loop = loop;
    } else {
      // Return this sound's loop value.
      sound = self._soundById(parseInt(args[0], 10));
      return sound ? sound._loop : false;
    }
  } else if (args.length === 2) {
    loop = args[0];
    id = parseInt(args[1], 10);
  }

  // If no id is passed, get all ID's to be looped.
  var ids = self._getSoundIds(id);
  for (var i=0; i<ids.length; i++) {
    sound = self._soundById(ids[i]);

    if (sound) {
      sound._loop = loop;
      if (self._webAudio && sound._node && sound._node.bufferSource) {
        sound._node.bufferSource.loop = loop;
        if (loop) {
          sound._node.bufferSource.loopStart = sound._start || 0;
          sound._node.bufferSource.loopEnd = sound._stop;
        }
      }
    }
  }

  return self;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.howler.Howl.prototype.mute"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>mute (muted, id)](#apidoc.element.howler.Howl.prototype.mute)
- description and source-code
```javascript
mute = function (muted, id) {
  var self = this;

  // If the sound hasn't loaded, add it to the load queue to mute when capable.
  if (self._state !== 'loaded') {
    self._queue.push({
      event: 'mute',
      action: function() {
        self.mute(muted, id);
      }
    });

    return self;
  }

  // If applying mute/unmute to all sounds, update the group's value.
  if (typeof id === 'undefined') {
    if (typeof muted === 'boolean') {
      self._muted = muted;
    } else {
      return self._muted;
    }
  }

  // If no id is passed, get all ID's to be muted.
  var ids = self._getSoundIds(id);

  for (var i=0; i<ids.length; i++) {
    // Get the sound.
    var sound = self._soundById(ids[i]);

    if (sound) {
      sound._muted = muted;

      if (self._webAudio && sound._node) {
        sound._node.gain.setValueAtTime(muted ? 0 : sound._volume, Howler.ctx.currentTime);
      } else if (sound._node) {
        sound._node.muted = Howler._muted ? true : muted;
      }

      self._emit('mute', sound._id);
    }
  }

  return self;
}
```
- example usage
```shell
...
var self = this;

// If the sound hasn't loaded, add it to the load queue to mute when capable.
if (self._state !== 'loaded') {
  self._queue.push({
    event: 'mute',
    action: function() {
      self.mute(muted, id);
    }
  });

  return self;
}

// If applying mute/unmute to all sounds, update the group's value.
...
```

#### <a name="apidoc.element.howler.Howl.prototype.off"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>off (event, fn, id)](#apidoc.element.howler.Howl.prototype.off)
- description and source-code
```javascript
off = function (event, fn, id) {
  var self = this;
  var events = self['_on' + event];
  var i = 0;

  if (fn) {
    // Loop through event store and remove the passed function.
    for (i=0; i<events.length; i++) {
      if (fn === events[i].fn && id === events[i].id) {
        events.splice(i, 1);
        break;
      }
    }
  } else if (event) {
    // Clear out all events of this type.
    self['_on' + event] = [];
  } else {
    // Clear out all events of every type.
    var keys = Object.keys(self);
    for (i=0; i<keys.length; i++) {
      if ((keys[i].indexOf('_on') === 0) && Array.isArray(self[keys[i]])) {
        self[keys[i]] = [];
      }
    }
  }

  return self;
}
```
- example usage
```shell
...
    if (!events[i].id || events[i].id === id || event === 'load') {
      setTimeout(function(fn) {
        fn.call(this, id, msg);
      }.bind(self, events[i].fn), 0);

      // If this event was setup with 'once', remove it.
      if (events[i].once) {
        self.off(event, events[i].fn, events[i].id);
      }
    }
  }

  return self;
},
...
```

#### <a name="apidoc.element.howler.Howl.prototype.on"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>on (event, fn, id, once)](#apidoc.element.howler.Howl.prototype.on)
- description and source-code
```javascript
on = function (event, fn, id, once) {
  var self = this;
  var events = self['_on' + event];

  if (typeof fn === 'function') {
    events.push(once ? {id: id, fn: fn, once: once} : {id: id, fn: fn});
  }

  return self;
}
```
- example usage
```shell
...

// Clear listener after first call.
sound.once('load', function(){
  sound.play();
});

// Fires when the sound finishes playing.
sound.on('end', function(){
  console.log('Finished!');
});
'''

##### Control multiple sounds:
'''javascript
var sound = new Howl({
...
```

#### <a name="apidoc.element.howler.Howl.prototype.once"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>once (event, fn, id)](#apidoc.element.howler.Howl.prototype.once)
- description and source-code
```javascript
once = function (event, fn, id) {
  var self = this;

  // Setup the event listener.
  self.on(event, fn, id, 1);

  return self;
}
```
- example usage
```shell
...
##### Listen for events:
'''javascript
var sound = new Howl({
  src: ['sound.webm', 'sound.mp3']
});

// Clear listener after first call.
sound.once('load', function(){
  sound.play();
});

// Fires when the sound finishes playing.
sound.on('end', function(){
  console.log('Finished!');
});
...
```

#### <a name="apidoc.element.howler.Howl.prototype.orientation"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>orientation (x, y, z, id)](#apidoc.element.howler.Howl.prototype.orientation)
- description and source-code
```javascript
orientation = function (x, y, z, id) {
  var self = this;

  // Stop right here if not using Web Audio.
  if (!self._webAudio) {
    return self;
  }

  // If the sound hasn't loaded, add it to the load queue to change orientation when capable.
  if (self._state !== 'loaded') {
    self._queue.push({
      event: 'orientation',
      action: function() {
        self.orientation(x, y, z, id);
      }
    });

    return self;
  }

  // Set the defaults for optional 'y' & 'z'.
  y = (typeof y !== 'number') ? self._orientation[1] : y;
  z = (typeof z !== 'number') ? self._orientation[2] : z;

  // Setup the group's spatial orientation if no ID is passed.
  if (typeof id === 'undefined') {
    // Return the group's spatial orientation if no parameters are passed.
    if (typeof x === 'number') {
      self._orientation = [x, y, z];
    } else {
      return self._orientation;
    }
  }

  // Change the spatial orientation of one or all sounds in group.
  var ids = self._getSoundIds(id);
  for (var i=0; i<ids.length; i++) {
    // Get the sound.
    var sound = self._soundById(ids[i]);

    if (sound) {
      if (typeof x === 'number') {
        sound._orientation = [x, y, z];

        if (sound._node) {
          // Check if there is a panner setup and create a new one if not.
          if (!sound._panner) {
            // Make sure we have a position to setup the node with.
            if (!sound._pos) {
              sound._pos = self._pos || [0, 0, -0.5];
            }

            setupPanner(sound, 'spatial');
          }

          sound._panner.setOrientation(x, y, z);
        }

        self._emit('orientation', sound._id);
      } else {
        return sound._orientation;
      }
    }
  }

  return self;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.howler.Howl.prototype.pannerAttr"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>pannerAttr ()](#apidoc.element.howler.Howl.prototype.pannerAttr)
- description and source-code
```javascript
pannerAttr = function () {
  var self = this;
  var args = arguments;
  var o, id, sound;

  // Stop right here if not using Web Audio.
  if (!self._webAudio) {
    return self;
  }

  // Determine the values based on arguments.
  if (args.length === 0) {
    // Return the group's panner attribute values.
    return self._pannerAttr;
  } else if (args.length === 1) {
    if (typeof args[0] === 'object') {
      o = args[0];

      // Set the grou's panner attribute values.
      if (typeof id === 'undefined') {
        self._pannerAttr = {
          coneInnerAngle: typeof o.coneInnerAngle !== 'undefined' ? o.coneInnerAngle : self._coneInnerAngle,
          coneOuterAngle: typeof o.coneOuterAngle !== 'undefined' ? o.coneOuterAngle : self._coneOuterAngle,
          coneOuterGain: typeof o.coneOuterGain !== 'undefined' ? o.coneOuterGain : self._coneOuterGain,
          distanceModel: typeof o.distanceModel !== 'undefined' ? o.distanceModel : self._distanceModel,
          maxDistance: typeof o.maxDistance !== 'undefined' ? o.maxDistance : self._maxDistance,
          panningModel: typeof o.panningModel !== 'undefined' ? o.panningModel : self._panningModel,
          refDistance: typeof o.refDistance !== 'undefined' ? o.refDistance : self._refDistance,
          rolloffFactor: typeof o.rolloffFactor !== 'undefined' ? o.rolloffFactor : self._rolloffFactor
        };
      }
    } else {
      // Return this sound's panner attribute values.
      sound = self._soundById(parseInt(args[0], 10));
      return sound ? sound._pannerAttr : self._pannerAttr;
    }
  } else if (args.length === 2) {
    o = args[0];
    id = parseInt(args[1], 10);
  }

  // Update the values of the specified sounds.
  var ids = self._getSoundIds(id);
  for (var i=0; i<ids.length; i++) {
    sound = self._soundById(ids[i]);

    if (sound) {
      // Merge the new values into the sound.
      var pa = sound._pannerAttr;
      pa = {
        coneInnerAngle: typeof o.coneInnerAngle !== 'undefined' ? o.coneInnerAngle : pa.coneInnerAngle,
        coneOuterAngle: typeof o.coneOuterAngle !== 'undefined' ? o.coneOuterAngle : pa.coneOuterAngle,
        coneOuterGain: typeof o.coneOuterGain !== 'undefined' ? o.coneOuterGain : pa.coneOuterGain,
        distanceModel: typeof o.distanceModel !== 'undefined' ? o.distanceModel : pa.distanceModel,
        maxDistance: typeof o.maxDistance !== 'undefined' ? o.maxDistance : pa.maxDistance,
        panningModel: typeof o.panningModel !== 'undefined' ? o.panningModel : pa.panningModel,
        refDistance: typeof o.refDistance !== 'undefined' ? o.refDistance : pa.refDistance,
        rolloffFactor: typeof o.rolloffFactor !== 'undefined' ? o.rolloffFactor : pa.rolloffFactor
      };

      // Update the panner values or create a new panner if none exists.
      var panner = sound._panner;
      if (panner) {
        panner.coneInnerAngle = pa.coneInnerAngle;
        panner.coneOuterAngle = pa.coneOuterAngle;
        panner.coneOuterGain = pa.coneOuterGain;
        panner.distanceModel = pa.distanceModel;
        panner.maxDistance = pa.maxDistance;
        panner.panningModel = pa.panningModel;
        panner.refDistance = pa.refDistance;
        panner.rolloffFactor = pa.rolloffFactor;
      } else {
        // Make sure we have a position to setup the node with.
        if (!sound._pos) {
          sound._pos = self._pos || [0, 0, -0.5];
        }

        // Create a new panner node.
        setupPanner(sound, 'spatial');
      }
    }
  }

  return self;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.howler.Howl.prototype.pause"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>pause (id)](#apidoc.element.howler.Howl.prototype.pause)
- description and source-code
```javascript
pause = function (id) {
  var self = this;

  // If the sound hasn't loaded, add it to the load queue to pause when capable.
  if (self._state !== 'loaded') {
    self._queue.push({
      event: 'pause',
      action: function() {
        self.pause(id);
      }
    });

    return self;
  }

  // If no id is passed, get all ID's to be paused.
  var ids = self._getSoundIds(id);

  for (var i=0; i<ids.length; i++) {
    // Clear the end timer.
    self._clearTimer(ids[i]);

    // Get the sound.
    var sound = self._soundById(ids[i]);

    if (sound && !sound._paused) {
      // Reset the seek position.
      sound._seek = self.seek(ids[i]);
      sound._rateSeek = 0;
      sound._paused = true;

      // Stop currently running fades.
      self._stopFade(ids[i]);

      if (sound._node) {
        if (self._webAudio) {
          // make sure the sound has been created
          if (!sound._node.bufferSource) {
            return self;
          }

          if (typeof sound._node.bufferSource.stop === 'undefined') {
            sound._node.bufferSource.noteOff(0);
          } else {
            sound._node.bufferSource.stop(0);
          }

          // Clean up the buffer source.
          self._cleanBuffer(sound._node);
        } else if (!isNaN(sound._node.duration) || sound._node.duration === Infinity) {
          sound._node.pause();
        }
      }
    }

    // Fire the pause event, unless 'true' is passed as the 2nd argument.
    if (!arguments[1]) {
      self._emit('pause', sound ? sound._id : null);
    }
  }

  return self;
}
```
- example usage
```shell
...
var self = this;

// If the sound hasn't loaded, add it to the load queue to pause when capable.
if (self._state !== 'loaded') {
  self._queue.push({
    event: 'pause',
    action: function() {
      self.pause(id);
    }
  });

  return self;
}

// If no id is passed, get all ID's to be paused.
...
```

#### <a name="apidoc.element.howler.Howl.prototype.play"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>play (sprite, internal)](#apidoc.element.howler.Howl.prototype.play)
- description and source-code
```javascript
play = function (sprite, internal) {
  var self = this;
  var id = null;

  // Determine if a sprite, sound id or nothing was passed
  if (typeof sprite === 'number') {
    id = sprite;
    sprite = null;
  } else if (typeof sprite === 'string' && self._state === 'loaded' && !self._sprite[sprite]) {
    // If the passed sprite doesn't exist, do nothing.
    return null;
  } else if (typeof sprite === 'undefined') {
    // Use the default sound sprite (plays the full audio length).
    sprite = '__default';

    // Check if there is a single paused sound that isn't ended.
    // If there is, play that sound. If not, continue as usual.
    var num = 0;
    for (var i=0; i<self._sounds.length; i++) {
      if (self._sounds[i]._paused && !self._sounds[i]._ended) {
        num++;
        id = self._sounds[i]._id;
      }
    }

    if (num === 1) {
      sprite = null;
    } else {
      id = null;
    }
  }

  // Get the selected node, or get one from the pool.
  var sound = id ? self._soundById(id) : self._inactiveSound();

  // If the sound doesn't exist, do nothing.
  if (!sound) {
    return null;
  }

  // Select the sprite definition.
  if (id && !sprite) {
    sprite = sound._sprite || '__default';
  }

  // If we have no sprite and the sound hasn't loaded, we must wait
  // for the sound to load to get our audio's duration.
  if (self._state !== 'loaded' && !self._sprite[sprite]) {
    self._queue.push({
      event: 'play',
      action: function() {
        self.play(self._soundById(sound._id) ? sound._id : undefined);
      }
    });

    return sound._id;
  }

  // Don't play the sound if an id was passed and it is already playing.
  if (id && !sound._paused) {
    // Trigger the play event, in order to keep iterating through queue.
    if (!internal) {
      setTimeout(function() {
        self._emit('play', sound._id);
      }, 0);
    }

    return sound._id;
  }

  // Make sure the AudioContext isn't suspended, and resume it if it is.
  if (self._webAudio) {
    Howler._autoResume();
  }

  // Determine how long to play for and where to start playing.
  var seek = Math.max(0, sound._seek > 0 ? sound._seek : self._sprite[sprite][0] / 1000);
  var duration = Math.max(0, ((self._sprite[sprite][0] + self._sprite[sprite][1]) / 1000) - seek);
  var timeout = (duration * 1000) / Math.abs(sound._rate);

  // Update the parameters of the sound
  sound._paused = false;
  sound._ended = false;
  sound._sprite = sprite;
  sound._seek = seek;
  sound._start = self._sprite[sprite][0] / 1000;
  sound._stop = (self._sprite[sprite][0] + self._sprite[sprite][1]) / 1000;
  sound._loop = !!(sound._loop || self._sprite[sprite][2]);

  // Begin the actual playback.
  var node = sound._node;
  if (self._webAudio) {
    // Fire this when the sound is ready to play to begin Web Audio playback.
    var playWebAudio = function() {
      self._refreshBuffer(sound);

      // Setup the playback params.
      var vol = (sound._muted || self._muted) ? 0 : sound._volume;
      node.gain.setValueAtTime(vol, Howler.ctx.currentTime);
      sound._playStart = Howler.ctx.currentTime;

      // Play the sound using the supported method.
      if (typeof node.bufferSource.start === 'undefined') {
        sound._loop ? node.bufferSource.noteGrainOn(0, seek, 86400) : node.bufferSource.noteGrainOn(0, seek, duration);
      } else {
        sound._loop ? node.bufferSource.start(0, seek, 86400) : node.bufferSource.start(0, seek, duration);
      }

      // Start a new timer if none is present.
      if (timeout !== Infinity) {
        self._endTimers[sound._id] = setTimeout(self._ended.bind(self, sound), timeout);
      }

      if (!internal) {
        setTimeout(function() {
          self._emit('play', sound._id);
        }, 0);
      }
    };

    var isRunning = (Howler.state === 'running');
    if (self._state === 'loaded' && isRunning) {
      playWebAudio();
    } else {
      // Wait for the audio to load and then begin playback.
      var event = !isRunning && self._state === 'loaded' ? 'resume' : 'load';
      self.once(event, playWebAudio, isRunn ...
```
- example usage
```shell
...

##### Most basic, play an MP3:
'''javascript
var sound = new Howl({
src: ['sound.mp3']
});

sound.play();
'''

##### More playback options:
'''javascript
var sound = new Howl({
src: ['sound.webm', 'sound.mp3', 'sound.wav'],
autoplay: true,
...
```

#### <a name="apidoc.element.howler.Howl.prototype.playing"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>playing (id)](#apidoc.element.howler.Howl.prototype.playing)
- description and source-code
```javascript
playing = function (id) {
  var self = this;

  // Check the passed sound ID (if any).
  if (typeof id === 'number') {
    var sound = self._soundById(id);
    return sound ? !sound._paused : false;
  }

  // Otherwise, loop through all sounds and check if any are playing.
  for (var i=0; i<self._sounds.length; i++) {
    if (!self._sounds[i]._paused) {
      return true;
    }
  }

  return false;
}
```
- example usage
```shell
...

      // Get the sound.
      var sound = self._soundById(id);

      if (sound) {
        if (typeof seek === 'number' && seek >= 0) {
// Pause the sound and update position for restarting playback.
var playing = self.playing(id);
if (playing) {
  self.pause(id, true);
}

// Move the position of the track and cancel timer.
sound._seek = seek;
sound._ended = false;
...
```

#### <a name="apidoc.element.howler.Howl.prototype.pos"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>pos (x, y, z, id)](#apidoc.element.howler.Howl.prototype.pos)
- description and source-code
```javascript
pos = function (x, y, z, id) {
  var self = this;

  // Stop right here if not using Web Audio.
  if (!self._webAudio) {
    return self;
  }

  // If the sound hasn't loaded, add it to the load queue to change position when capable.
  if (self._state !== 'loaded') {
    self._queue.push({
      event: 'pos',
      action: function() {
        self.pos(x, y, z, id);
      }
    });

    return self;
  }

  // Set the defaults for optional 'y' & 'z'.
  y = (typeof y !== 'number') ? 0 : y;
  z = (typeof z !== 'number') ? -0.5 : z;

  // Setup the group's spatial position if no ID is passed.
  if (typeof id === 'undefined') {
    // Return the group's spatial position if no parameters are passed.
    if (typeof x === 'number') {
      self._pos = [x, y, z];
    } else {
      return self._pos;
    }
  }

  // Change the spatial position of one or all sounds in group.
  var ids = self._getSoundIds(id);
  for (var i=0; i<ids.length; i++) {
    // Get the sound.
    var sound = self._soundById(ids[i]);

    if (sound) {
      if (typeof x === 'number') {
        sound._pos = [x, y, z];

        if (sound._node) {
          // Check if there is a panner setup and create a new one if not.
          if (!sound._panner || sound._panner.pan) {
            setupPanner(sound, 'spatial');
          }

          sound._panner.setPosition(x, y, z);
        }

        self._emit('pos', sound._id);
      } else {
        return sound._pos;
      }
    }
  }

  return self;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.howler.Howl.prototype.rate"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>rate ()](#apidoc.element.howler.Howl.prototype.rate)
- description and source-code
```javascript
rate = function () {
  var self = this;
  var args = arguments;
  var rate, id;

  // Determine the values based on arguments.
  if (args.length === 0) {
    // We will simply return the current rate of the first node.
    id = self._sounds[0]._id;
  } else if (args.length === 1) {
    // First check if this is an ID, and if not, assume it is a new rate value.
    var ids = self._getSoundIds();
    var index = ids.indexOf(args[0]);
    if (index >= 0) {
      id = parseInt(args[0], 10);
    } else {
      rate = parseFloat(args[0]);
    }
  } else if (args.length === 2) {
    rate = parseFloat(args[0]);
    id = parseInt(args[1], 10);
  }

  // Update the playback rate or return the current value.
  var sound;
  if (typeof rate === 'number') {
    // If the sound hasn't loaded, add it to the load queue to change playback rate when capable.
    if (self._state !== 'loaded') {
      self._queue.push({
        event: 'rate',
        action: function() {
          self.rate.apply(self, args);
        }
      });

      return self;
    }

    // Set the group rate.
    if (typeof id === 'undefined') {
      self._rate = rate;
    }

    // Update one or all volumes.
    id = self._getSoundIds(id);
    for (var i=0; i<id.length; i++) {
      // Get the sound.
      sound = self._soundById(id[i]);

      if (sound) {
        // Keep track of our position when the rate changed and update the playback
        // start position so we can properly adjust the seek position for time elapsed.
        sound._rateSeek = self.seek(id[i]);
        sound._playStart = self._webAudio ? Howler.ctx.currentTime : sound._playStart;
        sound._rate = rate;

        // Change the playback rate.
        if (self._webAudio && sound._node && sound._node.bufferSource) {
          sound._node.bufferSource.playbackRate.value = rate;
        } else if (sound._node) {
          sound._node.playbackRate = rate;
        }

        // Reset the timers.
        var seek = self.seek(id[i]);
        var duration = ((self._sprite[sound._sprite][0] + self._sprite[sound._sprite][1]) / 1000) - seek;
        var timeout = (duration * 1000) / Math.abs(sound._rate);

        // Start a new end timer if sound is already playing.
        if (self._endTimers[id[i]] || !sound._paused) {
          self._clearTimer(id[i]);
          self._endTimers[id[i]] = setTimeout(self._ended.bind(self, sound), timeout);
        }

        self._emit('rate', sound._id);
      }
    }
  } else {
    sound = self._soundById(id);
    return sound ? sound._rate : self._rate;
  }

  return self;
}
```
- example usage
```shell
...
// Play returns a uniqe Sound ID that can be passed
// into any method on Howl to control that specific sound.
var id1 = sound.play();
var id2 = sound.play();

// Fade out the first sound and speed up the second.
sound.fade(1, 0, 1000, id1);
sound.rate(1.5, id2);
'''

More in-depth examples (with accompanying live demos) can be found in the [examples directory](https://github.com/goldfire/howler
.js/tree/master/examples).


## Core
...
```

#### <a name="apidoc.element.howler.Howl.prototype.seek"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>seek ()](#apidoc.element.howler.Howl.prototype.seek)
- description and source-code
```javascript
seek = function () {
  var self = this;
  var args = arguments;
  var seek, id;

  // Determine the values based on arguments.
  if (args.length === 0) {
    // We will simply return the current position of the first node.
    id = self._sounds[0]._id;
  } else if (args.length === 1) {
    // First check if this is an ID, and if not, assume it is a new seek position.
    var ids = self._getSoundIds();
    var index = ids.indexOf(args[0]);
    if (index >= 0) {
      id = parseInt(args[0], 10);
    } else {
      id = self._sounds[0]._id;
      seek = parseFloat(args[0]);
    }
  } else if (args.length === 2) {
    seek = parseFloat(args[0]);
    id = parseInt(args[1], 10);
  }

  // If there is no ID, bail out.
  if (typeof id === 'undefined') {
    return self;
  }

  // If the sound hasn't loaded, add it to the load queue to seek when capable.
  if (self._state !== 'loaded') {
    self._queue.push({
      event: 'seek',
      action: function() {
        self.seek.apply(self, args);
      }
    });

    return self;
  }

  // Get the sound.
  var sound = self._soundById(id);

  if (sound) {
    if (typeof seek === 'number' && seek >= 0) {
      // Pause the sound and update position for restarting playback.
      var playing = self.playing(id);
      if (playing) {
        self.pause(id, true);
      }

      // Move the position of the track and cancel timer.
      sound._seek = seek;
      sound._ended = false;
      self._clearTimer(id);

      // Restart the playback if the sound was playing.
      if (playing) {
        self.play(id, true);
      }

      // Update the seek position for HTML5 Audio.
      if (!self._webAudio && sound._node) {
        sound._node.currentTime = seek;
      }

      self._emit('seek', id);
    } else {
      if (self._webAudio) {
        var realTime = self.playing(id) ? Howler.ctx.currentTime - sound._playStart : 0;
        var rateSeek = sound._rateSeek ? sound._rateSeek - sound._seek : 0;
        return sound._seek + (rateSeek + realTime * Math.abs(sound._rate));
      } else {
        return sound._node.currentTime;
      }
    }
  }

  return self;
}
```
- example usage
```shell
...
        self._clearTimer(ids[i]);

        // Get the sound.
        var sound = self._soundById(ids[i]);

        if (sound && !sound._paused) {
// Reset the seek position.
sound._seek = self.seek(ids[i]);
sound._rateSeek = 0;
sound._paused = true;

// Stop currently running fades.
self._stopFade(ids[i]);

if (sound._node) {
...
```

#### <a name="apidoc.element.howler.Howl.prototype.state"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>state ()](#apidoc.element.howler.Howl.prototype.state)
- description and source-code
```javascript
state = function () {
  return this._state;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.howler.Howl.prototype.stereo"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>stereo (pan, id)](#apidoc.element.howler.Howl.prototype.stereo)
- description and source-code
```javascript
stereo = function (pan, id) {
  var self = this;

  // Stop right here if not using Web Audio.
  if (!self._webAudio) {
    return self;
  }

  // If the sound hasn't loaded, add it to the load queue to change stereo pan when capable.
  if (self._state !== 'loaded') {
    self._queue.push({
      event: 'stereo',
      action: function() {
        self.stereo(pan, id);
      }
    });

    return self;
  }

  // Check for PannerStereoNode support and fallback to PannerNode if it doesn't exist.
  var pannerType = (typeof Howler.ctx.createStereoPanner === 'undefined') ? 'spatial' : 'stereo';

  // Setup the group's stereo panning if no ID is passed.
  if (typeof id === 'undefined') {
    // Return the group's stereo panning if no parameters are passed.
    if (typeof pan === 'number') {
      self._stereo = pan;
      self._pos = [pan, 0, 0];
    } else {
      return self._stereo;
    }
  }

  // Change the streo panning of one or all sounds in group.
  var ids = self._getSoundIds(id);
  for (var i=0; i<ids.length; i++) {
    // Get the sound.
    var sound = self._soundById(ids[i]);

    if (sound) {
      if (typeof pan === 'number') {
        sound._stereo = pan;
        sound._pos = [pan, 0, 0];

        if (sound._node) {
          // If we are falling back, make sure the panningModel is equalpower.
          sound._pannerAttr.panningModel = 'equalpower';

          // Check if there is a panner setup and create a new one if not.
          if (!sound._panner || !sound._panner.pan) {
            setupPanner(sound, pannerType);
          }

          if (pannerType === 'spatial') {
            sound._panner.setPosition(pan, 0, 0);
          } else {
            sound._panner.pan.value = pan;
          }
        }

        self._emit('stereo', sound._id);
      } else {
        return sound._stereo;
      }
    }
  }

  return self;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.howler.Howl.prototype.stop"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>stop (id, internal)](#apidoc.element.howler.Howl.prototype.stop)
- description and source-code
```javascript
stop = function (id, internal) {
  var self = this;

  // If the sound hasn't loaded, add it to the load queue to stop when capable.
  if (self._state !== 'loaded') {
    self._queue.push({
      event: 'stop',
      action: function() {
        self.stop(id);
      }
    });

    return self;
  }

  // If no id is passed, get all ID's to be stopped.
  var ids = self._getSoundIds(id);

  for (var i=0; i<ids.length; i++) {
    // Clear the end timer.
    self._clearTimer(ids[i]);

    // Get the sound.
    var sound = self._soundById(ids[i]);

    if (sound) {
      // Reset the seek position.
      sound._seek = sound._start || 0;
      sound._rateSeek = 0;
      sound._paused = true;
      sound._ended = true;

      // Stop currently running fades.
      self._stopFade(ids[i]);

      if (sound._node) {
        if (self._webAudio) {
          // make sure the sound has been created
          if (!sound._node.bufferSource) {
            if (!internal) {
              self._emit('stop', sound._id);
            }

            return self;
          }

          if (typeof sound._node.bufferSource.stop === 'undefined') {
            sound._node.bufferSource.noteOff(0);
          } else {
            sound._node.bufferSource.stop(0);
          }

          // Clean up the buffer source.
          self._cleanBuffer(sound._node);
        } else if (!isNaN(sound._node.duration) || sound._node.duration === Infinity) {
          sound._node.currentTime = sound._start || 0;
          sound._node.pause();
        }
      }
    }

    if (sound && !internal) {
      self._emit('stop', sound._id);
    }
  }

  return self;
}
```
- example usage
```shell
...
  if (!sound._node.bufferSource) {
    return self;
  }

  if (typeof sound._node.bufferSource.stop === 'undefined') {
    sound._node.bufferSource.noteOff(0);
  } else {
    sound._node.bufferSource.stop(0);
  }

  // Clean up the buffer source.
  self._cleanBuffer(sound._node);
} else if (!isNaN(sound._node.duration) || sound._node.duration === Infinity) {
  sound._node.pause();
}
...
```

#### <a name="apidoc.element.howler.Howl.prototype.unload"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>unload ()](#apidoc.element.howler.Howl.prototype.unload)
- description and source-code
```javascript
unload = function () {
  var self = this;

  // Stop playing any active sounds.
  var sounds = self._sounds;
  for (var i=0; i<sounds.length; i++) {
    // Stop the sound if it is currently playing.
    if (!sounds[i]._paused) {
      self.stop(sounds[i]._id);
    }

    // Remove the source or disconnect.
    if (!self._webAudio) {
      // Set the source to 0-second silence to stop any downloading.
      sounds[i]._node.src = 'data:audio/wav;base64,UklGRigAAABXQVZFZm10IBIAAAABAAEARKwAAIhYAQACABAAAABkYXRhAgAAAAEA';

      // Remove any event listeners.
      sounds[i]._node.removeEventListener('error', sounds[i]._errorFn, false);
      sounds[i]._node.removeEventListener(Howler._canPlayEvent, sounds[i]._loadFn, false);
    }

    // Empty out all of the nodes.
    delete sounds[i]._node;

    // Make sure all timers are cleared out.
    self._clearTimer(sounds[i]._id);

    // Remove the references in the global Howler object.
    var index = Howler._howls.indexOf(self);
    if (index >= 0) {
      Howler._howls.splice(index, 1);
    }
  }

  // Delete this sound from the cache (if no other Howl is using it).
  var remCache = true;
  for (i=0; i<Howler._howls.length; i++) {
    if (Howler._howls[i]._src === self._src) {
      remCache = false;
      break;
    }
  }

  if (cache && remCache) {
    delete cache[self._src];
  }

  // Clear global errors.
  Howler.noAudio = false;

  // Clear out 'self'.
  self._state = 'unloaded';
  self._sounds = [];
  self = null;

  return null;
}
```
- example usage
```shell
...
     * Unload and destroy all currently loaded Howl objects.
     * @return {Howler}
     */
    unload: function() {
var self = this || Howler;

for (var i=self._howls.length-1; i>=0; i--) {
  self._howls[i].unload();
}

// Create a new AudioContext to make sure it is fully reset.
if (self.usingWebAudio && self.ctx && typeof self.ctx.close !== 'undefined') {
  self.ctx.close();
  self.ctx = null;
  setupAudioContext();
...
```

#### <a name="apidoc.element.howler.Howl.prototype.volume"></a>[function <span class="apidocSignatureSpan">howler.Howl.prototype.</span>volume ()](#apidoc.element.howler.Howl.prototype.volume)
- description and source-code
```javascript
volume = function () {
  var self = this;
  var args = arguments;
  var vol, id;

  // Determine the values based on arguments.
  if (args.length === 0) {
    // Return the value of the groups' volume.
    return self._volume;
  } else if (args.length === 1 || args.length === 2 && typeof args[1] === 'undefined') {
    // First check if this is an ID, and if not, assume it is a new volume.
    var ids = self._getSoundIds();
    var index = ids.indexOf(args[0]);
    if (index >= 0) {
      id = parseInt(args[0], 10);
    } else {
      vol = parseFloat(args[0]);
    }
  } else if (args.length >= 2) {
    vol = parseFloat(args[0]);
    id = parseInt(args[1], 10);
  }

  // Update the volume or return the current volume.
  var sound;
  if (typeof vol !== 'undefined' && vol >= 0 && vol <= 1) {
    // If the sound hasn't loaded, add it to the load queue to change volume when capable.
    if (self._state !== 'loaded') {
      self._queue.push({
        event: 'volume',
        action: function() {
          self.volume.apply(self, args);
        }
      });

      return self;
    }

    // Set the group volume.
    if (typeof id === 'undefined') {
      self._volume = vol;
    }

    // Update one or all volumes.
    id = self._getSoundIds(id);
    for (var i=0; i<id.length; i++) {
      // Get the sound.
      sound = self._soundById(id[i]);

      if (sound) {
        sound._volume = vol;

        // Stop currently running fades.
        if (!args[2]) {
          self._stopFade(id[i]);
        }

        if (self._webAudio && sound._node && !sound._muted) {
          sound._node.gain.setValueAtTime(vol, Howler.ctx.currentTime);
        } else if (sound._node && !sound._muted) {
          sound._node.volume = vol * Howler.volume();
        }

        self._emit('volume', sound._id);
      }
    }
  } else {
    sound = id ? self._soundById(id) : self._sounds[0];
    return sound ? sound._volume : 0;
  }

  return self;
}
```
- example usage
```shell
...
self._clearTimer(sound._id);
        }
      } else {
        // Fire this when the sound is ready to play to begin HTML5 Audio playback.
        var playHtml5 = function() {
node.currentTime = seek;
node.muted = sound._muted || self._muted || Howler._muted || node.muted;
node.volume = sound._volume * Howler.volume();
node.playbackRate = sound._rate;
node.play();

// Setup the new end timer.
if (timeout !== Infinity) {
  self._endTimers[sound._id] = setTimeout(self._ended.bind(self, sound), timeout);
}
...
```



# <a name="apidoc.module.howler.howler_core"></a>[module howler.howler_core](#apidoc.module.howler.howler_core)

#### <a name="apidoc.element.howler.howler_core.Howl"></a>[function <span class="apidocSignatureSpan">howler.howler_core.</span>Howl (o)](#apidoc.element.howler.howler_core.Howl)
- description and source-code
```javascript
Howl = function (o) {
  var self = this;

  // Throw an error if no source is provided.
  if (!o.src || o.src.length === 0) {
    console.error('An array of source files must be passed with any new Howl.');
    return;
  }

  self.init(o);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
