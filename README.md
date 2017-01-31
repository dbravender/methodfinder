# methodfinder

A simple way to search for methods / side-effects that change objects a certain way. Be careful - if you are working with objects that delete things or make network calls I wouldn't use this.

## Examples

If you are unfamiliar with Python and want to see how to capitalize a string you can run:

    >>> from methodfinder import methodfinder
    >>> methodfinder('fred', [], 'Fred')
    'fred'.capitalize() == 'Fred'
    'fred'.title() == 'Fred'

It can even find methods that have side effects:

    >>> methodfinder([0, 1, 2, 3], [4], [0, 1, 2, 3, 4])
    o = [0, 1, 2, 3]
    o.append(4)
    o == [0, 1, 2, 3, 4]
