# NAME

WWW::Yotpo - API for Yotpo

# SYNOPSIS

    use WWW::Yotpo;

    my $yotpo = WWW::Yotpo->new(
        client_id => $ENV{YOTPO_CLIENT_ID}, # from https://my.yotpo.com/settings
        client_secret => $ENV{YOTPO_CLIENT_SECRET},
    );

    my $token = $yotpo->oauth_token();
    my $access_token = $token->{access_token}; # save it somewhere

    my $res = $yotpo->mass_create(
        utoken => $access_token,
        platform => 'general',
        orders => [
            {
                "email" => "client\@example.com",
                "customer_name" => "bob",
                "order_id" => "1121",
                "order_date" => "2013-05-01",
                "currency_iso" => "USD",
                ....

    my $res = $yotpo->purchases(
        utoken => $access_token,
    );

# DESCRIPTION

WWW::Yotpo is for [http://docs.yotpoapi.apiary.io/](http://docs.yotpoapi.apiary.io/)

# AUTHOR

Fayland Lam <fayland@binary.com>

# COPYRIGHT

Copyright 2015- Fayland Lam

# LICENSE

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# SEE ALSO
