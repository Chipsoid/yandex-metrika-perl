=encoding utf-8

=head1 NAME

Yandex::Metrika - It's module to get access to Yandex.Metrika API via OAuth

=head1 SYNOPSIS

    use Yandex::Metrika;

    my $metrika = Yandex::Metrika->new( token => '*******************************', counter => 1234567 );

    $metrika->set_per_page( 20 ); # optional, default 100
    $metrika->set_pretty( 1 ); # optional, default 1

    $metrika->user_vars({ date1 => '20150501', date2 => '20150501', table_mode => 'tree', group => 'all' });

    # if answer contains {links}->{next} you can load next page by

    $metrika->user_vars({ next => 1});
    
    # show next link

    say $metrika->next_url;


=head1 DESCRIPTION

Yandex::Metrika is using Yandex::OAuth::Client as base class to get access.
API methods are mapped to object methods.
See api docs for parameters and response formats at https://tech.yandex.ru/metrika/doc/ref/stat/api-stat-method-docpage/

Looking for contributors for this and other Yandex.APIs


=head1 METHODS

=over

=item B<traffic()>

=item B<conversion()>

=item B<sites()>

=item B<search_engines()>

=item B<phrases()>

=item B<social_networks()>

=item B<marketing()>

=item B<direct_summary()>

=item B<direct_platforms_all()>

=item B<direct_platform_types()>

=item B<direct_regions()>

=item B<tags()>

=item B<geo()>

=item B<interest()>

=item B<demography_age()>

=item B<demography_gender()>

=item B<demography_structure()>

=item B<deepness_time()>

=item B<deepness_depth()>

=item B<hourly()>

=item B<popular()>

=item B<entrance()>

=item B<exit()>

=item B<titles()>

=item B<url_param()>

=item B<share_services()>

=item B<share_titles()>

=item B<links()>

=item B<downloads()>

=item B<user_vars()>

=item B<ecommerce()>

=item B<browsers()>

=item B<os()>

=item B<display_all()>

=item B<display_groups()>

=item B<mobile_devices()>

=item B<mobile_phones()>

=item B<flash()>

=item B<silverlight()>

=item B<java()>

=item B<cookies()>

=item B<javascript()>

=item B<load()>

=item B<load_minutely_24()>

=item B<load_minutely_all()>

=item B<robots_all()>

=item B<robot_types()>

=back

=head1 LICENSE

Copyright (C) Andrey Kuzmin.

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

=head1 AUTHOR

Andrey Kuzmin E<lt>chipsoid@cpan.orgE<gt>

=cut