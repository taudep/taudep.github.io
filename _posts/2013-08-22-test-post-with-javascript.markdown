---
title: "This is a test post for code formatting"
categories: python, flask
---

Going to write some GitHub Markdown. Let's test this out.



{% highlight python %}
@app.route('/login/authorized_linkedin')
@linkedin.authorized_handler
def authorized_linkedin(resp):
    if resp is None:
        # error, error_description, state
        flash('Access denied: reason=%s error=%s' % (
                request.args['error'],
                request.args['error_description']
            ), 'alert'
        )
        return login() # TODO: It might make more sense to REDIRECT to a registration page?
{% endhighlight %}




Some Javascript:
{% highlight javascript %}
'use strict';

angular.module('ui.config', []).value('ui.config', {});

//  Regex for Integer Validator
var INTEGER_REGEXP = /^\-?\d*$/;
var CURRENCY_REGEXP = /^(?:\$\s*)?(?:(?:\d{0,3}(?:[, ]\d{0,3})*[, ])+\d{3}|\d+)(?:\.\d*)?(?:\s*\$)?$/;
//  OR ^(\d*\.\d{1,2}|\d+)$
function formatNum(val) {
    val = Math.round(val * 100) / 100;
    val = ("" + val).indexOf(".") > -1 ? val + "00" : val + ".00";
    var dec = val.indexOf(".");
    return dec == val.length - 3 || dec == 0 ? val : val.substring(0, dec + 3);
}
{% endhighlight %}