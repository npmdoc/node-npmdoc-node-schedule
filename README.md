# api documentation for  [node-schedule (v1.2.1)](https://github.com/node-schedule/node-schedule#readme)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-node-schedule.svg)](https://travis-ci.org/npmdoc/node-npmdoc-node-schedule)
#### A cron-like and not-cron-like job scheduler for Node.

[![NPM](https://nodei.co/npm/node-schedule.png?downloads=true)](https://www.npmjs.com/package/node-schedule)

[![apidoc](https://npmdoc.github.io/node-npmdoc-node-schedule/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-node_schedule_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-node-schedule/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-node-schedule/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Matt Patenaude",
        "email": "matt@mattpatenaude.com",
        "url": "http://mattpatenaude.com"
    },
    "bugs": {
        "url": "https://github.com/node-schedule/node-schedule/issues"
    },
    "dependencies": {
        "cron-parser": "1.1.0",
        "long-timeout": "0.1.1",
        "sorted-array-functions": "^1.0.0"
    },
    "description": "A cron-like and not-cron-like job scheduler for Node.",
    "devDependencies": {
        "coveralls": "^2.11.2",
        "eslint": "^0.15.1",
        "istanbul": "^0.4.5",
        "nodeunit": "^0.10.2",
        "sinon": "^1.14.1"
    },
    "directories": {},
    "dist": {
        "shasum": "8800b34d0cceb0ff0318432ef9f20b2499630e36",
        "tarball": "https://registry.npmjs.org/node-schedule/-/node-schedule-1.2.1.tgz"
    },
    "gitHead": "aa45a76109f3968c8f7a2d63363f8b44ce3f493a",
    "homepage": "https://github.com/node-schedule/node-schedule#readme",
    "keywords": [
        "schedule",
        "task",
        "job",
        "cron"
    ],
    "license": "MIT",
    "main": "./lib/schedule.js",
    "maintainers": [
        {
            "name": "mattpat",
            "email": "matt@mattpatenaude.com"
        },
        {
            "name": "tejasmanohar",
            "email": "me@tejas.io"
        },
        {
            "name": "sgimeno",
            "email": "santiago.gimeno@gmail.com"
        },
        {
            "name": "jonhester",
            "email": "jon.d.hester@gmail.com"
        }
    ],
    "name": "node-schedule",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/node-schedule/node-schedule.git"
    },
    "scripts": {
        "lint": "eslint lib",
        "test": "nodeunit"
    },
    "version": "1.2.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module node-schedule](#apidoc.module.node-schedule)
1.  [function <span class="apidocSignatureSpan">node-schedule.</span>Invocation (job, fireDate, recurrenceRule, endDate)](#apidoc.element.node-schedule.Invocation)
1.  [function <span class="apidocSignatureSpan">node-schedule.</span>Job (name, job, callback)](#apidoc.element.node-schedule.Job)
1.  [function <span class="apidocSignatureSpan">node-schedule.</span>Range (start, end, step)](#apidoc.element.node-schedule.Range)
1.  [function <span class="apidocSignatureSpan">node-schedule.</span>RecurrenceRule (year, month, date, dayOfWeek, hour, minute, second)](#apidoc.element.node-schedule.RecurrenceRule)
1.  [function <span class="apidocSignatureSpan">node-schedule.</span>cancelJob (job)](#apidoc.element.node-schedule.cancelJob)
1.  [function <span class="apidocSignatureSpan">node-schedule.</span>rescheduleJob (job, spec)](#apidoc.element.node-schedule.rescheduleJob)
1.  [function <span class="apidocSignatureSpan">node-schedule.</span>scheduleJob ()](#apidoc.element.node-schedule.scheduleJob)
1.  object <span class="apidocSignatureSpan">node-schedule.</span>Job.prototype
1.  object <span class="apidocSignatureSpan">node-schedule.</span>Range.prototype
1.  object <span class="apidocSignatureSpan">node-schedule.</span>RecurrenceRule.prototype
1.  object <span class="apidocSignatureSpan">node-schedule.</span>scheduledJobs

#### [module node-schedule.Job](#apidoc.module.node-schedule.Job)
1.  [function <span class="apidocSignatureSpan">node-schedule.</span>Job (name, job, callback)](#apidoc.element.node-schedule.Job.Job)
1.  [function <span class="apidocSignatureSpan">node-schedule.Job.</span>super_ ()](#apidoc.element.node-schedule.Job.super_)

#### [module node-schedule.Job.prototype](#apidoc.module.node-schedule.Job.prototype)
1.  [function <span class="apidocSignatureSpan">node-schedule.Job.prototype.</span>invoke ()](#apidoc.element.node-schedule.Job.prototype.invoke)
1.  [function <span class="apidocSignatureSpan">node-schedule.Job.prototype.</span>runOnDate (date)](#apidoc.element.node-schedule.Job.prototype.runOnDate)
1.  [function <span class="apidocSignatureSpan">node-schedule.Job.prototype.</span>schedule (spec)](#apidoc.element.node-schedule.Job.prototype.schedule)

#### [module node-schedule.Range](#apidoc.module.node-schedule.Range)
1.  [function <span class="apidocSignatureSpan">node-schedule.</span>Range (start, end, step)](#apidoc.element.node-schedule.Range.Range)

#### [module node-schedule.Range.prototype](#apidoc.module.node-schedule.Range.prototype)
1.  [function <span class="apidocSignatureSpan">node-schedule.Range.prototype.</span>contains (val)](#apidoc.element.node-schedule.Range.prototype.contains)

#### [module node-schedule.RecurrenceRule](#apidoc.module.node-schedule.RecurrenceRule)
1.  [function <span class="apidocSignatureSpan">node-schedule.</span>RecurrenceRule (year, month, date, dayOfWeek, hour, minute, second)](#apidoc.element.node-schedule.RecurrenceRule.RecurrenceRule)

#### [module node-schedule.RecurrenceRule.prototype](#apidoc.module.node-schedule.RecurrenceRule.prototype)
1.  [function <span class="apidocSignatureSpan">node-schedule.RecurrenceRule.prototype.</span>nextInvocationDate (base)](#apidoc.element.node-schedule.RecurrenceRule.prototype.nextInvocationDate)



# <a name="apidoc.module.node-schedule"></a>[module node-schedule](#apidoc.module.node-schedule)

#### <a name="apidoc.element.node-schedule.Invocation"></a>[function <span class="apidocSignatureSpan">node-schedule.</span>Invocation (job, fireDate, recurrenceRule, endDate)](#apidoc.element.node-schedule.Invocation)
- description and source-code
```javascript
function Invocation(job, fireDate, recurrenceRule, endDate) {
  this.job = job;
  this.fireDate = fireDate;
  this.endDate = endDate;
  this.recurrenceRule = recurrenceRule || DoesntRecur;

  this.timerID = null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-schedule.Job"></a>[function <span class="apidocSignatureSpan">node-schedule.</span>Job (name, job, callback)](#apidoc.element.node-schedule.Job)
- description and source-code
```javascript
function Job(name, job, callback) {
  // setup a private pendingInvocations variable
  var pendingInvocations = [];

  //setup a private number of invocations variable
  var triggeredJobs = 0;

  // Set scope vars
  var jobName = name && typeof name === 'string' ? name : '<Anonymous Job ' + (++anonJobCounter) + '>';
  this.job = name && typeof name === 'function' ? name : job;

  // Make sure callback is actually a callback
  if (this.job === name) {
    // Name wasn't provided and maybe a callback is there
    this.callback = typeof job === 'function' ? job : false;
  } else {
    // Name was provided, and maybe a callback is there
    this.callback = typeof callback === 'function' ? callback : false;
  }

  // Check for generator
  if (typeof this.job === 'function' &&
      this.job.prototype &&
      this.job.prototype.next) {
    this.job = function() {
      return this.next().value;
    }.bind(this.job.call(this));
  }

  // define properties
  Object.defineProperty(this, 'name', {
    value: jobName,
    writable: false,
    enumerable: true
  });

  // method that require private access
  this.trackInvocation = function(invocation) {
    // add to our invocation list
    sorted.add(pendingInvocations, invocation, sorter);
    return true;
  };
  this.stopTrackingInvocation = function(invocation) {
    var invIdx = pendingInvocations.indexOf(invocation);
    if (invIdx > -1) {
      pendingInvocations.splice(invIdx, 1);
      return true;
    }

    return false;
  };
  this.triggeredJobs = function() {
    return triggeredJobs;
  };
  this.setTriggeredJobs = function(triggeredJob) {
    triggeredJobs = triggeredJob;
  };
  this.cancel = function(reschedule) {
    reschedule = (typeof reschedule == 'boolean') ? reschedule : false;

    var inv, newInv;
    var newInvs = [];
    for (var j = 0; j < pendingInvocations.length; j++) {
      inv = pendingInvocations[j];

      cancelInvocation(inv);

      if (reschedule && inv.recurrenceRule.recurs) {
        newInv = scheduleNextRecurrence(inv.recurrenceRule, this, inv.fireDate, inv.endDate);
        if (newInv !== null) {
          newInvs.push(newInv);
        }
      }
    }

    pendingInvocations = [];

    for (var k = 0; k < newInvs.length; k++) {
      this.trackInvocation(newInvs[k]);
    }

    // remove from scheduledJobs if reschedule === false
    if (!reschedule) {
      if (this.name) {
        delete scheduledJobs[this.name];
      }
    }

    return true;
  };
  this.cancelNext = function(reschedule) {
    reschedule = (typeof reschedule == 'boolean') ? reschedule : true;

    if (!pendingInvocations.length) {
      return false;
    }

    var newInv;
    var nextInv = pendingInvocations.shift();

    cancelInvocation(nextInv);

    if (reschedule && nextInv.recurrenceRule.recurs) {
      newInv = scheduleNextRecurrence(nextInv.recurrenceRule, this, nextInv.fireDate, nextInv.endDate);
      if (newInv !== null) {
        this.trackInvocation(newInv);
      }
    }

    return true;
  };
  this.reschedule = function(spec) {
    var inv;
    var cInvs = pendingInvocations.slice();

    for (var j = 0; j < cInvs.length; j++) {
      inv = cInvs[j];

      cancelInvocation(inv);
    }

    pendingInvocations = [];

    if (this.schedule(spec)) {
      this.setTriggeredJobs(0);
      return true;
    } else {
      pendingInvocations = cInvs;
      return false;
    }
  };
  this.nextInvocation = function() {
    if (!pendingInvocations.length) {
      return null;
    }
    return pendingInvocations[0].fireDate;
  };
  this.pendingInvocations = function() {
    return pendingInvocations;
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-schedule.Range"></a>[function <span class="apidocSignatureSpan">node-schedule.</span>Range (start, end, step)](#apidoc.element.node-schedule.Range)
- description and source-code
```javascript
function Range(start, end, step) {
  this.start = start || 0;
  this.end = end || 60;
  this.step = step || 1;
}
```
- example usage
```shell
...

You can also use arrays to specify a list of acceptable values, and the 'Range'
object to specify a range of start and end values, with an optional step parameter.
For instance, this will print a message on Thursday, Friday, Saturday, and Sunday at 5pm:

'''js
var rule = new schedule.RecurrenceRule();
rule.dayOfWeek = [0, new schedule.Range(4, 6)];
rule.hour = 17;
rule.minute = 0;

var j = schedule.scheduleJob(rule, function(){
  console.log('Today is recognized by Rebecca Black!');
});
'''
...
```

#### <a name="apidoc.element.node-schedule.RecurrenceRule"></a>[function <span class="apidocSignatureSpan">node-schedule.</span>RecurrenceRule (year, month, date, dayOfWeek, hour, minute, second)](#apidoc.element.node-schedule.RecurrenceRule)
- description and source-code
```javascript
function RecurrenceRule(year, month, date, dayOfWeek, hour, minute, second) {
  this.recurs = true;

  this.year = (year == null) ? null : year;
  this.month = (month == null) ? null : month;
  this.date = (date == null) ? null : date;
  this.dayOfWeek = (dayOfWeek == null) ? null : dayOfWeek;
  this.hour = (hour == null) ? null : hour;
  this.minute = (minute == null) ? null : minute;
  this.second = (second == null) ? 0 : second;
}
```
- example usage
```shell
...

You can build recurrence rules to specify when a job should recur. For instance,
consider this rule, which executes the function every hour at 42 minutes after the hour:

'''js
var schedule = require('node-schedule');

var rule = new schedule.RecurrenceRule();
rule.minute = 42;

var j = schedule.scheduleJob(rule, function(){
  console.log('The answer to life, the universe, and everything!');
});
'''
...
```

#### <a name="apidoc.element.node-schedule.cancelJob"></a>[function <span class="apidocSignatureSpan">node-schedule.</span>cancelJob (job)](#apidoc.element.node-schedule.cancelJob)
- description and source-code
```javascript
function cancelJob(job) {
  var success = false;
  if (job instanceof Job) {
    success = job.cancel();
  } else if (typeof job == 'string' || job instanceof String) {
    if (job in scheduledJobs && scheduledJobs.hasOwnProperty(job)) {
      success = scheduledJobs[job].cancel();
    }
  }

  return success;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-schedule.rescheduleJob"></a>[function <span class="apidocSignatureSpan">node-schedule.</span>rescheduleJob (job, spec)](#apidoc.element.node-schedule.rescheduleJob)
- description and source-code
```javascript
function rescheduleJob(job, spec) {
  if (job instanceof Job) {
    if (job.reschedule(spec)) {
      return job;
    }
  } else if (typeof job == 'string' || job instanceof String) {
    if (job in scheduledJobs && scheduledJobs.hasOwnProperty(job)) {
      if (scheduledJobs[job].reschedule(spec)) {
        return scheduledJobs[job];
      }
    }
  }
  return null;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-schedule.scheduleJob"></a>[function <span class="apidocSignatureSpan">node-schedule.</span>scheduleJob ()](#apidoc.element.node-schedule.scheduleJob)
- description and source-code
```javascript
function scheduleJob() {
  if (arguments.length < 2) {
    return null;
  }

  var name = (arguments.length >= 3 && typeof arguments[0] === 'string') ? arguments[0] : null;
  var spec = name ? arguments[1] : arguments[0];
  var method = name ? arguments[2] : arguments[1];
  var callback = name ? arguments[3] : arguments[2];

  var job = new Job(name, method, callback);

  if (job.schedule(spec)) {
    return job;
  }

  return null;
}
```
- example usage
```shell
...
'''

Examples with the cron format:

'''js
var schedule = require('node-schedule');

var j = schedule.scheduleJob('42 * * * *', function(){
  console.log('The answer to life, the universe, and everything!');
});
'''

Execute a cron job when the minute is 42 (e.g. 19:42, 20:42, etc.).

And:
...
```



# <a name="apidoc.module.node-schedule.Job"></a>[module node-schedule.Job](#apidoc.module.node-schedule.Job)

#### <a name="apidoc.element.node-schedule.Job.Job"></a>[function <span class="apidocSignatureSpan">node-schedule.</span>Job (name, job, callback)](#apidoc.element.node-schedule.Job.Job)
- description and source-code
```javascript
function Job(name, job, callback) {
  // setup a private pendingInvocations variable
  var pendingInvocations = [];

  //setup a private number of invocations variable
  var triggeredJobs = 0;

  // Set scope vars
  var jobName = name && typeof name === 'string' ? name : '<Anonymous Job ' + (++anonJobCounter) + '>';
  this.job = name && typeof name === 'function' ? name : job;

  // Make sure callback is actually a callback
  if (this.job === name) {
    // Name wasn't provided and maybe a callback is there
    this.callback = typeof job === 'function' ? job : false;
  } else {
    // Name was provided, and maybe a callback is there
    this.callback = typeof callback === 'function' ? callback : false;
  }

  // Check for generator
  if (typeof this.job === 'function' &&
      this.job.prototype &&
      this.job.prototype.next) {
    this.job = function() {
      return this.next().value;
    }.bind(this.job.call(this));
  }

  // define properties
  Object.defineProperty(this, 'name', {
    value: jobName,
    writable: false,
    enumerable: true
  });

  // method that require private access
  this.trackInvocation = function(invocation) {
    // add to our invocation list
    sorted.add(pendingInvocations, invocation, sorter);
    return true;
  };
  this.stopTrackingInvocation = function(invocation) {
    var invIdx = pendingInvocations.indexOf(invocation);
    if (invIdx > -1) {
      pendingInvocations.splice(invIdx, 1);
      return true;
    }

    return false;
  };
  this.triggeredJobs = function() {
    return triggeredJobs;
  };
  this.setTriggeredJobs = function(triggeredJob) {
    triggeredJobs = triggeredJob;
  };
  this.cancel = function(reschedule) {
    reschedule = (typeof reschedule == 'boolean') ? reschedule : false;

    var inv, newInv;
    var newInvs = [];
    for (var j = 0; j < pendingInvocations.length; j++) {
      inv = pendingInvocations[j];

      cancelInvocation(inv);

      if (reschedule && inv.recurrenceRule.recurs) {
        newInv = scheduleNextRecurrence(inv.recurrenceRule, this, inv.fireDate, inv.endDate);
        if (newInv !== null) {
          newInvs.push(newInv);
        }
      }
    }

    pendingInvocations = [];

    for (var k = 0; k < newInvs.length; k++) {
      this.trackInvocation(newInvs[k]);
    }

    // remove from scheduledJobs if reschedule === false
    if (!reschedule) {
      if (this.name) {
        delete scheduledJobs[this.name];
      }
    }

    return true;
  };
  this.cancelNext = function(reschedule) {
    reschedule = (typeof reschedule == 'boolean') ? reschedule : true;

    if (!pendingInvocations.length) {
      return false;
    }

    var newInv;
    var nextInv = pendingInvocations.shift();

    cancelInvocation(nextInv);

    if (reschedule && nextInv.recurrenceRule.recurs) {
      newInv = scheduleNextRecurrence(nextInv.recurrenceRule, this, nextInv.fireDate, nextInv.endDate);
      if (newInv !== null) {
        this.trackInvocation(newInv);
      }
    }

    return true;
  };
  this.reschedule = function(spec) {
    var inv;
    var cInvs = pendingInvocations.slice();

    for (var j = 0; j < cInvs.length; j++) {
      inv = cInvs[j];

      cancelInvocation(inv);
    }

    pendingInvocations = [];

    if (this.schedule(spec)) {
      this.setTriggeredJobs(0);
      return true;
    } else {
      pendingInvocations = cInvs;
      return false;
    }
  };
  this.nextInvocation = function() {
    if (!pendingInvocations.length) {
      return null;
    }
    return pendingInvocations[0].fireDate;
  };
  this.pendingInvocations = function() {
    return pendingInvocations;
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-schedule.Job.super_"></a>[function <span class="apidocSignatureSpan">node-schedule.Job.</span>super_ ()](#apidoc.element.node-schedule.Job.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.node-schedule.Job.prototype"></a>[module node-schedule.Job.prototype](#apidoc.module.node-schedule.Job.prototype)

#### <a name="apidoc.element.node-schedule.Job.prototype.invoke"></a>[function <span class="apidocSignatureSpan">node-schedule.Job.prototype.</span>invoke ()](#apidoc.element.node-schedule.Job.prototype.invoke)
- description and source-code
```javascript
invoke = function () {
  if (typeof this.job == 'function') {
    this.setTriggeredJobs(this.triggeredJobs() + 1);
    this.job();
  } else {
    this.job.execute();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-schedule.Job.prototype.runOnDate"></a>[function <span class="apidocSignatureSpan">node-schedule.Job.prototype.</span>runOnDate (date)](#apidoc.element.node-schedule.Job.prototype.runOnDate)
- description and source-code
```javascript
runOnDate = function (date) {
  return this.schedule(date);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-schedule.Job.prototype.schedule"></a>[function <span class="apidocSignatureSpan">node-schedule.Job.prototype.</span>schedule (spec)](#apidoc.element.node-schedule.Job.prototype.schedule)
- description and source-code
```javascript
schedule = function (spec) {
  var self = this;
  var success = false;
  var inv;
  var start;
  var end;

  if (typeof spec === 'object' && spec.rule) {
    start = spec.start || null;
    end = spec.end || null;
    spec = spec.rule;

    if (start != null) {
      if (!(start instanceof Date)) {
        start = new Date(start);
      }
      if (!isValidDate(start) || start.getTime() < Date.now()) {
        start = null;
      }
    }

    if (end != null && !(end instanceof Date) && !isValidDate(end = new Date(end))) {
      end = null;
    }
  }

  try {
    var res = cronParser.parseExpression(spec, { currentDate: start });
    inv = scheduleNextRecurrence(res, self, start, end);
    if (inv !== null) {
      success = self.trackInvocation(inv);
    }

  } catch (err) {
    var type = typeof spec;
    if ((type === 'string') || (type === 'number')) {
      spec = new Date(spec);
    }

    if ((spec instanceof Date) && (isValidDate(spec))) {
      if (spec.getTime() >= Date.now()) {
        inv = new Invocation(self, spec);
        scheduleInvocation(inv);
        success = self.trackInvocation(inv);
      }
    } else if (type === 'object') {
      if (!(spec instanceof RecurrenceRule)) {
        var r = new RecurrenceRule();
        if ('year' in spec) {
          r.year = spec.year;
        }
        if ('month' in spec) {
          r.month = spec.month;
        }
        if ('date' in spec) {
          r.date = spec.date;
        }
        if ('dayOfWeek' in spec) {
          r.dayOfWeek = spec.dayOfWeek;
        }
        if ('hour' in spec) {
          r.hour = spec.hour;
        }
        if ('minute' in spec) {
          r.minute = spec.minute;
        }
        if ('second' in spec) {
          r.second = spec.second;
        }

        spec = r;
      }

      inv = scheduleNextRecurrence(spec, self, start, end);
      if (inv !== null) {
        success = self.trackInvocation(inv);
      }
    }
  }

  scheduledJobs[this.name] = this;
  return success;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.node-schedule.Range"></a>[module node-schedule.Range](#apidoc.module.node-schedule.Range)

#### <a name="apidoc.element.node-schedule.Range.Range"></a>[function <span class="apidocSignatureSpan">node-schedule.</span>Range (start, end, step)](#apidoc.element.node-schedule.Range.Range)
- description and source-code
```javascript
function Range(start, end, step) {
  this.start = start || 0;
  this.end = end || 60;
  this.step = step || 1;
}
```
- example usage
```shell
...

You can also use arrays to specify a list of acceptable values, and the 'Range'
object to specify a range of start and end values, with an optional step parameter.
For instance, this will print a message on Thursday, Friday, Saturday, and Sunday at 5pm:

'''js
var rule = new schedule.RecurrenceRule();
rule.dayOfWeek = [0, new schedule.Range(4, 6)];
rule.hour = 17;
rule.minute = 0;

var j = schedule.scheduleJob(rule, function(){
  console.log('Today is recognized by Rebecca Black!');
});
'''
...
```



# <a name="apidoc.module.node-schedule.Range.prototype"></a>[module node-schedule.Range.prototype](#apidoc.module.node-schedule.Range.prototype)

#### <a name="apidoc.element.node-schedule.Range.prototype.contains"></a>[function <span class="apidocSignatureSpan">node-schedule.Range.prototype.</span>contains (val)](#apidoc.element.node-schedule.Range.prototype.contains)
- description and source-code
```javascript
contains = function (val) {
  if (this.step === null || this.step === 1) {
    return (val >= this.start && val <= this.end);
  } else {
    for (var i = this.start; i < this.end; i += this.step) {
      if (i === val) {
        return true;
      }
    }

    return false;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.node-schedule.RecurrenceRule"></a>[module node-schedule.RecurrenceRule](#apidoc.module.node-schedule.RecurrenceRule)

#### <a name="apidoc.element.node-schedule.RecurrenceRule.RecurrenceRule"></a>[function <span class="apidocSignatureSpan">node-schedule.</span>RecurrenceRule (year, month, date, dayOfWeek, hour, minute, second)](#apidoc.element.node-schedule.RecurrenceRule.RecurrenceRule)
- description and source-code
```javascript
function RecurrenceRule(year, month, date, dayOfWeek, hour, minute, second) {
  this.recurs = true;

  this.year = (year == null) ? null : year;
  this.month = (month == null) ? null : month;
  this.date = (date == null) ? null : date;
  this.dayOfWeek = (dayOfWeek == null) ? null : dayOfWeek;
  this.hour = (hour == null) ? null : hour;
  this.minute = (minute == null) ? null : minute;
  this.second = (second == null) ? 0 : second;
}
```
- example usage
```shell
...

You can build recurrence rules to specify when a job should recur. For instance,
consider this rule, which executes the function every hour at 42 minutes after the hour:

'''js
var schedule = require('node-schedule');

var rule = new schedule.RecurrenceRule();
rule.minute = 42;

var j = schedule.scheduleJob(rule, function(){
  console.log('The answer to life, the universe, and everything!');
});
'''
...
```



# <a name="apidoc.module.node-schedule.RecurrenceRule.prototype"></a>[module node-schedule.RecurrenceRule.prototype](#apidoc.module.node-schedule.RecurrenceRule.prototype)

#### <a name="apidoc.element.node-schedule.RecurrenceRule.prototype.nextInvocationDate"></a>[function <span class="apidocSignatureSpan">node-schedule.RecurrenceRule.prototype.</span>nextInvocationDate (base)](#apidoc.element.node-schedule.RecurrenceRule.prototype.nextInvocationDate)
- description and source-code
```javascript
nextInvocationDate = function (base) {
  base = (base instanceof Date) ? base : (new Date());
  if (!this.recurs) {
    return null;
  }

  var now = new Date();
  var fullYear = now.getFullYear();
  if ((this.year !== null) &&
      (typeof this.year == 'number') &&
      (this.year < fullYear)) {
    return null;
  }

  var next = new CronDate(base.getTime());
  next.addSecond();

  while (true) {
    if (this.year !== null) {
      fullYear = next.getFullYear();
      if ((typeof this.year == 'number') && (this.year < fullYear)) {
        next = null;
        break;
      }

      if (!recurMatch(fullYear, this.year)) {
        next.addYear();
        next.setMonth(0);
        next.setDate(1);
        next.setHours(0);
        next.setMinutes(0);
        next.setSeconds(0);
        continue;
      }
    }
    if (this.month != null && !recurMatch(next.getMonth(), this.month)) {
      next.addMonth();
      continue;
    }
    if (this.date != null && !recurMatch(next.getDate(), this.date)) {
      next.addDay();
      continue;
    }
    if (this.dayOfWeek != null && !recurMatch(next.getDay(), this.dayOfWeek)) {
      next.addDay();
      continue;
    }
    if (this.hour != null && !recurMatch(next.getHours(), this.hour)) {
      next.addHour();
      continue;
    }
    if (this.minute != null && !recurMatch(next.getMinutes(), this.minute)) {
      next.addMinute();
      continue;
    }
    if (this.second != null && !recurMatch(next.getSeconds(), this.second)) {
      next.addSecond();
      continue;
    }

    break;
  }

  return next;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
