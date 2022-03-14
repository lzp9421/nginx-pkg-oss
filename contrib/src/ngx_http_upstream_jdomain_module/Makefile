# ngx_http_upstream_jdomain_module

include $(dir $(abspath $(lastword $(MAKEFILE_LIST))))/version
UPSTREAM_JDOMAIN_NGINX_MODULE_GITURL := $(GITHUB)/nicholaschiasson/ngx_upstream_jdomain.git

PKGS += ngx_http_upstream_jdomain_module

$(TARBALLS)/ngx_http_upstream_jdomain_module-$(UPSTREAM_JDOMAIN_NGINX_MODULE_GITHASH).tar.xz:
	$(call download_git,$(UPSTREAM_JDOMAIN_NGINX_MODULE_GITURL),,$(UPSTREAM_JDOMAIN_NGINX_MODULE_GITHASH))

.sum-ngx_http_upstream_jdomain_module: ngx_http_upstream_jdomain_module-$(UPSTREAM_JDOMAIN_NGINX_MODULE_GITHASH).tar.xz
	$(call check_githash,$(UPSTREAM_JDOMAIN_NGINX_MODULE_GITHASH))
	touch $@

ngx_http_upstream_jdomain_module: ngx_http_upstream_jdomain_module-$(UPSTREAM_JDOMAIN_NGINX_MODULE_GITHASH).tar.xz .sum-ngx_http_upstream_jdomain_module
	$(UNPACK)
	$(MOVE)

.ngx_http_upstream_jdomain_module: ngx_http_upstream_jdomain_module
	touch $@
