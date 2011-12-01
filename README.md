A simple block based Objective-C wrapper around the Instagram API

Requires AFNetworking (git submodule init && git submodule update)

Simple example:

    // Fetch a user by ID
    [client getUser:@"128643"
            success:^(InstagramUser* user) {
                NSLog(@"Got user : %@ (%@)", user.fullname, user.username);
            } 
            failure:^(NSError *error, NSInteger statusCode) {
                NSLog(@"Error fetching user %ld - %@", statusCode, [error localizedDescription]);
            }
     ];

Check InstagramClient.h for all endpoints

You'll need a client ID from http://instagram.com/developer/manage/

Note : Only the user endpoints are currently implemented (http://instagram.com/developer/endpoints/users/)