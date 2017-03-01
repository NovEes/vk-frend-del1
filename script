vk.api.friends.getRequests({
    extended: 0,
    out: 1,
    need_mutual: 1
}, function (x) {
    log('Will be deleted [' + x.response.items.length + '] of [' + x.response.count + ']');
    x.response.items.map(y => vk.api.friends.delete({
        user_id: y.user_id
    }, function () {
        log("User deleted ", y.user_id);
    }));
});
