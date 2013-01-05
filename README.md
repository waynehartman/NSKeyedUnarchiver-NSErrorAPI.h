NSKeyedUnarchiver+NSErrorAPI.h
==============================

For those that abhore try/catch and need something a little more flexible when using NSKeyedUnarchiver.

##How to use it

Nothing to it really, just:

    NSError *error = nil;
    NSDictionary *dict = [NSKeyedUnarchiver unarchiveObjectWithData:dictionary 
                                                              error:&error];
                                     
	if (dict) {
	   //  happy day, proceed
	} else {
		NSLog(@"error unarchiving: %@", error.description);
		// handle error condition
	}
