
# tfc.same_padding_for_kernel

### Aliases:

* `tfc.python.ops.padding_ops.same_padding_for_kernel`
* `tfc.same_padding_for_kernel`

``` python
tfc.same_padding_for_kernel(
    shape,
    corr,
    strides_up=None
)
```



Defined in [`python/ops/padding_ops.py`](https://github.com/tensorflow/compression/tree/master/python/ops/padding_ops.py).

<!-- Placeholder for "Used in" -->

Determine correct amount of padding for `same` convolution.

To implement `'same'` convolutions, we first pad the image, and then perform a
`'valid'` convolution or correlation. Given the kernel shape, this function
determines the correct amount of padding so that the output of the convolution
or correlation is the same size as the pre-padded input.

#### Args:

* <b>`shape`</b>: Shape of the convolution kernel (without the channel dimensions).
* <b>`corr`</b>: Boolean. If `True`, assume cross correlation, if `False`, convolution.
* <b>`strides_up`</b>: If this is used for an upsampled convolution, specify the
    strides here. (For downsampled convolutions, specify `(1, 1)`: in that
    case, the strides don't matter.)


#### Returns:

The amount of padding at the beginning and end for each dimension.