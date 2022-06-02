size = scalable

iconsdir = $(datadir)/icons/hicolor/$(size)/apps

icons_DATA =					\
	kiran-panel-clock.svg			\
	kiran-panel-drawer.svg			\
	kiran-panel-fish.svg			\
	kiran-panel-force-quit.svg		\
	kiran-panel-launcher.svg		\
	kiran-panel-notification-area.svg	\
	kiran-panel-separator.svg		\
	kiran-panel.svg				\
	kiran-panel-window-list.svg		\
	kiran-panel-window-menu.svg		\
	kiran-panel-workspace-switcher.svg

gtk_update_icon_cache = gtk-update-icon-cache -f -t $(datadir)/icons/hicolor

install-data-hook: update-icon-cache
uninstall-hook: update-icon-cache
update-icon-cache:
	@-if test -z "$(DESTDIR)"; then \
		echo "Updating Gtk icon cache."; \
		$(gtk_update_icon_cache); \
	else \
		echo "*** Icon cache not updated. After (un)install, run this:"; \
		echo "***   $(gtk_update_icon_cache)"; \
	fi

EXTRA_DIST =		\
	$(icons_DATA)

-include $(top_srcdir)/git.mk
