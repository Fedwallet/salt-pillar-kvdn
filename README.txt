root@7484193a8698:/# KEY_SET='PWD UID' encodeJson 
{"PWD":"/","UID":"0"}
root@7484193a8698:/# KEY_SET='PWD UID' encodeJson | python /opt/clients-3.3.2-1.0.9/python/kvdn-cli.py --set --key test_key1 this/that                                                                       
JWT_TOKEN not set 
that:test_key1
root@7484193a8698:/# salt '*' pillar.items                                                                                                                                                                   

saltmaster:
    ----------
    complex_pillar_value:
        ----------
        test_key1:
            ----------
            PWD:
                /
            UID:
                0
        test_key2:
            h2ello
    test_value1:
        ----------
        PWD:
            /
        UID:
            0
    test_value2:
        h2ello
