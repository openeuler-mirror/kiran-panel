size = 32x32

iconsdir = $(datadir)/icons/hicolor/$(size)/apps

icons_DATA =					\
	kiran-panel-clock.png			\
	kiran-panel-drawer.png			\
	kiran-panel-fish.png			\
	kiran-panel-force-quit.png		\
	kiran-panel-launcher.png		\
	kiran-panel-notification-area.png	\
	kiran-panel-separator.png		\
	kiran-panel.png				\
	kiran-panel-window-list.png		\
	kiran-panel-window-menu.png		\
	kiran-panel-workspace-switcher.png

icons_SOURCE =					\
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
	$(icons_DATA)	\
	$(icons_SOURCE)

-include $(top_srcdir)/git.mk
