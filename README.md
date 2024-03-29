# commonly-used-scss-mixins

Commonly used scss mixins.

## Usage

### text truncating

```scss
@mixin truncate-text($font-size: 14px, $line-height: 1.4, $lines-to-show: 1) {
  font-size: $font-size;
  line-height: $line-height;
  display: block;
  // Fallback for non-webkit
  display: -webkit-box;
  max-height: $font-size * $line-height * $lines-to-show;
  -webkit-line-clamp: $lines-to-show;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
}

// usage
.text-truncate {
  @include truncate-text(12px, 1.4, 2);
}
```

## License

MIT
