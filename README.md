# Animated Gif Support

This library adds support for using animated GIFs as images in Codename One. It's based on [this code](https://gist.github.com/devunwired/4479231) but was adapted for simple usage in Codename One.

You can use the GifImage as any other image in Codename One:

````java
Form hi = new Form("Gif", new BorderLayout());

try {
    hi.add(CENTER, new ScaleImageLabel(GifImage.decode(getResourceAsStream("/giphy-downsized.gif"), 1177720)));
} catch(IOException err) {
    log(err);
}
hi.show();
````

Notice that you need to pass in the length of the input stream that is decoded when opening a gif.

## Changelog
### 2017-12-25
#### Modified
- Loop checking inside animate() function yields sensible results for finite looped gifs.
- Animate function no longer skips last frame.
