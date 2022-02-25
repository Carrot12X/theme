@import url(https://mwittrien.github.io/BetterDiscordAddons/Themes/_res/SettingsIcons.css);
@import url(https://mwittrien.github.io/BetterDiscordAddons/Themes/_res/UsrBgs.css);
@import url(https://mwittrien.github.io/BetterDiscordAddons/Themes/BlurpleRecolor/BlurpleRecolor.css);

:root {
	--transparencycolor:			0,0,0;
	--transparencyalpha:			0.15;
	--messagetransparency:			0.5;
	--usechatbubbles: 				calc(var(--messagetransparency) / (var(--messagetransparency) + 0.00000000000000000000001));
	--guildchanneltransparency:		0.15;
	--chatinputtransparency:		0.0;
	--memberlisttransparency:		0.0;
	
	--font:							Whitney, Helvetica Neue, Helvetica, Arial, sans-serif;
	--textshadow:					transparent;
	
	--accentcolor:					190,78,180;
	--accentcolor2:					var(--accentcolor);
	--mentioncolor:					var(--accentcolor);
	--linkcolor:					var(--accentcolor);
	
	--successcolor: 				59,165,92;
	--warningcolor: 				250,166,26;
	--dangercolor: 					237,66,69;
	
	--textbrightest: 				255,255,255;
	--textbrighter: 				222,222,222;
	--textbright: 					200,200,200;
	--textdark: 					160,160,160;
	--textdarker: 					125,125,125;
	--textdarkest: 					90,90,90;
	
	--background:					url(https://mwittrien.github.io/BetterDiscordAddons/Themes/BasicBackground/_res/background.jpg);
	--backgroundposition:			center;
	--backgroundsize:				cover;
	--backgroundblur:				unset;
	
	--popout:						var(--background);
	--popoutposition:				var(--backgroundposition);
	--popoutsize:					var(--backgroundsize);
	--popoutblur:					var(--backgroundblur);
	
	--backdrop:						rgba(0,0,0,0.85);
	--backdropposition:				center;
	--backdropsize:					cover;
	--backdropblur:					unset;
	
	--bdfdb-green:					rgb(var(--successcolor));
	--bdfdb-yellow:					rgb(var(--warningcolor));
	--bdfdb-red:					rgb(var(--dangercolor));
}

.theme-light, .theme-dark {
	--text-positive: rgb(var(--successcolor));
	--text-warning: rgb(var(--warningcolor));
	--text-danger: rgb(var(--dangercolor));
	--info-positive-background: rgba(var(--successcolor),.1);
	--info-positive-foreground: rgb(var(--successcolor));
	--info-positive-text: #fff;
	--info-warning-background: rgba(var(--warningcolor),.1);
	--info-warning-foreground: rgb(var(--warningcolor));
	--info-warning-text: #fff;
	--info-danger-background: rgba(var(--dangercolor),.1);
	--info-danger-foreground: rgb(var(--dangercolor));
	--info-danger-text: #fff;
	--status-positive-background: rgb(var(--successcolor));
	--status-positive-text: #fff;
	--status-warning-background: rgb(var(--warningcolor));
	--status-warning-text: #fff;
	--status-danger-background: rgb(var(--dangercolor));
	--status-danger-text: #fff;
	--header-primary: rgb(var(--textbrightest));
	--header-secondary: rgb(var(--textbright));
	--text-normal: rgb(var(--textbrighter));
	--text-muted: rgb(var(--textdarker));
	--channels-default: rgb(var(--textdark));
	--interactive-normal: rgb(var(--textbright));
	--interactive-hover: rgb(var(--textbrighter));
	--interactive-active: rgb(var(--textbrightest));
	--interactive-muted: rgb(var(--textdarkest));
	--logo-primary: rgb(var(--textbrightest));
	--background-accent: rgba(var(--transparencycolor), .1);
	--background-primary: rgba(var(--transparencycolor), .2);
	--background-secondary: rgba(var(--transparencycolor), .3);
	--background-secondary-alt: rgba(var(--transparencycolor), .35);
	--background-tertiary: rgba(var(--transparencycolor), .4);
	--background-floating: rgba(var(--transparencycolor), .5);
	--background-modifier-accent: rgba(var(--textbrightest),.1);
	--elevation-low: 0 1px 5px 0 rgba(var(--transparencycolor), .3);
	--elevation-high: 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	--font-primary: var(--font) !important;
	--font-display: var(--font) !important;
}

html {
	color: var(--header-primary);
}


/* ~~~~		0.		TABLE OF CONTENTS				~~~~ */
/*
	1.	TRANSPARENCY
	2.	BACKGROUND
	3.	TITLEBAR
	4.	GUILDLIST
	5.	CHANNELLIST
		1.	GUILDHEADER
		2.	CHANNELS
		3.	DMCHANNELS
		4.	ACCOUNT/VOICE/GOLIVE
	6.	CHAT
		1.	CHANNELHEADER
		2.	MESSAGES
			1.	MESSAGE
			2.	EMBEDS
			3.	NITROGIFT
			4.	INVITE
		3.	TEXTAREA
		4.	AUTOCOMPLETEMENU
		5.	MEMBERLIST
		6.	SEARCHPAGE
		7.	THREADS
		8.	CALL
		9.	UNAVAILABLESCREEN
	7.	PEOPLES
	8.	STORE/NITRO
	9.	LIBRARY
	10.	DISCOVERY/UNIHUB
	11.	USERSETTINGS
	12.	GUILDSETTINGS
	13.	MODALS
		1.	USERMODAL
		2.	GUILDADD/CREATION
		3.	REGIONSELECTMODAL
		4.	UPLOADMODAL
		5.	KEYBOARDSHORTCUTSMODAL
		6.	QUICKSWITCHER
		7.	INVITEMODAL/GROUPCREATE
		8.	LOGINSCREEN
		9.	TERMACCEPTMODAL
		10.	DOWNLOADAPPMODAL
		11.	GUILDBOOSTMODAL
		12.	REACTIONSMODAL
		13.	GUILDTEMPLATEMODAL
		14.	GUILDWELCOMEMODAL
		15.	GUILDRULESMODAL
		16.	GUILDFEEDBACKMODAL
		17.	SCREENSHAREMODAL
		18.	PHONEVERIFICATIONMODAL
		19.	NOTIFICATIONSMODAL
		20.	DISCOVERYENTRYMODAL
		21.	NITROFEATUREMODAL
	14.	POPOUTS
		1.	CONTEXTMENU
		2.	USERPOPOUT
		3.	EMOJIPICKER
		4.	PINS/MENTIONS
		5.	SEARCHPOPOUT
		6.	COLORPICKER
		7.	ADDROLE
		8.	EVERYONEMENTION
		9.	CHANNELFOLLOW
		10.	CHANNELFOLLOWINFO
		11.	EMOJIINFO
		12.	STREAMPREVIEW
		13.	STREAMINFO
		14.	PUBLICGUILDANNOUNCEMENT
		15.	RTCSTATUSPOPOUT
		16.	PHONE-/EMAILVALIDATION
		17.	QUICKSELECTPOPOUT
		18.	WARNINGPOPOUT
		19.	ACTIVETHREADLISTPOPOUT
	15.	GENERAL
		1.	TEXT
		2.	BUTTONS
		3.	INPUTS
		4.	SEARCHBARS
		5.	TAGS
		6.	ICONS
		7.	SCROLLBARS
		8.	NOTIFICATIONBAR
		9.	TOOLTIPS
	16.	BDSUPPORT
	17.	POWERCORDSUPPORT
	18.	PLUGINSUPPORT
		1.	BDFDB
		2.	DATEVIEWER
		3.	MEMBERCOUNT
		4.	LINENUMBERS
		5.	PERMISSIONVIEWER
		6.	DIRECTDOWNLOAD
		7.	BETTERFORMATINGREDUX
		8.	CHANNELHISTORY
		9.	CHANNELTABS
		10.	TYPINGINDICATOR
		11.	BADGESEVERYWHERE
	19.	UPDATENOTICE
	20.	WATERMARK
*/


/* ~~~~		1.		TRANSPARENCY					~~~~ */

body,														/* body														*/
#app-mount .app-3xd6d0,										/* app					container							*/
#app-mount .app-2CXKsg,										/* app					inner								*/
#app-mount .loading-1yrGTe,									/* app					i18n loading						*/
#app-mount .wrapper-3AZUiP,									/* app					errorscreen							*/
#app-mount .bg-1QIAus,										/* app					background							*/
#app-mount .layer-86YKbF,									/* layer				container							*/
#app-mount .container-2o3qEW,								/* layer				container							*/
#app-mount .container-1NXEtd,								/* channels				inner								*/
#app-mount .privateChannels-oVe7HL,							/* dmchannels												*/
#app-mount .panels-3wFtMD > *,								/* account/voice		inner								*/
#app-mount .chat-2ZfjoI,									/* chat					container							*/
#app-mount .container-3XgAHv,								/* chat					thread sidebar						*/
#app-mount .wrapper-3HVHpV,									/* chat					messages loading					*/
#app-mount .noChannel-Z1DQK7,								/* nochannel												*/
#app-mount .members-3WRCEx,									/* members													*/
#app-mount .members-3WRCEx > div,							/* members				content								*/
#app-mount .content-3_h0XI,									/* unavailable												*/
#app-mount .container-2cd8Mz,								/* peoples													*/
#app-mount .container-1oAagU,								/* peoples				activity list						*/
#app-mount .applicationStore-2nk7Lo,						/* nitro													*/
#app-mount .pageWrapper-2PwDoS,								/* guilddiscovery											*/
#app-mount .pageWrapper-1x6lGh,								/* unihub													*/
#app-mount .scrollerBase-_bVAAt,							/* scroller													*/
#app-mount .scroller-2FKFPG,								/* scroller old												*/
#app-mount .standardSidebarView-E9Pc3j,						/* settings													*/
#app-mount .contentRegion-3HkfJJ {							/* settings				content								*/
	background: transparent;
}

#app-mount .scroller-hE2gWq {								/* peoples				activity scroller					*/
	border: none;
}

#app-mount .sidebarRegion-1VBisG,							/* settings				sidebar								*/
#app-mount .sidebar-_0OpfR {								/* sidebarlist			sidebar								*/
	background-color: rgba(var(--transparencycolor), calc(0.2 * (var(--transparencyalpha) / (var(--transparencyalpha) + 0.00000000000000000000001))));
}

#app-mount {												/* app-mount												*/
	background-color: rgba(var(--transparencycolor), var(--transparencyalpha));
}
#app-mount .wrapper-1_HaEi {								/* guilds				container							*/
	background-color: rgba(var(--transparencycolor), calc(var(--guildchanneltransparency) * 2));
}
#app-mount .sidebar-1tnWFu {								/* channels				container							*/
	background-color: rgba(var(--transparencycolor), var(--guildchanneltransparency));
}
#app-mount .panels-3wFtMD {									/* account/voice		container							*/
	background-color: rgba(var(--transparencycolor), calc(var(--guildchanneltransparency) / 1.5));
}
#app-mount .container-ZMc96U.themed-Hp1KC_ {				/* channelheader		container							*/
	background-color: rgba(var(--transparencycolor), var(--guildchanneltransparency));
}
#app-mount .membersWrap-3NUR2t {							/* members				container							*/
	background-color: rgba(var(--transparencycolor), var(--memberlisttransparency));
}
#app-mount .tabBar-fg4VK9 {									/* members				tabbar								*/
	background-color: rgba(var(--transparencycolor), var(--memberlisttransparency));
}
#app-mount .nowPlayingColumn-1eCBCN {						/* peoples				now playing							*/
	background-color: rgba(var(--transparencycolor), var(--memberlisttransparency));
}

#app-mount .image-35kDIs {									/* app					errorscreen image					*/
	background-image: url(https://discord.com/assets/e9baf4b505eb54129f832556ea16538e.svg);
	opacity: 0.6;
}


/* ~~~~		2.		BACKGROUND						~~~~ */

body::before,
body::after {
	content: "";
	position: fixed;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	pointer-events: none;
	z-index: -1;
}
body::before {
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
}
body::after {
	backdrop-filter: blur(var(--backgroundblur));
}
.layer-86YKbF {
	z-index: 1000;
}
.container-2RRFHK::before,
.layer-86YKbF ~ .layer-86YKbF::before,
.root-2zfUH6::before,
.container-2RRFHK::after,
.layer-86YKbF ~ .layer-86YKbF::after,
.root-2zfUH6::after {
	content: "";
	position: absolute;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	pointer-events: none;
	z-index: -1;
}
.container-2RRFHK::before,
.layer-86YKbF ~ .layer-86YKbF::before,
.root-2zfUH6::before {
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
}
.container-2RRFHK::after,
.layer-86YKbF ~ .layer-86YKbF::after,
.root-2zfUH6::after {
	background-color: rgba(var(--transparencycolor), var(--transparencyalpha));
	backdrop-filter: blur(var(--backgroundblur));
}
.uploadArea-2Nu_Vc,
.backdrop-1BR_bn,
.backdrop-2ByYRN {
	background: transparent !important;
	opacity: 1 !important;
	animation: none !important;
}
.uploadArea-2Nu_Vc::before,
.backdrop-1BR_bn::before,
.backdrop-2ByYRN::before,
.uploadArea-2Nu_Vc::after,
.backdrop-1BR_bn::after,
.backdrop-2ByYRN::after {
	content: "";
	position: absolute;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	pointer-events: none;
	z-index: -2;
}
.uploadArea-2Nu_Vc::before,
.backdrop-1BR_bn::before,
.backdrop-2ByYRN::before {
	background: var(--backdrop) var(--backdropposition)/var(--backdropsize);
	background-attachment: fixed;
}
.uploadArea-2Nu_Vc::after,
.backdrop-1BR_bn::after,
.backdrop-2ByYRN::after {
	backdrop-filter: blur(var(--backdropblur));
}
.withLayer-2VVmpp {
	z-index: -1;
}


/* ~~~~		3.		TITLEBAR						~~~~ */

.titleBar-1it3bQ {
	z-index: 5001;
}
.titleBar-1it3bQ::after {
	content: "";
	pointer-events: none;
	position: absolute;
	z-index: -1;
	top: 0;
	left: 0;
	width: 100%;
	background-color: rgba(var(--transparencycolor), calc(0.1 + var(--guildchanneltransparency) * 2));
}
.titleBar-1it3bQ:not(.typeMacOS-3V4xXE)::after {
	height: 22px;
}
.titleBar-1it3bQ.typeMacOS-3V4xXE::after {
	height: 28px;
	width: calc(100% - 4px);
	margin: 2px;
	border-radius: 5px;
}
.titleBar-1it3bQ.typeMacOS-3V4xXE,
.titleBar-1it3bQ.typeMacOS-3V4xXE .macButtons-eIdy0e {
	width: 72px;
}
.titleBar-1it3bQ.typeMacOS-3V4xXE.typeMacOSWithFrame-1XEpN7 .macButtons-eIdy0e {
	margin-top: 0;
	margin-right: 0;
}
.platform-osx .wrapper-1_HaEi {
	margin-top: 0;
	padding-top: 32px;
}
.platform-osx .standardSidebarView-E9Pc3j::before {
	left: 72px;
}
.winButtonMinMax-3RsPUg:hover {
	background-color: rgba(var(--transparencycolor), .2);
}


/* ~~~~		4.		GUILDLIST						~~~~ */

.childWrapper-1j_1ub,										/* homebutton/acronym	innerwrap							*/
#bd-pub-button {											/* publicbutton			innerwrap							*/
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--text-normal);
	font-weight: 500;
}
.wrapper-3kah-n:hover .childWrapper-1j_1ub,
.wrapper-3kah-n.selected-1Drb7Z .childWrapper-1j_1ub,
#bd-pub-button:hover {
	text-shadow: 1px 1px var(--textshadow);
}
.wrapper-3kah-n rect[fill] {
	fill: rgba(var(--transparencycolor), .3);
}
.noIcon-3gSX9V {											/* acronym				minicontainer						*/
	background-color: rgba(var(--transparencycolor), .3);
}

.circleIconButton-1QV--U {									/* guildadd/discovery	innerwrap							*/
	background-color: rgba(var(--transparencycolor), .3);
}

.guildIconUnavailable-3IYARS,								/* guilderror			miniicon							*/
.guildsError-YJjW3A {										/* guilderror			innerwrap							*/
	background-color: rgba(var(--dangercolor)),.3);
}

.dragInner-Oq_toX {											/* dragplaceholder											*/
	background-color: rgba(var(--transparencycolor), .3);
}

.wrapper-38slSD {											/* folder				outerwrap							*/
	margin-bottom: 8px;
}
.folder-1hbNCn {											/* folder				iconwrap							*/
	background-color: rgba(var(--transparencycolor), .2);
}
.folder-1hbNCn.hover-qTxTR_ {
	background-color: rgba(var(--transparencycolor), .4);
}
.expandedFolderBackground-1kSAf6 {							/* folder				background							*/
	background-color: rgba(var(--transparencycolor), .2);
	border-radius: 15px 15px 24px 24px;
	top: 0;
	bottom: 0;
	margin-bottom: 8px;
	transition: border-radius 3s ease, background-color 1s ease;
}
.expandedFolderBackground-1kSAf6.hover-qTxTR_ {
	background-color: rgba(var(--transparencycolor), .4);
}

.wrapper-1_HaEi .wrapper-38slSD [role="group"] {			/* folder				guildwrap							*/
	margin-bottom: -8px;
}
.wrapper-1_HaEi .wrapper-38slSD [role="group"] .listItem-GuPuDH:last-child {
	margin-bottom: 0;
}

.bar-2eAyLE {												/* guild/channelbar		inner								*/
	box-shadow: 0 2px 6px rgba(var(--transparencycolor), .24);
}
.bar-2eAyLE:not(.mention-3XBnnZ) {
	background-color: transparent;
	overflow: hidden;
}
.bar-2eAyLE:not(.mention-3XBnnZ)::before,
.bar-2eAyLE:not(.mention-3XBnnZ)::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	pointer-events: none;
	z-index: -1;
}
.bar-2eAyLE:not(.mention-3XBnnZ)::before {
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
}
.bar-2eAyLE:not(.mention-3XBnnZ)::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.1));
	backdrop-filter: blur(var(--backgroundblur));
}
.sidebar-1tnWFu .bar-2eAyLE:not(.mention-3XBnnZ)::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + var(--guildchanneltransparency) * 0.85 + 0.1));
}
.wrapper-1_HaEi .bar-2eAyLE:not(.mention-3XBnnZ)::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + var(--guildchanneltransparency) * 1.9 + 0.1));
}


/* ~~~~		5.		CHANNELLIST						~~~~ */

#app-mount .sidebar-1tnWFu {								/* channels				container							*/
	border-radius: 0;
}

/* ----		5.1.	GUILDHEADER						---- */

.container-1-ERn5 .animatedContainer-2laTjx {				/* banner				wrap								*/
	background: none;
	box-shadow: none;
}
.bannerImage-1jOskm {										/* banner				image								*/
	-webkit-mask: linear-gradient(rgba(0,0,0,0.9) 70%, rgba(0,0,0,0) 100%);
}
.bannerImage-1jOskm::before {
	display: none;
}

.header-3OsQeK,												/* header				inner								*/
.searchBar-3TnChZ {											/* header				searchbar							*/
	box-shadow: 0 1px 0 rgba(var(--transparencycolor), .2), 0 1.5px 0 rgba(var(--transparencycolor), .05), 0 2px 0 rgba(var(--transparencycolor), .05);
}
.searchBar-3TnChZ .searchBarComponent-3N7dCG {				/* header				searchbarinner						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.clickable-vvKY2q:not(.hasBanner-2IrYih) .header-3OsQeK:hover,
.selected-1GtAC5:not(.hasBanner-2IrYih) .header-3OsQeK {
	background-color: rgba(var(--transparencycolor), .2);
}

.container-3O_wAf,
.channelNotice-tO6Tus {										/* notice				container							*/
	box-shadow: inset 0 -1px 0 rgba(var(--transparencycolor), .3);
}
.container-3O_wAf,
.channelNotice-tO6Tus.invite-OjTXrW,
.channelNotice-tO6Tus.guildMFAWarning-3GEzs8,
.channelNotice-tO6Tus.maxMembersCount-3E4zND,
.channelNotice-3DDmsB,
#app-mount .channelNotice-3hkOiI {
	background: transparent;
}
.channelNotice-tO6Tus.invite-OjTXrW::before {
	opacity: 0.6;
	background: url(https://discord.com/assets/bf625d222187f542b9d7179109422e2c.svg) center 20px no-repeat;
}
.channelNotice-tO6Tus.guildMFAWarning-3GEzs8::before {
	opacity: 0.6;
	background: url(https://discord.com/assets/916a384814e3bbd2a84e2a1b352a17c3.svg) center 20px no-repeat;
}
.channelNotice-tO6Tus.quickswitcher-35bYg4::before {
	opacity: 0.6;
}
.channelNotice-tO6Tus.maxMembersCount-3E4zND::before {
	opacity: 0.6;
	background: url(https://discord.com/assets/01f60394adffda20dc7270a1e3c727df.svg) center 16px no-repeat;
}
.channelNotice-3DDmsB::before {
	opacity: 0.6;
	background: url(https://discord.com/assets/1858873f28bdc62dfb3a1f4b67d459bf.svg) center top 20px/153px no-repeat;
}
#app-mount .channelNotice-3hkOiI::before {
	opacity: 0.6;
	background: url(https://discord.com/assets/7065587bd42fd829925bf6aa4b36f5e2.svg) center top 22px/220px no-repeat;
}

/* ----		5.2.	CHANNELS						---- */

.wrapper-NhbLHG:hover .content-1gYQeQ {						/* channel				content								*/
	background-color: rgba(var(--transparencycolor), .2);
}
.modeSelected-3DmyhH .content-1gYQeQ,
.modeSelected-3DmyhH:hover .content-1gYQeQ {
	background-color: rgb(var(--accentcolor));
	text-shadow: 1px 1px var(--textshadow);
}
.modeSelected-3DmyhH .content-1gYQeQ svg,
.modeSelected-3DmyhH:hover .content-1gYQeQ svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}

.icon-2W8DHg {												/* channel				icon								*/
	color: var(--channels-default);
}
.modeMuted-2T4MDZ .icon-2W8DHg {
	color: var(--interactive-muted);
}
.modeMuted-2T4MDZ:hover .icon-2W8DHg,
.wrapper-NhbLHG:hover .icon-2W8DHg {
	color: var(--interactive-hover);
}
.modeConnected-NrO4cP .icon-2W8DHg,
.modeConnected-NrO4cP:hover .icon-2W8DHg,
.modeSelected-3DmyhH .icon-2W8DHg,
.modeSelected-3DmyhH:hover .icon-2W8DHg,
.modeUnread-3Cxepe .icon-2W8DHg,
.modeUnread-3Cxepe:hover .icon-2W8DHg,
.notInteractive-2tFrlE.modeConnected-NrO4cP .icon-2W8DHg,
.notInteractive-2tFrlE.modeSelected-3DmyhH .icon-2W8DHg {
	color: var(--interactive-active);
}
.modeConnected-NrO4cP .subtitle-3PyFgf,						/* channel				subtitle							*/
.modeConnected-NrO4cP:hover .subtitle-3PyFgf,
.modeSelected-3DmyhH .subtitle-3PyFgf,
.modeSelected-3DmyhH:hover .subtitle-3PyFgf,
.modeUnread-3Cxepe .subtitle-3PyFgf,
.modeUnread-3Cxepe:hover .subtitle-3PyFgf,
.notInteractive-2tFrlE.modeConnected-NrO4cP .subtitle-3PyFgf,
.notInteractive-2tFrlE.modeSelected-3DmyhH .subtitle-3PyFgf {
	color: var(--interactive-normal);
}
.spine-29OFwR {												/* channel				thread spine						*/
	color: var(--channels-default);
}

.wrapper-2fEmwW {											/* voicechat			limit								*/
	background-color: rgba(var(--transparencycolor), .15);
}
.wrapper-2fEmwW .users-2JoyGL {
	background-color: transparent;
}
.wrapper-2fEmwW .total-1c5KCN {
	background-color: rgba(var(--transparencycolor), .3);
}
.wrapper-2fEmwW .total-1c5KCN::after {
	border-right-color: rgba(var(--transparencycolor), .3);
}

.listDefault-2F-w65 .clickable-1ctZ-H:hover .content-1Tgc42 {
	background-color: rgba(var(--transparencycolor), .2);
}

/* ----		5.3.	DMCHANNELS						---- */

.channel-1Shao0:hover .layout-1qmrhw {						/* dmchannel/page		inner							*/
	background-color: rgba(var(--transparencycolor), .2);
}
.selected-1-Z6gm.channel-1Shao0 .layout-1qmrhw {
	background-color: rgb(var(--accentcolor));
	text-shadow: 1px 1px var(--textshadow);
}
.selected-1-Z6gm.channel-1Shao0 .layout-1qmrhw svg:not(.svg-2azL_l) {
	filter: drop-shadow(1px 1px var(--textshadow));
}

.empty-yQo7LQ {												/* loadingplaceholders										*/
	fill: rgba(var(--transparencycolor), .4);
}

/* ----		5.4.	ACCOUNT/VOICE/GOLIVE			---- */

.panels-3wFtMD > *,											/* account/voice		inner								*/
.panels-3wFtMD .wrapper-3Hk9OB > * {						/* account/voice		inner								*/
	border: none;
}
.panels-3wFtMD > *:not(:empty) ~ *:not(:empty) {
	border-top: 1px solid rgba(var(--transparencycolor), .2);
}

.button-12Fmur.enabled-9OeuTA {								/* account/voice		panel button						*/
	opacity: 0.7;
}
.button-12Fmur.enabled-9OeuTA:hover {
	opacity: 1;
	background-color: rgb(var(--accentcolor));
}
.button-12Fmur.enabled-9OeuTA:hover svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}
.button-1EGGcP.buttonColor-3bP3fX {
	background-color: rgba(var(--transparencycolor), .2);
}
.button-1EGGcP.buttonColor-3bP3fX:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
.button-1EGGcP.buttonColor-3bP3fX.buttonActive-Uc1jHx,
.button-1EGGcP.buttonColor-3bP3fX.buttonActive-Uc1jHx:hover {
	background-color: rgb(var(--accentcolor));
	text-shadow: 1px 1px var(--textshadow);
}
.button-1EGGcP.buttonColor-3bP3fX.buttonActive-Uc1jHx svg,
.button-1EGGcP.buttonColor-3bP3fX.buttonActive-Uc1jHx:hover svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}


/* ~~~~		6.		CHAT							~~~~ */

.chat-2ZfjoI.threadSidebarOpen-1LSXvU {
	border-radius: 0;
}
.chat-2ZfjoI.threadSidebarOpen-1LSXvU .content-1jQy2l::after {
	content: "";
	display: block;
	position: static;
	min-width: 408px;
	width: 29vw;
}
@media (max-width: 1150px) {
	.chat-2ZfjoI.threadSidebarOpen-1LSXvU .content-1jQy2l::after {
		display: none;
	}
}

/* ----		6.1.	CHANNELHEADER					---- */

.container-ZMc96U.themed-Hp1KC_ {							/* header				themedcontainer						*/
	box-shadow: 0 1px 0 rgba(var(--transparencycolor), .2), 0 1.5px 0 rgba(var(--transparencycolor), .05), 0 2px 0 rgba(var(--transparencycolor), .05);
}

.input-1nrc5P:focus {										/* header				dmchannelinput						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.input-1nrc5P:focus,
.outer-1KB3kA:hover .input-1nrc5P {
	box-shadow: inset 0 0 0 1px rgba(var(--transparencycolor), .2);
}
.children-3xh0VB::after {									/* header				topicgradient						*/
	display: none;
}

.akaBadge-3i7V3p {											/* header				aka									*/
	background-color: rgba(var(--transparencycolor), .3);
}

.badge-2qGa_k::after {										/* header				iconbadge red dot					*/
	border: none;
}

.searchBar-zdmu7v {											/* header				searchbar							*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .public-DraftEditorPlaceholder-root {
	color: rgb(var(--textdarker));
}
#app-mount .public-DraftEditorPlaceholder-hasFocus {
	color: var(--header-secondary);
}
#app-mount .searchFilter-2UfsDk,
#app-mount .searchAnswer-23w-CH {
	background-color: rgb(var(--accentcolor));
	text-shadow: 1px 1px var(--textshadow);
}

/* ----		6.2.	MESSAGES						---- */

.emptyChannelIcon-1YdEz2 {									/* welcomemessage		empty channelicon					*/
	background-color: rgba(var(--transparencycolor), .4);
}
.card-1yV8cG {												/* welcomemessage		first steps card					*/
	background-color: rgba(var(--transparencycolor), .3);
}
.card-1yV8cG:hover {
	background-color: rgba(var(--transparencycolor), .5);
}

.button-1kija8:hover {										/* welcomemessage		edit channel						*/
	background-color: rgb(var(--accentcolor));
	color: var(--interactive-active);
	text-shadow: 1px 1px var(--textshadow);
}

#app-mount .role-23oyrw {									/* welcomemessage		role								*/
	background: transparent;
	border-color: rgba(var(--textbrighter), .6);
	border-radius: 5px;
	height: 22px;
	padding: 0 5px;
	position: relative;
}
#app-mount .role-23oyrw[style*="border-color: rgba(185, 187, 190, .6)"] {
	border-color: rgba(var(--textbrighter), .6) !important;
}
#app-mount .role-23oyrw .roleColor-3cA0as {					/* welcomemessage		rolecircle							*/
	position: absolute;
	background-color: var(--text-normal);
	border-radius: 3px;
	opacity: 0.5;
	height: 100%;
	width: 100%;
	margin: 0;
	left: 0;
	top: 0;
	z-index: -1;
}
#app-mount .role-23oyrw:hover .roleColor-3cA0as {
	opacity: 0.8;
}
#app-mount .role-23oyrw .roleColor-3cA0as[style*="background-color: rgb(185, 187, 190)"] {
	background-color: var(--text-normal) !important;
}

.divider-2rZFJK.hasContent-31hcsn {							/* divider				hascontent							*/
	border-width: calc(1px * (1 - var(--usechatbubbles)));
}
.divider-2rZFJK.hasContent-31hcsn::before {
	content: "";
	position: absolute;
	top: -0.6rem;
	bottom: -0.6rem;
	right: -0.2rem;
	left: 0;
	background: rgba(var(--transparencycolor), calc(var(--messagetransparency) * 0.5));
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.content-3spvdd {											/* divider				content								*/
	position: absolute;
	background-color: transparent;
	padding: 2px 8px;
	width: unset;
}
.content-3spvdd::before,
.content-3spvdd::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	pointer-events: none;
	opacity: calc(1 - var(--usechatbubbles));
	z-index: -1;
}
.content-3spvdd::before {
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
}
.content-3spvdd::after {
	background-color: rgba(var(--transparencycolor), var(--transparencyalpha));
	backdrop-filter: blur(var(--backgroundblur));
}
.unreadPill-3nEWYM {										/* divider				unreadpill							*/
	border-radius: calc(4px * var(--usechatbubbles)) 4px 4px calc(4px * var(--usechatbubbles));
	padding-left: calc(4px * var(--usechatbubbles) + 1px * (1 - var(--usechatbubbles)));
}
.unreadPillCap-2-iI4h {										/* divider				unreadpillcap						*/
	opacity: calc(1 - var(--usechatbubbles));
}

.hasMore-2mIMwb:hover {
	background-color: rgba(var(--transparencycolor), .2);
}
.jumpToPresentBar-1cEnH0 {									/* bar					jumptopresent						*/
	background-color: transparent;
	overflow: hidden;
	opacity: 1;
}
.jumpToPresentBar-1cEnH0::before,
.jumpToPresentBar-1cEnH0::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	pointer-events: none;
	z-index: -1;
}
.jumpToPresentBar-1cEnH0::before {
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
}
.jumpToPresentBar-1cEnH0::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	backdrop-filter: blur(var(--backgroundblur));
}

/* ====		6.2.1.	MESSAGE							==== */

#app-mount .message-G6O-Wv {								/* message				confirm modal						*/
	background-color: rgba(var(--transparencycolor), .2);
	box-shadow: none;
}
.message-2CShn3,											/* message				container							*/
.messagesWrapper-RpOMA3 .wrapper-30-Nkg,					/* message				upload placeholder					*/
.wrapper-15CKyy,											/* message				loading 							*/
.message-3g3FYR,											/* message				mention popout						*/
.message-372Ods,											/* message				inbox popout						*/
.message-G6O-Wv .wrapper-30-Nkg,							/* message				settings preview					*/
.messageGroupCozy-3v_RqN,									/* message				pin popout							*/
.message-24k8JL .wrapper-30-Nkg {							/* message				searchpage							*/
	background-color: rgba(var(--transparencycolor), var(--messagetransparency)) !important;
	contain: unset;
}
.message-24k8JL .wrapper-30-Nkg {							/* message				searchpage							*/
	background-color: rgba(var(--transparencycolor), calc(var(--messagetransparency) * 0.8)) !important;
}
.message-2CShn3.selected-2LX7Jy,
.mouse-mode .message-2CShn3:hover,
.mouse-mode.full-motion .message-2CShn3:hover,
.mouse-mode .wrapper-15CKyy:hover,
.mouse-mode.full-motion .wrapper-15CKyy:hover {
	background-color: rgba(var(--transparencycolor), calc(var(--messagetransparency) * 1.2 * var(--usechatbubbles) + 0.3 * (1 - var(--usechatbubbles)))) !important;
}
.backgroundFlash-1X5jVs .message-2CShn3 {					/* message				jump flash							*/
	position: relative;
}
.backgroundFlash-1X5jVs .message-2CShn3::before {
	content: "";
	position: absolute;
	background: var(--message-background-flash, transparent);
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	z-index: 1;
	pointer-events: none;
}
.backgroundFlash-1X5jVs .cozyMessage-1DWF9U::before {
	left: calc(-80px * var(--usechatbubbles));
}
.message-2CShn3.ephemeral-2nDdnn,							/* message				localbot							*/
.message-2CShn3.replying-eZ7p5z {							/* message				replying							*/
	background-image: linear-gradient(rgba(var(--accentcolor), calc(0.2 * (1 - var(--usechatbubbles)))), rgba(var(--accentcolor), calc(0.2 * (1 - var(--usechatbubbles)))));
}
.message-2CShn3.mentioned-Tre-dv {							/* message				mentioned							*/
	background-image: linear-gradient(rgba(var(--mentioncolor), calc(0.2 * (1 - var(--usechatbubbles)))), rgba(var(--accentcolor), calc(0.2 * (1 - var(--usechatbubbles)))));
}
.message-2CShn3.ephemeral-2nDdnn::before,
.message-2CShn3.replying-eZ7p5z::before {
	background-color: rgb(var(--accentcolor));
}
.message-2CShn3.mentioned-Tre-dv::before {
	background-color: rgb(var(--mentioncolor));
}
.message-2CShn3.mentioned-Tre-dv .contents-2MsGLg .messageContent-2t3eCI {
	border-radius: 3px;
	background-color: rgba(var(--mentioncolor), calc(0.3 * var(--usechatbubbles)));
}
#app-mount .avatar-2e8lTP,									/* message				container avatar					*/
#app-mount .avatar-l9Txm5 {									/* message				loading avatar						*/
	position: absolute;
	top: 2px;
	left: calc(-70px * var(--usechatbubbles) + 16px);
}
#app-mount .repliedMessage-3Z6XBG ~ * .avatar-2e8lTP {
	top: 24px;
}
.container-3FojY8 .avatar-2e8lTP {
	left: calc(-10px * var(--usechatbubbles));
}

#app-mount .replyBadge-LMm_Ic {								/* message				reply badge							*/
	background-color: rgba(var(--transparencycolor), .5);
}
#app-mount .spine-3OoQS_ {
	width: 0px;
	top: 20px;
	right: calc(1px * (-32 * var(--usechatbubbles) + -25 * (1 - var(--usechatbubbles))));
	left: unset;
	border: none;
}
#app-mount .compact-2Nkcau .spine-3OoQS_ {
	right: 0;
}
#app-mount .repliedMessage-3Z6XBG::before,					/* message				reply spine							*/
#app-mount .repliedMessage-3Z6XBG::after,
#app-mount .spine-3OoQS_::before,							/* message				command spine						*/
#app-mount .spine-3OoQS_::after {
	--avatar-size: 38px;
	--gutter: 16px;
	--spine-width: 2px;
	content: "";
	display: block;
	position: absolute;
	-webkit-box-sizing: border-box;
	box-sizing: border-box;
	top: 50%;
	right: unset;
	bottom: 0;
	left: calc(-1 * var(--avatar-size) - (6px * var(--usechatbubbles)));
	width: calc(var(--avatar-size) - 4px);
	margin: calc(-1 * var(--spine-width)/2) var(--reply-spacing) calc(.125rem - 4px) calc(-1 * var(--spine-width)/2);
	border-right: 0 solid var(--background-accent);
	border-left: var(--spine-width) solid var(--background-accent);
}
#app-mount .repliedMessage-3Z6XBG::before,
#app-mount .repliedMessage-3Z6XBG::after {
	border-top: var(--spine-width) solid var(--background-accent);
	border-bottom: 0 solid var(--background-accent);
	border-top-left-radius: 6px;
}
#app-mount .spine-3OoQS_::before,
#app-mount .spine-3OoQS_::after {
	border-top: 0 solid var(--background-accent);
	border-bottom: var(--spine-width) solid var(--background-accent);
	border-bottom-left-radius: 6px;
}
#app-mount .compact-2Nkcau .repliedMessage-3Z6XBG::before,
#app-mount .compact-2Nkcau .repliedMessage-3Z6XBG::after,
#app-mount .compact-2Nkcau .spine-3OoQS_::before,
#app-mount .compact-2Nkcau .spine-3OoQS_::after {
	--avatar-size: 20px;
	left: calc(-1 * var(--avatar-size));
}
#app-mount .repliedMessage-3Z6XBG::before,
#app-mount .spine-3OoQS_::before {
	border-color: rgba(var(--textbrighter), calc(0.3 * (1 - var(--usechatbubbles))));
}
#app-mount .repliedMessage-3Z6XBG::after,
#app-mount .spine-3OoQS_::after {
	border-color: rgba(var(--transparencycolor), calc(0.5 * var(--usechatbubbles)));
}
#app-mount .compact-2Nkcau .repliedMessage-3Z6XBG::before,
#app-mount .compact-2Nkcau .spine-3OoQS_::before {
	border-color: rgba(var(--textbrighter), .3);
}
#app-mount .compact-2Nkcau .repliedMessage-3Z6XBG::after,
#app-mount .compact-2Nkcau .spine-3OoQS_::after {
	border-color: transparent;
}

#app-mount .cozy-VmLDNB.hasThread-3h-KJV::before,			/* message				thread spine						*/
#app-mount .cozy-VmLDNB.hasThread-3h-KJV::after,
#app-mount .compact-2Nkcau.hasThread-3h-KJV::after {
	--avatar-size: 38px;
	--gutter: 16px;
	--spine-width: 2px;
	content: "";
	display: block;
	position: absolute;
	top: 2rem;
	bottom: 29px;
	left: calc(var(--avatar-size) * (1 - var(--usechatbubbles)) - var(--avatar-size) * var(--usechatbubbles));
	width: calc(var(--avatar-size) - 10px + (4px * var(--usechatbubbles)));
	margin: calc(-1 * var(--spine-width)/2) var(--reply-spacing) calc(.125rem - 4px) calc(-1 * var(--spine-width)/2);
	border-top: 0 solid var(--background-accent);
	border-right: 0 solid var(--background-accent);
	border-bottom: var(--spine-width) solid var(--background-accent);
	border-left: var(--spine-width) solid var(--background-accent);
	border-bottom-left-radius: 8px;
}
#app-mount .cozy-VmLDNB.hasThread-3h-KJV::before {
	border-color: rgba(var(--textbrighter), calc(0.3 * (1 - var(--usechatbubbles))));
}
#app-mount .cozy-VmLDNB.hasThread-3h-KJV::after {
	border-color: rgba(var(--transparencycolor), calc(0.5 * var(--usechatbubbles)));
}
#app-mount .message-2CShn3.mentioned-Tre-dv.hasThread-3h-KJV::before {
	background-color: transparent;
}
#app-mount .compact-2Nkcau.hasThread-3h-KJV::after {
	left: calc(var(--avatar-size) + 11px);
	width: calc(var(--avatar-size) - 13px);
	border-color: rgba(var(--textbrighter), .3);
}
#app-mount .compact-2Nkcau.hasThread-3h-KJV .contents-2MsGLg::before {
	border-color: rgba(var(--textbrighter), .3);
}

.spine-2vt3pM {
	border-color: rgba(var(--textbrighter), .3);
}
.hasThread-3h-KJV .spine-2vt3pM {
	display: none;
}

.cozy-25GiHp.content-1UQFwj {								/* message				command content						*/
	background-color: rgba(var(--transparencycolor), .3);
}

.cozy-VmLDNB .header-2jRmjb::after,							/* message				container header					*/
.cozy-3hKWhq .header-35u4WP::after {						/* message				loading header						*/
	content: "";
	position: absolute;
	top: 12px;
	left: -32px;
	border: 10px solid transparent;
	border-right: 12px solid rgba(var(--transparencycolor), var(--messagetransparency));
}
.cozy-VmLDNB .container-3FojY8 .header-2jRmjb::after {
	left: 40px;
}
.messageGroupWrapper-1jf_7C .messageGroupCozy-3v_RqN .header-2jRmjb::after {
	top: 2px;
}
.message-24k8JL .wrapper-30-Nkg .header-2jRmjb::after {
	border-right-color: rgba(var(--transparencycolor), calc(var(--messagetransparency) * 0.8));
}
.cozy-VmLDNB .timestamp-p1Df1m.alt-1dvXnH {
	left: calc(-78px * var(--usechatbubbles));
}
.cozy-VmLDNB .iconContainer-2rPbqG {
	background-color: rgba(var(--transparencycolor), var(--messagetransparency));
	border-radius: 50%;
	left: calc(1px * (-58 * var(--usechatbubbles) + -48 * (1 - var(--usechatbubbles))));
	height: 25px !important;
	width: 25px !important;
	margin: unset;
	margin-right: 1rem;
	padding: 0;
}
.cozy-VmLDNB .blockedSystemMessage-3FmE9n .iconContainer-2rPbqG {
	background-color: transparent;
}
.cozy-VmLDNB .iconContainer-2rPbqG::after {
	content: "";
	position: absolute;
	top: 2px;
	left: 26px;
	border: 10px solid transparent;
	border-right: 12px solid rgba(var(--transparencycolor), var(--messagetransparency));
}
.cozy-VmLDNB .blockedSystemMessage-3FmE9n .iconContainer-2rPbqG::after {
	display: none;
}
.selected-2LX7Jy.message-2CShn3.cozy-VmLDNB .header-2jRmjb::after, 
.mouse-mode .message-2CShn3.cozy-VmLDNB:hover .header-2jRmjb::after,
.mouse-mode.full-motion .message-2CShn3.cozy-VmLDNB:hover .header-2jRmjb::after,
.mouse-mode .wrapper-15CKyy.cozy-3hKWhq:hover .header-35u4WP::after,
.mouse-mode.full-motion .wrapper-15CKyy.cozy-3hKWhq:hover .header-35u4WP::after,
.selected-2LX7Jy.message-2CShn3.cozy-VmLDNB .iconContainer-2rPbqG::after,
.mouse-mode .message-2CShn3.cozy-VmLDNB:hover .iconContainer-2rPbqG::after,
.mouse-mode.full-motion .message-2CShn3.cozy-VmLDNB:hover .iconContainer-2rPbqG::after {
	border-right-color: rgba(var(--transparencycolor), calc(var(--messagetransparency) * 1.2));
}
#app-mount .mentioned-Tre-dv.cozy-VmLDNB .header-2jRmjb::after {
	border-right-color: rgba(var(--mentioncolor), calc(var(--messagetransparency) * 100000000000000000000000000000));
}
#app-mount .ephemeral-2nDdnn.cozy-VmLDNB .header-2jRmjb::after,
#app-mount .replying-eZ7p5z.cozy-VmLDNB .header-2jRmjb::after {
	border-right-color: rgba(var(--accentcolor), calc(var(--messagetransparency) * 100000000000000000000000000000));
}
.message-3g3FYR,
.message-372Ods,
.zalgo-26OfGz .messageContent-2t3eCI,
.zalgo-26OfGz.cozy-VmLDNB .header-2jRmjb,
.wrapper-15CKyy,
.cozy-3hKWhq .header-35u4WP {
	overflow: visible;
}
.container-3FojY8 {
	padding: 0;
	overflow: visible;
}
#app-mount .cozyMessage-1DWF9U,								/* message				container cozy						*/
#app-mount .messagesWrapper-RpOMA3 .cozy-VmLDNB,			/* message				upload placeholder cozy				*/
#app-mount .cozy-3hKWhq {									/* message				loading cozy						*/
	margin-left: calc(80px * var(--usechatbubbles));
	padding-left: calc(1px * (10 * var(--usechatbubbles) + 72 * (1 - var(--usechatbubbles))));
}
#app-mount .wrapper-30-Nkg[data-list-item-id*="Uploader"] {
	margin-top: 1rem;
}
#app-mount .compact-QWkw9- {								/* message				loading compact						*/
	margin-top: .0625rem;
}
#app-mount .cozy-VmLDNB .header-2jRmjb,
#app-mount .cozy-VmLDNB .messageContent-2t3eCI,
#app-mount .cozy-3hKWhq .header-35u4WP {
	margin-left: 0;
	padding-left: 0;
}
.messageContainer-3VTXBC .wrapper-30-Nkg,
.messages-23can0 .wrapper-30-Nkg,
.message-G6O-Wv .wrapper-30-Nkg,
.messageGroupWrapper-1jf_7C .messageGroupCozy-3v_RqN,
.message-24k8JL .wrapper-30-Nkg {
	border-radius: 5px;
	margin-left: calc(60px * var(--usechatbubbles));
	padding-left: calc(1px * (10 * var(--usechatbubbles) + 72 * (1 - var(--usechatbubbles))));
}
.messages-23can0 .wrapper-30-Nkg {
	border-radius: 0;
}

.avatar-l9Txm5 {											/* message				loading avatar						*/
	background: rgba(var(--transparencycolor), .4);
	opacity: 1 !important;
}
.attachment-16cAbS,											/* message				loading attachment					*/
.blob-1uHjdp {												/* message				loading blob						*/
	background: rgb(var(--accentcolor));
}

.expanded-3lghlw {											/* message				expanded blocked					*/
	background-color: rgba(var(--transparencycolor), .2);
	border-radius: 5px 5px 0 5px;
	margin-bottom: .5625rem;
}

.reaction-2A2y9y {											/* message				reaction							*/
	background-color: rgba(var(--transparencycolor), .3);
	border: none;
}
.reaction-2A2y9y:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
.reaction-2A2y9y.reactionMe-3I9gFK {
	background-color: rgba(var(--accentcolor), .8);
}
.reaction-2A2y9y.reactionMe-3I9gFK:hover {
	background-color: rgb(var(--accentcolor));
}
.reaction-2A2y9y.reactionMe-3I9gFK .reactionCount-1zkLcN {
	color: #FFF;
	text-shadow: 1px 1px var(--textshadow);
}
.reaction-2A2y9y:hover {
	background-color: rgba(var(--transparencycolor), .4);
}

.wrapper-2vIMkT {											/* message				buttons								*/
	position: relative;
	background: transparent;
}
.wrapper-2vIMkT::before,
.wrapper-2vIMkT::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 4px;
	pointer-events: none;
	z-index: -1;
}
.wrapper-2vIMkT::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.wrapper-2vIMkT::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}
.button-3bklZh:hover {										/* message				button								*/
	background-color: rgba(var(--transparencycolor), .2);
}
.button-3bklZh.selected-69H4ua {
	background-color: rgba(var(--transparencycolor), .4);
}

.bumpBox-1Pp4td {											/* messageelement		publish box							*/
	background-color: rgba(var(--transparencycolor), .4);
}

.markup-eYLPri code {										/* messageelement		code								*/
	background-color: transparent;
	border-color: transparent;
}
.markup-eYLPri pre {										/* messageelement		pre									*/
	background-color: rgba(var(--transparencycolor), .4);
	border-color: rgba(var(--transparencycolor), .1);
}
.markup-eYLPri .inline,										/* messageelement		inline								*/
.after_inlineCode-WydEur,
.before_inlineCode-xn8Llh,
.inlineCode-2auMQi {
	background-color: rgba(var(--transparencycolor), .4);
}

.textContainer-36wgKK {										/* messageelement 		plain file text						*/
	background-color: rgba(var(--transparencycolor), .4);
	border-color: rgba(var(--transparencycolor), .1);
}
.footer-GXWBBp {											/* messageelement 		plain file footer					*/
	background-color: rgba(var(--transparencycolor), .4);
	border-color: rgba(var(--transparencycolor), .1);
}
.languageSelector-2e1IuO {									/* messageelement 		plain file popout					*/
	background-color: transparent;
	border: 1px solid rgba(var(--transparencycolor), .3);
	border-radius: 5px;
	box-shadow: 0px 1px 5px 0px rgba(var(--transparencycolor), .3);
	overflow: hidden;
}
.languageSelector-2e1IuO::before,
.languageSelector-2e1IuO::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.languageSelector-2e1IuO::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.languageSelector-2e1IuO::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}

#app-mount .spoilerText-27bIiA {							/* messageelement		spoiler								*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .spoilerText-27bIiA.hidden-3B-Rum {				/* messageelement		hiddenspoiler						*/
	background-color: rgba(var(--transparencycolor), .6);
}

.icon-JRJzJz[style*="/assets/5da4cdab01d4d89c593c48c62ae0d937.svg"] {		/* systemmessage			pinicon									*/
	-webkit-mask: url(https://discord.com/assets/5da4cdab01d4d89c593c48c62ae0d937.svg) center/cover no-repeat;
	background: var(--channels-default) !important;
}
.icon-JRJzJz[style*="/assets/d80d1fdc43a3c42134a31a39581160ac.svg"] {		/* systemmessage			missedcall								*/
	-webkit-mask: url(https://discord.com/assets/d80d1fdc43a3c42134a31a39581160ac.svg) center/cover no-repeat;
	background: var(--channels-default) !important;
}
.icon-JRJzJz[style*="/assets/b8029fe196b8f1382e90bbe81dab50dc.svg"] {		/* systemmessage			joincallicon							*/
	-webkit-mask: url(https://discord.com/assets/b8029fe196b8f1382e90bbe81dab50dc.svg) center/cover no-repeat;
	background: rgb(var(--accentcolor)) !important;
}
.icon-JRJzJz[style*="/assets/c30220457097b064286a8759a9b6c4af.svg"] {		/* systemmessage			recievecallicon							*/
	-webkit-mask: url(https://discord.com/assets/c30220457097b064286a8759a9b6c4af.svg) center/cover no-repeat;
	background: rgb(var(--accentcolor)) !important;
}

/* ====		6.2.2.	EMBEDS							==== */

#app-mount .embedFull-1HGV2S {								/* embed				wrapper								*/
	background-color: rgba(var(--transparencycolor), .3);
	border-left-color: rgb(var(--textdarkest));
}

#app-mount .attachment-1PZZB2 {								/* attachment			container							*/
	background-color: rgba(var(--transparencycolor), .3);
	border-color: rgba(var(--transparencycolor), .1);
	margin-left: 18px;
}
#app-mount .message-2CShn3 .attachment-1PZZB2 {
	margin-left: 0;
}
#app-mount .twitchSectionPlayButton-2RamGG {
	object-position: -999999px -999999px;
	background: rgba(var(--transparencycolor), .4) url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 32 32" fill="none"><path d="M12.3333 10.002V22.002L22.3333 16.002L12.3333 10.002Z" fill="rgb(185,187,190)"/></svg>');
	border-radius: 50%;
}
#app-mount .twitchSectionPlayButton-2RamGG:hover {
	background-color: rgba(var(--transparencycolor), .8);
}

#app-mount .wrapper-1FP9YQ {								/* attachment			videowrapper						*/
	background-color: rgba(var(--transparencycolor), .3);
}

/* ====		6.2.3.	NITROGIFT						==== */

#app-mount .tile-2mmK5T {									/* gift					container							*/
	background-color: rgba(var(--transparencycolor), .2);
	box-shadow: 0 0 0 rgba(var(--transparencycolor), .15);
}
#app-mount .tile-2mmK5T:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .title-oJa_A6 {									/* gift					title								*/
	color: var(--header-primary);
}
#app-mount .description-X8_53U {							/* gift					description							*/
	color: var(--header-primary);
}
#app-mount .tagline-3DhQWg {								/* gift					tagline								*/
	color: var(--header-secondary);
}

/* ====		6.2.4.	INVITE							==== */

#app-mount .wrapper-1HIH0j {								/* invite				container							*/
	background-color: rgba(var(--transparencycolor), .3);
	border-color: rgba(var(--transparencycolor), .1);
}
#app-mount .guildIconImage-74OdmM {							/* invite				icon								*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .guildName-3G4jq- {								/* invite				name								*/
	color: var(--header-primary);
}
#app-mount .guildDetail-3EJhW_ {							/* invite				details								*/
	color: var(--channels-default);
}

#app-mount .invite-3uuHYQ {									/* invite				group invite						*/
	background-color: rgba(var(--transparencycolor), .3);
	border-color: rgba(var(--transparencycolor), .1);
}
#app-mount .header-1Fx4D1 {
	color: rgb(var(--textdarker));
}
#app-mount .name-QjR4Jk,
#app-mount .partyStatus-2-VcyG {
	color: var(--header-primary);
}
#app-mount .moreUsers-3PdGZN {
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--header-secondary);
}
#app-mount .partyMemberEmpty-GtlQ_s {
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .helpIcon-24pk1Z {
	background-color: var(--header-primary);
}


/* ----		6.3.	TEXTAREA						---- */

.form-3gdLxP {
	padding-top: 0;
	margin-top: 0;
}
.form-3gdLxP {												/* textarea				form								*/
	background: rgba(var(--transparencycolor), var(--chatinputtransparency));
	margin-top: 0;
	padding-top: 8px;
	border-top-right-radius: calc(8px * (1 - (var(--memberlisttransparency) / (var(--memberlisttransparency) + 0.00000000000000000000001))));
	border-top-left-radius: calc(8px * (1 - (var(--guildchanneltransparency) / (var(--guildchanneltransparency) + 0.00000000000000000000001))));
}
.threadSidebarOpen-1LSXvU .form-3gdLxP {
	border-top-right-radius: 8px;
}
.form-3gdLxP::before {
	display: none;
}

.channelTextArea-1FufC0 {									/* textarea				channeltextarea						*/
	background-color: transparent;
	border-top-color: var(--background-modifier-accent);
}

.container-A2jo65 {											/* textarea				reply								*/
	background: rgba(var(--transparencycolor), .3);
	border: none;
	border-bottom: 1px solid var(--background-modifier-accent);
}

.scrollableContainer-15eg7h {								/* textarea				container							*/
	background-color: rgba(var(--transparencycolor), .3);
}

.sprite-2lxwfc {											/* textarea				emojibutton							*/
	transform: none !important;
}

.wrapper-2SplAX {											/* textarea				placeholder							*/
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--text-normal);
}

.toolbar-37BrJ5 {											/* textarea				formattoolbar						*/
	background-color: rgb(var(--accentcolor));
}
.toolbar-37BrJ5::before {
	border-top-color: rgb(var(--accentcolor));
}
.divider-3NY7PF {											/* textarea				formattoolbar divider				*/
	border-left-color: hsla(0, 0%,100%, .1);
}
.active-136ioF,												/* textarea				buttonactive						*/
.hover-3OQb9Y:hover {										/* textarea				buttonhover							*/
	background-color: hsla(0, 0%, 100%, .2);
}
.icon-3g7qdA {												/* textarea				buttonicon							*/
	color: #fff;
	opacity: .7;
}
.active-136ioF .icon-3g7qdA,
.hover-3OQb9Y:hover .icon-3g7qdA {
	color: #fff;
	opacity: 1;
}

#app-mount .pill-1HLSrc {									/* textarea				command query pill					*/
	background-color: rgba(var(--transparencycolor), .5);
	border-radius: 5px;
}

/* ----		6.4.	AUTOCOMPLETEMENU				---- */

#app-mount .autocomplete-3NRXG8 {							/* autocomplete			container							*/
	background-color: transparent;
	overflow: hidden;
}
#app-mount .autocomplete-3NRXG8::before,
#app-mount .autocomplete-3NRXG8::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
#app-mount .autocomplete-3NRXG8::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
#app-mount .autocomplete-3NRXG8::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}
.theme-brand .autocomplete-3NRXG8 {
	background: rgb(var(--accentcolor)) linear-gradient(rgba(var(--transparencycolor), .2), rgba(var(--transparencycolor), .2)) !important;
}
.theme-brand .autocomplete-3NRXG8::before,
.theme-brand .autocomplete-3NRXG8::after {
	display: none;
}
#app-mount .bar-AokMp3 {									/* autocomplete			command info						*/
	background-color: transparent;
}
#app-mount .container-23gRWx::after {
	box-shadow: inset 0 -7px 12px -7px rgba(var(--transparencycolor), .3);
}
#app-mount .header-JHwfVI {									/* autocomplete			header								*/
	box-shadow: 0 1px 0 0 rgba(var(--transparencycolor), .2), 0 1px 2px 0 rgba(var(--transparencycolor), .2);
}
#app-mount .selected-3H3-RC {								/* autocomplete			rowselected							*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .option-Tt7anD {									/* autocomplete			option								*/
	background-color: rgba(var(--transparencycolor), .5);
}

#app-mount .wrapper-3z7DuG {								/* autocomplete			categories							*/
	background-color: transparent;
}
#app-mount .selected-3B2w1z,								/* autocomplete			category selected					*/
#app-mount .selected-3B2w1z:hover {
	background-color: rgb(var(--accentcolor));
}
#app-mount .selected-3B2w1z svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}

#app-mount .searchSuggestion-1dxIOj:hover {					/* gifpicker			suggestions							*/
	text-shadow: 1px 1px var(--textshadow);
}

#app-mount .placeholder-2Mfkde {							/* gifpicker			result placeholder					*/
	background-color: rgba(var(--transparencycolor), .3);
}

/* ----		6.5.	MEMBERLIST						---- */

.member-2gU6Ar:hover .layout-1qmrhw {						/* member				inner								*/
	background-color: rgba(var(--transparencycolor), .2);
}
.selected-1-Z6gm.member-2gU6Ar .layout-1qmrhw {
	background-color: rgb(var(--accentcolor));
	text-shadow: 1px 1px var(--textshadow);
}
.selected-1-Z6gm.member-2gU6Ar .layout-1qmrhw svg:not(.svg-2azL_l) {
	filter: drop-shadow(1px 1px var(--textshadow));
}
.member-2gU6Ar.selected-1-Z6gm .premiumIcon-2IFPOX {
	color: var(--header-primary) !important;
}

.avatar-b5OQ1N::before {									/* emptyavatar												*/
	background-color: rgba(var(--transparencycolor), .3);
}

.memberGroupsPlaceholder-9tqX9V,							/* loadingplaceholders										*/
.placeholderAvatar-1qAcRZ,
.placeholderUsername-3iQi_D {
	background-color: rgba(var(--transparencycolor), .4);
}

/* ----		6.6.	SEARCHPAGE						---- */

.searchResultsWrap-5RVOkx {									/* searchpage			container							*/
	background-color: transparent;
}
.searchHeader-1r_ZSh {										/* searchpage			header								*/
	background-color: rgba(var(--transparencycolor), calc(var(--guildchanneltransparency) * 0.8));
	border-radius: 0 0 0 8px;
}
#app-mount .tab-2j5AEF.selected-2LAck8 {					/* searchpage			selected tab						*/
	background-color: rgb(var(--accentcolor));
	text-shadow: 1px 1px var(--textshadow);
}
.channelName-3w2Y3c {										/* searchpage			channelname							*/
	background-color: transparent;
}
.searchResult-O9NDji {										/* searchpage			searchresult						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.button-cfOvv- {											/* searchpage			jumpbutton							*/ 
	background-color: rgba(var(--transparencycolor), .4);
}
.button-cfOvv-:hover {
	background-color: rgb(var(--accentcolor));
	text-shadow: 1px 1px var(--textshadow);
}
.pageButton-1GMGeJ:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
.activeButton-LRWFC_ {
	text-shadow: 1px 1px var(--textshadow);
}

/* ----		6.7.	THREADS							---- */

.container-3XgAHv {											/* threadsidebar											*/
	position: absolute;
	top: 48px;
	right: 0;
	bottom: 0;
	border-radius: 0;
	z-index: 100;
}
.container-3XgAHv .container-ZMc96U {						/* threadsidebar		header								*/
	background-color: rgba(var(--transparencycolor), calc(var(--guildchanneltransparency) * 0.8));
	box-shadow: unset;
	border-radius: 0 0 0 8px;
}
.container-3XgAHv .form-3gdLxP {							/* threadsidebar		form								*/
	border-radius: 8px 0 0 0;
}
@media (max-width: 1150px) {
	.container-3XgAHv::before,
	.container-3XgAHv::after {
		content: "";
		position: absolute;
		top: 0;
		bottom: 0;
		right: 0;
		left: 0;
		pointer-events: none;
		z-index: -1;
	}
	.container-3XgAHv::before {
		background: var(--background) var(--backgroundposition)/var(--backgroundsize);
		background-attachment: fixed;
	}
	.container-3XgAHv::after {
		background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + var(--memberlisttransparency) * 0.85));
		backdrop-filter: blur(var(--backgroundblur));
	}
	.container-3XgAHv .container-ZMc96U {
		border-radius: 0;
	}
	.container-3XgAHv .form-3gdLxP {
		border-radius: 0;
	}
}

/* ----		6.8.	CALL							---- */

#app-mount .wrapper-3X0c60 {
	z-index: 1002;
}
#app-mount .root-1e2tfc {									/* popout				inner								*/
	background-color: transparent;
	border: none;
}
.root-1e2tfc::before,
.root-1e2tfc::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.root-1e2tfc::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.root-1e2tfc::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}

#app-mount .wrapper-1gVUIN {								/* call					voice wrapper					*/
	background-color: rgba(var(--transparencycolor), calc(var(--guildchanneltransparency) * 0.8));
}
#app-mount .root-22AK9z {									/* call					root							*/
	color: var(--header-primary);
}
.videoWrapper-3rtb_V {										/* call					video wrapper					*/
	background-color: rgba(var(--transparencycolor), .3);
}
.video-eAcneW {												/* call					video							*/
	background-color: transparent;
}
.tile-2TcwiO,												/* call					user video voicechannel			*/
.tile-2Dr6M1 {												/* call					user video dm					*/
	background-color: rgba(var(--transparencycolor), .3);
}
.gradientContainer-phMG8d {									/* call					gradientcontainer				*/
	display: none;
}
.participantsButton-1WBdFP {								/* call					participantsbutton				*/
	background-color: rgba(0, 0, 0, .3);
}
.participantsButton-1WBdFP:hover {
	background-color: rgba(0, 0, 0, .6);
}
.centerButton-1IShs7,
.colorable-3rVGna.primaryDark-2UJt1G {
	background-color: rgba(var(--transparencycolor), .5);
}
.centerButton-1IShs7:hover,
.colorable-3rVGna.primaryDark-2UJt1G:hover {
	background-color: rgb(var(--accentcolor));
}
.button-3Vyz67 {
	background-color: rgba(var(--transparencycolor), .4);
}
.button-3Vyz67:hover {
	background-color: rgba(var(--transparencycolor), .6);
}
.controlButton-2PMNom.leaveButton-2YnTyt {
	background-color: rgba(var(--dangercolor)),.5);
}
.controlButton-2PMNom.leaveButton-2YnTyt:hover {
	background-color: rgb(var(--dangercolor));
}
.regionSelectPopout-3sEzVB {
	width: 170px;
}

.container-cH6QoY {											/* call					podium wrapper					*/
	background-color: rgba(var(--transparencycolor), calc(var(--guildchanneltransparency) * 0.8));
}
.callContainer-BGIngG {										/* call					podium inner					*/
	background-color: transparent;
}
.scroller-35tvpe {											/* call					podium scroller					*/
	background-color: transparent;
}
.container-3r7mfc {											/* call					podium info						*/
	background-color: transparent;
}
.rowContainer-jDvyA4 {										/* call					podium row						*/
	background-color: transparent;
}
.participants-3hk3ND {										/* call					podium participants				*/
	background-color: transparent;
}
.tileContainer-Os085F:hover {								/* call					podium participant				*/
	background-color: rgb(var(--accentcolor));
}
.container-lqPArA {											/* call					podium requests					*/
	background-color: rgba(var(--transparencycolor), calc(var(--guildchanneltransparency) * 0.3));
}
.headerContainer-21E-jZ {									/* call					podium requests header			*/
	box-shadow: 0 1px 0 rgba(var(--transparencycolor), .2), 0 1.5px 0 rgba(var(--transparencycolor), .05), 0 2px 0 rgba(var(--transparencycolor), .05);
}

/* ----		6.9.	UNAVAILABLESCREEN				---- */

.category-2haXBH,											/* loadingplaceholders										*/
.channelIcon-1TvDoP,
.channelName-2wrHHc {
	background: rgba(var(--transparencycolor), .4);
}
.splashImage-3x240k {										/* screen				image								*/
	opacity: 0.7;
}


/* ~~~~		7.		PEOPLES							~~~~ */

.wrapper-1cBijl {											/* friendsadd			inputcontainer						*/
	background-color: rgba(var(--transparencycolor), .1);
	border-color: rgba(var(--transparencycolor), .3);
}
.wrapper-1cBijl:hover {
	border-color: rgb(var(--transparencycolor));
}

.peopleListItem-u6dGxF .actionButton-3-B2x-,				/* peoples				actionbutton						*/
.peopleListItem-u6dGxF .actionButton-3-B2x {				/* peoples				actionbutton						*/
	background-color: rgba(var(--transparencycolor), .1);
}
.peopleListItem-u6dGxF .actionButton-3-B2x-:hover,
.peopleListItem-u6dGxF .actionButton-3-B2x:hover {
	background-color: rgb(var(--accentcolor));
}
.peopleListItem-u6dGxF .actionButton-3-B2x-:hover svg,
.peopleListItem-u6dGxF .actionButton-3-B2x:hover svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}
.peopleListItem-u6dGxF.active-2UF8Zh,
.peopleListItem-u6dGxF:hover,
.peopleListItem-u6dGxF.active-2UF8Zh,
.peopleListItem-u6dGxF:hover {
	background-color: rgba(var(--transparencycolor), .3);
}
.peopleListItem-u6dGxF.active-2UF8Zh .actionButton-3-B2x-,
.peopleListItem-u6dGxF:hover .actionButton-3-B2x-,
.peopleListItem-u6dGxF.active-2UF8Zh .actionButton-3-B2x,
.peopleListItem-u6dGxF:hover .actionButton-3-B2x {
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .outer-2JOHae,									/* playing				card								*/
#app-mount .outer-2JOHae {									/* playing				card								*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .outer-2JOHae.active-1W_Gl9,
#app-mount .outer-2JOHae.interactive-2zD88a:hover,
#app-mount .outer-2JOHae.active-1W_Gl9,
#app-mount .outer-2JOHae.interactive-2zD88a:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .inset-SbsSFp,									/* playing				card inner							*/
#app-mount .inset-SbsSFp {									/* playing				card inner							*/
	background-color: rgba(var(--transparencycolor), .2);
}
.emptyCard-KDifrB {											/* playing				empty card							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .partyMemberOverflow-3G1oZz {
	background: rgba(var(--transparencycolor), .5);
}
#app-mount .partyMemberBackground-35PUxI,
#app-mount .partyMemberUnknown-3RMTbX {
	background-color: rgba(var(--transparencycolor), .5);
}
#app-mount .partyMemberUnknownIcon-3HapjE {
	color: var(--channels-default);
}
#app-mount .popout-3Zw0qN {									/* playing				popout								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 8px 16px 0 rgba(var(--transparencycolor), .3);
	overflow: hidden;
}
.popout-3Zw0qN::before,
.popout-3Zw0qN::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.popout-3Zw0qN::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.popout-3Zw0qN::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.3));
	backdrop-filter: blur(var(--popoutblur));
}
#app-mount .memberListItem-31QoHj:not(.popoutDisabled-2RK7MF):hover,
#app-mount .enabled-1t_Gxm:hover {
	background-color: rgba(var(--transparencycolor), .2);
}


/* ~~~~		7.		STORE/NITRO						~~~~ */

.gridItemBadge-1Se-Pu {
	text-shadow: 1px 1px var(--textshadow);
}

.marketingHeader-cnc4f7 {									/* marketingheader											*/
	background-color: rgba(var(--transparencycolor), .3);
}

.detailsBlock-FoDTGA {										/* billing 				details								*/
	background-color: rgba(var(--transparencycolor), .3);
}

#app-mount .categoryHeader-93jmyE,							/* categoryheader											*/
#app-mount .premiumApplicationsHeader-3K67Qe {
	border-color: var(--background-modifier-accent);
	color: var(--header-primary);
}

#app-mount .tier1Banner-LvpkWu {							/* tier1banner			container							*/
	background-color: rgba(var(--transparencycolor), .3);
	color: #fff;
}
.headerIcon-3bqya6 {										/* tier1banner			svgtitle							*/
	color: #fff;
}

.smallCarousel-20QIi8 {
	background-color: rgba(var(--transparencycolor), .3);
	border-radius: 5px;
}
#app-mount .item-g96i1Z {									/* gamepreview			previewitem							*/
	background-color: rgba(var(--transparencycolor), .3);
}
.arrow-3M4PD9 {												/* gamepreview			prev/nextarrow (big)				*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .themedPagination-3jclKS .arrow-2PTaaz {			/* gamepreview			prev/nextarrow (small)				*/
	color: var(--header-primary);
}
#app-mount .themedPagination-3jclKS .dot-1xabNQ {			/* gamepreview			itemdot (small)						*/
	background-color: var(--header-primary);
}

#app-mount .root-3mkK8X {									/* gameinfo				sectioncontainer					*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .header-13C7x6 {									/* gameinfo				sectionheader						*/
	color: var(--header-primary);
}
#app-mount .section-3Et6MX {								/* gameinfo				subsection							*/
	border-bottom-color: var(--background-modifier-accent);
}
#app-mount .playerOverflow-GbSZQs {
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--header-secondary);
}
#app-mount .description-hC8iQf {							/* gameinfo				subsectiondescription				*/
	color: var(--header-secondary);
}
#app-mount .description-hC8iQf strong,
#app-mount .username-pDGZS1 {								/* gameinfo				subsectionusername					*/
	color: var(--header-primary);
}
#app-mount .smallHeader--lYkq9 {							/* gameinfo				subsectionheader					*/
	color: var(--header-secondary);
}
#app-mount .text-3UzHA4 {									/* gameinfo				subsectiontext						*/
	color: var(--header-primary);
}
#app-mount .iconCircle-3CMTjB {
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .circle-1ceChx {
	color: var(--header-primary);
}

#app-mount .divider-3y7HAB {								/* section				divider								*/
	border-color: var(--background-modifier-accent);
}
#app-mount .blurb-btvBEJ {									/* section				description							*/
	color: var(--text-normal);
}
#app-mount .description-BzYBA2 {							/* section				subdescription						*/
	color: var(--header-secondary);
}

#app-mount .requirements-2IwVy6 {							/* requirements												*/
	color: var(--text-normal);
}
#app-mount .requirementKey-3Mlwzf {							/* requirements			key									*/
	color: rgb(var(--textdarker));
}
#app-mount .content-3N5BG9 {								/* requirements			rating								*/
	color: rgb(var(--textdarker));
}
#app-mount .content-26qlhD {								/* requirements			copyright							*/
	color: rgb(var(--textdarker));
}

#app-mount .bodySection-3iDdop {							/* sidebar				section								*/
	background-color: rgba(var(--transparencycolor), .2);
	border-top-color: var(--background-modifier-accent);
}
#app-mount .actionText-1Yglc4 {								/* sidebar				header								*/
	color: var(--text-normal);
}
#app-mount .purchaseUnitOperatingSystem-1OW7Kw {			/* sidebar				OSicon								*/
	color: rgb(var(--textdarkest));
}
#app-mount .price-2SHLzi,									/* sidebar				price								*/
#app-mount .listingPrice-3Byrq9 {
	color: var(--header-primary);
}
#app-mount .title-3cAMJ9 {									/* sidebar				subtitle							*/
	color: var(--header-primary);
}
#app-mount .skuNormal-213nY8 {								/* sidebar				pricerow							*/
	border-bottom-color: var(--background-modifier-accent);
}
#app-mount .name-aq9Dm0 {									/* sidebar				pricename							*/
	color: var(--header-secondary);
}
#app-mount .sku-3GRW_9:hover .name-aq9Dm0 {
	color: var(--header-primary);
}
#app-mount .price-1BMuA2 {									/* sidebar				priceamount							*/
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--header-primary);
}
#app-mount .label-29p9qC {									/* sidebar				label								*/
	color: rgb(var(--textdarker));
}
#app-mount .info-3k6QpS {									/* sidebar				labelinfo							*/
	color: var(--header-primary);
}

#app-mount .content-1W9-9i {								/* invitecard			container							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .name-22c6Wk {									/* invitecard			guildname							*/
	color: var(--header-secondary);
}
#app-mount .memberInfo-QIpngr {								/* invitecard			memberinfo							*/
	color: rgb(var(--textdarker));
}

.premiumSubscriptionAccountCredit-1UInYJ {					/* abonnements			abocard								*/
	background-color: rgba(var(--transparencycolor), .4);
}

#app-mount .row-2qQ--F {									/* features				row									*/
	background-color: rgba(var(--transparencycolor), .2);
	color: var(--header-secondary);
}
#app-mount .featureIcon-3GwsEQ {							/* features				featureicon							*/
	color: var(--header-secondary);
}
#app-mount .feature-2IUcBI {								/* features				feature								*/
	background-color: rgba(var(--transparencycolor), .4);
}
.featureImage-91H2fC {										/* features				image								*/
	opacity: 0.7;
}
.banner-WELp4M {											/* features				xbox promo							*/
	background-color: rgba(var(--transparencycolor), .4);
}


/* ~~~~		9.		LIBRARY							~~~~ */

.header-2EadGG {											/* library				table header						*/
	background-color: transparent;
	border-bottom-color: var(--background-modifier-accent);
	position: relative;
}
.header-2EadGG::before,
.header-2EadGG::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.header-2EadGG::before {
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
}
.header-2EadGG::after {
	background-color: rgba(var(--transparencycolor), .4);
	backdrop-filter: blur(var(--backgroundblur));
}

#app-mount .headerCellSorted-1bg4Lp {
	color: var(--header-primary);
}

.rowWrapperActive-nOO7R3 {
	background-color: rgba(var(--transparencycolor), .2);
}
.rowWrapper-N-4fji + .rowWrapper-N-4fji .row-1_1Nya {
	border-top-color: var(--background-modifier-accent);
}

#app-mount .rate-1lw2ml {
	color: var(--text-muted);
}
#app-mount .background-3laMJt {								/* library				usagebar							*/
	stroke: rgb(var(--transparencycolor), .5);
}
#app-mount .usageInfo-2CQ9c7 {								/* gamelibrary			usageinfo							*/
	color: var(--header-secondary);
}

#app-mount .installationPath-2PbaRC {						/* library				game row path						*/
	box-shadow: 0 1px 0 0 var(--background-accent);
}
#app-mount .rowTitle-2MoCno {								/* library				game row title						*/
	color: var(--text-normal);
}
#app-mount .rowBody-uWDd7Y {								/* library				game row body						*/
	color: var(--text-muted);
}
#app-mount .defaultLocationCheckbox-1Y3dSI {				/* library				location checkbox					*/
	color: var(--header-primary);
}
#app-mount .defaultIndicator-1AxErs {						/* library				location indicator					*/
	background-color: rgba(var(--transparencycolor), .5);
	color: var(--header-primary);
}

#app-mount .applicationName-1uqOrC {						/* library				application name					*/
	color: var(--header-primary);
}
#app-mount .applicationSubText-2SBEgj {						/* library				application subtext					*/
	color: var(--text-muted);
}

#app-mount .emptyWumpus-11kRB0 {							/* library				no games							*/
	background: url(https://discord.com/assets/131dcaaa628405e6d0ebee7708111c7a.svg);
	opacity: 0.6;
}


/* ~~~~		10.		DISCOVERY/UNIHUB				~~~~ */

.categoryItem-1QIroW:hover .itemInner-gPkiWb,				/* guilddiscovery		categoryitem						*/
.optionItem-2tdutc:hover .itemInner-3k3Sn6 {				/* unihub				categoryitem						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.categoryItem-1QIroW.selectedCategoryItem-FHKU_o .itemInner-gPkiWb,
.optionItem-2tdutc.selectedOptionItem-3v62YZ .itemInner-3k3Sn6 {
	background-color: rgb(var(--accentcolor));
	text-shadow: 1px 1px var(--textshadow);
}
.categoryItem-1QIroW.selectedCategoryItem-FHKU_o .itemInner-gPkiWb svg:not(.svg-2azL_l),
.optionItem-2tdutc.selectedOptionItem-3v62YZ .itemInner-3k3Sn6 svg:not(.svg-2azL_l) {
	filter: drop-shadow(1px 1px var(--textshadow));
}

#app-mount .pageWrapper-2PwDoS,								/* guilddiscovery		container							*/
#app-mount .pageWrapper-1x6lGh {							/* unihub				container							*/
	color: var(--header-primary);
}
#app-mount .pageWrapper-2PwDoS .searchBox-31Zv9h,			/* guilddiscovery		searchbox							*/
#app-mount .pageWrapper-1x6lGh .searchBox-3wTyE4 {			/* unihub				searchbox							*/
	background-color: #fff;
}
#app-mount .card-2TuZPZ,									/* guilddiscovery		card								*/
#app-mount .card-3N2v9t {									/* unihub				card								*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .iconMask-2fMR98,								/* guilddiscovery		iconmask							*/
#app-mount .iconMask-24Ybpm {								/* unihub				iconmask							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .card-2TuZPZ:hover,
#app-mount .iconMask-2fMR98:hover,
#app-mount .card-3N2v9t:hover,
#app-mount .iconMask-24Ybpm:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .cardPlaceholder-1E2FEs {						/* guildcard			placeholder							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .loading-3ozbwt {								/* guildcard			loading								*/
	background-color: rgba(var(--transparencycolor), .5);
}

#app-mount .addEntryCard-w9XVzQ {							/* add entry card											*/
	background-color: rgba(var(--transparencycolor),.2);
	border-color: var(--interactive-normal);
}
#app-mount .addEntryCard-w9XVzQ:hover {
	background-color: rgba(var(--transparencycolor),.4);
	border-color: var(--interactive-active);
}

.emojiContainer-1u-_sQ {									/* search				emojicontainer						*/
	background-color: rgba(var(--transparencycolor), .3);
}
.emptyContainer-poti7J {									/* search				no results							*/
	background-color: rgba(var(--transparencycolor), .4);
}
.placeholder-2erB-x {										/* search				placeholder							*/
	background-color: rgba(var(--transparencycolor), .4);
}


/* ~~~~		11.		USERSETTINGS					~~~~ */

.premiumTabItem-1QTfBr[aria-selected=true],
.item-3XjbnG.selected-g-kMVV[aria-controls="Nitro Server Boost-tab"],
.serverBoostTabItem-2hFTIN[aria-selected=true] {
	text-shadow: 1px 1px var(--textshadow);
}
#app-mount .side-2ur1Qk .themed-2-lozF.item-3XjbnG:hover:not(.disabled-1nofHP),		/*		sideitems					*/
#app-mount .topPill-3DJJNV .themed-2-lozF.item-3XjbnG:hover:not(.disabled-1nofHP) {	/*		tabitems					*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .side-2ur1Qk .themed-2-lozF.selected-g-kMVV.item-3XjbnG,
#app-mount .topPill-3DJJNV .themed-2-lozF.selected-g-kMVV.item-3XjbnG,
#app-mount .side-2ur1Qk .themed-2-lozF.selected-g-kMVV.item-3XjbnG:hover,
#app-mount .topPill-3DJJNV .themed-2-lozF.selected-g-kMVV.item-3XjbnG:hover {
	background-color: rgb(var(--accentcolor));
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}

#app-mount .foreground-2hyALB {								/* sidebar				sideitemlink						*/
	background: var(--interactive-normal);
}
#app-mount .link-39xJu3:hover .foreground-2hyALB {
	background: var(--interactive-active);
}

.bd-social-link[title="BD" i] .bd-social-logo,
.bd-social-link[title="BetterDiscord" i] .bd-social-logo,
.bd-social-link[title="BBD" i] .bd-social-logo,
.bd-social-link[title="BandagedBD" i] .bd-social-logo {
	background: var(--interactive-normal);
	-webkit-mask: url(https://mwittrien.github.io/BetterDiscordAddons/Themes/_res/svgs/settingsicons/betterdiscord.svg) center/contain no-repeat;
	opacity: 1;
	transition: background .15s ease;
}
.bd-social-link[title="BD" i]:hover .bd-social-logo,
.bd-social-link[title="BetterDiscord" i]:hover .bd-social-logo,
.bd-social-link[title="BBD" i]:hover .bd-social-logo,
.bd-social-link[title="BandagedBD" i]:hover .bd-social-logo {
	background: var(--interactive-active);
}
.bd-social-link[title="BD" i] .bd-social-logo > *,
.bd-social-link[title="BetterDiscord" i] .bd-social-logo > *,
.bd-social-link[title="BBD" i] .bd-social-logo > *,
.bd-social-link[title="BandagedBD" i] .bd-social-logo > * {
	display: none;
}

.contentRegion-3HkfJJ div[role="tabpanel"] {				/* tabpanel													*/
	width: 100%;
}
.toolsContainer-25FL6V {									/* closebutton			wrapper								*/
	margin-right: 37px;
}
#app-mount .closeButton-PCZcma {							/* closebutton			button								*/
	border-color: var(--channels-default);
}
#app-mount .closeButton-PCZcma path[fill] {
	fill: var(--channels-default);
}
#app-mount .closeButton-PCZcma:hover {
	background-color: rgba(var(--accentcolor), .2);
	border-color: var(--header-secondary);
}
#app-mount .closeButton-PCZcma:hover path[fill] {
	fill: var(--header-secondary);
}
#app-mount .closeButton-PCZcma:active {
	border-color: var(--text-normal);
}
#app-mount .closeButton-PCZcma:active path[fill] {
	fill: var(--text-normal);
}
#app-mount .keybind-13vtq8 {								/* closebutton			keybind								*/
	color: var(--channels-default);
}

#app-mount .closeButtonBold-2Wgbg8 {						/* closebutton			button bold							*/
	border-color: var(--header-secondary);
}
#app-mount .closeButtonBold-2Wgbg8 path[fill] {
	fill: var(--header-secondary);
}
#app-mount .closeButtonBold-2Wgbg8:hover {
	background-color: rgba(var(--accentcolor), .4);
	border-color: var(--text-normal);
}
#app-mount .closeButtonBold-2Wgbg8:hover path[fill] {
	fill: var(--text-normal);
}
#app-mount .closeButtonBold-2Wgbg8:active {
	border-color: var(--header-primary);
}
#app-mount .closeButtonBold-2Wgbg8:active path[fill] {
	fill: var(--header-primary);
}
#app-mount .keybindBold-1U6HoA {							/* closebutton			keybind bold						*/
	color: var(--header-secondary);
}

.cardPrimary-3qRT__, .cardPrimaryEditable-2mz_3i {			/* settingsitems		card								*/
	border-color: rgba(var(--transparencycolor), .1);
}
.cardPrimary-3qRT__ {
	background-color: rgba(var(--transparencycolor), .2);
}
.cardPrimaryEditable-2mz_3i {
	background-color: rgba(var(--transparencycolor), .1);
}
.cardPrimaryOutline-1ofwVz {
	border-color: rgba(var(--transparencycolor), .2);
}

.accountProfileCard-lbN7n-,									/* accountsettings		container							*/
.profileBannerPreview-3_l0Wd {								/* accountsettings		preview								*/
	background: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
}
.accountProfileCard-lbN7n-::before,
.profileBannerPreview-3_l0Wd::before,
.accountProfileCard-lbN7n-::after,
.profileBannerPreview-3_l0Wd::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.accountProfileCard-lbN7n-::before,
.profileBannerPreview-3_l0Wd::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.accountProfileCard-lbN7n-::after,
.profileBannerPreview-3_l0Wd::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}
.accountProfileCard-lbN7n- .avatar-3mTjvZ {					/* accountsettings		container avatar					*/
	background-color: transparent;
	border-color: transparent;
}
.profileBannerPreview-3_l0Wd .avatarUploaderInner-Oiob_P {	/* accountsettings		preview avatar						*/
	background-color: transparent;
	border: unset;
	margin: 6px;
}
.accountProfileCard-lbN7n- .banner-1YaD3N {					/* accountsettings		container banner					*/
	-webkit-mask: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="2400" height="120" viewBox="0 0 2400 120" fill="none"><path fill="black" d="M 0 0 L 0 120 L 20.576172 120 A 46 46 0 0 1 62 94 A 46 46 0 0 1 103.41992 120 L 2400 120 L 2400 0 L 0 0 z"/></svg>') bottom left no-repeat;
}
.profileBannerPreview-3_l0Wd .banner-hcPdsd {				/* accountsettings		preview banner						*/
	-webkit-mask: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="2400" height="120" viewBox="0 0 2400 120" fill="none"><path fill="black" d="M 0 0 L 0 120 L 16 120 A 46 46 0 0 1 62 76 A 46 46 0 0 1 108 120 L 2400 120 L 2400 0 L 0 0 z"/></svg>') bottom left no-repeat;
}
.questionMark-3V9mGJ svg {									/* accountsettings		questionmark new					*/
	filter: drop-shadow(1px 1px var(--textshadow));
}
#app-mount .avatarUploader-AF-hm- .removeButton-3B_Vmg {	/* accountsettings		removeavatar						*/
	color: var(--header-secondary);
}
#app-mount .avatarUploader-AF-hm- .removeButton-3B_Vmg:hover {
	color: var(--text-muted);
}
#app-mount .userSettingsSecurity-3C5Hg5 .codeCheckbox-12-XEX {
	color: var(--text-normal);
}
#app-mount .background-3d_SjE {								/* accountsettings		container							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .fieldList-in8WkP {								/* accountsettings		settings							*/
	background-color: transparent;
}

.colorSwatch-3g4qA8 {										/* profilesettings		colorswatch							*/
	display: flex;
	justify-content: center;
	align-items: center;
}
.colorSwatch-3g4qA8 > [role="radio"] {
	display: flex;
	flex-direction: column;
	align-items: center;
}
.colorSwatch-3g4qA8 > .dropperIconButton-2shYII {
	width: 69px;
	margin: auto;
}

.accountList-305sx3 {										/* connections			container							*/
	background-color: rgba(var(--transparencycolor), .4);
}
.accountBtn-1YkMgV .accountBtnInner-3XK70s {				/* connections			connectioninner						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.accountBtn-1YkMgV .accountBtnInner-3XK70s:hover {
	background-color: rgb(var(--accentcolor));
}
.connection-107AGH {										/* connections			connection							*/
	background-color: rgba(var(--transparencycolor), .3);
}
.connectionHeader-2rV1ze {									/* connections			connection header					*/
	background-color: rgba(var(--transparencycolor), .2);
}

.guildHeader-3nh5RK {										/* boostsettings		suggestioncard						*/
	background-color: rgba(var(--transparencycolor), .5);
}
.guildSubscriptionSlots-JPXXvN {							/* boostsettings		suggestioncard						*/
	background-color: rgba(var(--transparencycolor), .3);
}
.cardWrapper-CyvwQv {										/* boostsettings		suggestioncard						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.cardWrapper-CyvwQv:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
.cardWrapper-CyvwQv .card-2gdrYL,							/* boostsettings		suggestioncard inner				*/
.cardWrapper-CyvwQv .card-2gdrYL:hover {
	background-color: transparent;
}
#app-mount .gemIndicatorContainer-PqApbX {					/* boostsettings		suggestioncard circle				*/
	background-color: transparent;
}
#app-mount .summaryInfo-3hcuop {							/* boostsettings		past transactions summary			*/
	color: var(--header-primary);
}
#app-mount .payment-2bOh4k {								/* boostsettings		past transactions payment			*/
	background-color: transparent;
	color: var(--header-secondary);
}
#app-mount .hoverablePayment-lE1s4t:hover {
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .paymentHeader-2o7Phd {							/* boostsettings		past transactions header			*/
	color: var(--header-primary);
	border-color: var(--background-modifier-accent);
}
#app-mount .expandedInfo-1W31i3 {							/* boostsettings		past transactions expandedinfo		*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .paymentText-BPrx01 {							/* boostsettings		past transactions paymenttext		*/
	color: var(--header-secondary);
}
#app-mount .giftIcon-U9wStf {								/* boostsettings		past transactions gifticon			*/
	color: var(--header-primary);
}

#app-mount .paymentPane-ut5qKZ {							/* boostsettings		past transactions					*/
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--header-primary);
}
#app-mount .paginator-1eqD2g {								/* boostsettings		past transactions paginator			*/
	background: rgba(var(--transparencycolor), .3);
	color: var(--text-muted);
}
#app-mount .bottomDivider-ZmTm-j {							/* boostsettings		past transactions divider			*/
	border-bottom-color: rgba(var(--transparencycolor), .3);
}
#app-mount .tab-2hobIk {									/* boostsettings		past transactions tab				*/
	color: var(--text-muted);
}
#app-mount .externalRowHeader-LT6-4N {						/* boostsettings		past transactions extenal row		*/
	color: var(--header-secondary);
}

.emptyStateImage-2qGUMK {									/* giftinventory		no gifts							*/
	opacity: 0.6;
}

#app-mount .codeRedemptionRedirect-3SBiCp {					/* payment				coderedem							*/
	background-color: rgba(var(--transparencycolor), .2);
	border-color: rgba(var(--transparencycolor), .1);
	color: var(--header-primary);
}

.membershipDialogHouse1-R8jb0l {							/* hypesquad			membershipdialogs					*/
	background-color: rgba(156, 132, 239, .8);
}
.membershipDialogHouse2-2W27iJ {
	background-color: rgba(244, 123, 103, .8);
}
.membershipDialogHouse3-1E5AN4 {
	background-color: rgba(69, 221, 192, .8);
}
.videoWrapper-1_H3B3 {
	background-color: rgba(var(--transparencycolor), .4);
}

.container-3NTP7o {											/* voicesettings		voicebarcontainer					*/
	-webkit-mask: url(https://mwittrien.github.io/BetterDiscordAddons/Themes/_res/svgs/common/voice_level_bar.svg);
}
.notches-2w7UZJ {
	background: transparent !important;
}
#app-mount .progress-1S-TDF {								/* voicesettings		voicebar							*/
	background-color: rgba(var(--transparencycolor), .3);
}
.icon-1fWS75[src="/assets/ebfb23f0cdb11b1871ed8beb3f9ec0ee.svg"],
.icon-1fWS75[src="/assets/c28317e203e00b2d7390d5ece2399228.svg"] {
	-webkit-mask: url(https://discord.com/assets/c28317e203e00b2d7390d5ece2399228.svg) center/contain no-repeat;
	background-color: var(--header-primary);
	object-position: -999999px -999999px;
}
.icon-1fWS75[src="/assets/8c49c7d4a59675bb6ceaee1bb80b5803.png"],
.icon-1fWS75[src="/assets/e8b66317ab0dc9ba3bf8d41a4f3ec914.png"] {
	-webkit-mask: url(https://discord.com/assets/e8b66317ab0dc9ba3bf8d41a4f3ec914.png) center/contain no-repeat;
	background-color: var(--header-primary);
	object-position: -999999px -999999px;
}
.userSettingsVoice-1_dzjw .media-engine-video {				/* voicesettings		video								*/
	background: transparent;
}
#app-mount .userSettingsVoice-1_dzjw .previewOverlay-2reuWf {
	background-color: rgba(var(--transparencycolor), .2);
	border-color: rgba(var(--transparencycolor), .1);
}

.option-1QI4c9 {											/* overlay				option								*/
	background-color: rgba(var(--transparencycolor), .4);
}
.option-1QI4c9:hover,
.option-1QI4c9.selected-18Wszc {
	box-shadow: 0 2px 0 rgba(var(--transparencycolor), .3);
}
.disabled-35mc5w {
	color: rgba(var(--transparencycolor), .4);
}

#app-mount .row-1Tg75B {									/* hotkeys				row									*/
	box-shadow: inset 0 -1px 0 var(--background-modifier-accent);
}

#app-mount .card-2ART2V::before {							/* settingscard			backdrop							*/
	background-color: rgba(var(--transparencycolor), .2);
	border-color: rgba(var(--transparencycolor), .1);
}
#app-mount .button-1yVL_7 {									/* settingscard			removebutton						*/
	background-color: rgba(var(--transparencycolor), .3);
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .6), 0 1px 5px 0 rgba(var(--transparencycolor), .3);
}
#app-mount .button-1yVL_7:hover {
	background-color: rgba(var(--transparencycolor), .7);
}

#app-mount .game-3x3aDt {									/* games				card								*/
	box-shadow: 0 1px 0 0 var(--background-modifier-accent);
}
#app-mount .gameNameInput-3TuPuA:focus,
#app-mount .gameNameInput-3TuPuA:hover {
	background-color: rgba(var(--transparencycolor), .3);
	border-color: rgba(var(--transparencycolor), .1);
}
#app-mount .gameName-Uw4dbt {								/* games				gamename							*/
	color: var(--header-primary);
}
#app-mount .lastPlayed-3aHvxk,								/* games				lastplayed							*/
#app-mount .overlayStatusText-AHDYB3 {						/* games				overlaystatustext					*/
	color: var(--text-muted);
}
#app-mount .overlayToggleIconOn-3_-nGm .fill-MYciTJ {		/* games				overlaystatusicon					*/
	fill: var(--text-muted);
}
#app-mount .nowPlayingAdd-3lvnXJ {							/* games				descriptionhint						*/
	color: var(--header-secondary);
}
#app-mount .nowPlaying-zBamm2 .gameName-Uw4dbt {
	color: #fff;
}
#app-mount .nowPlaying-zBamm2 .lastPlayed-3aHvxk,
#app-mount .nowPlaying-zBamm2 .overlayStatusText-AHDYB3 {
	color: #b4e1cd;
}
#app-mount .nowPlaying-zBamm2 .overlayToggleIconOff-3hGOmN .fill-MYciTJ,
#app-mount .nowPlaying-zBamm2 .overlayToggleIconOn-3_-nGm .fill-MYciTJ {
	fill: #b4e1cd;
}
#app-mount .notDetected-2HEmAp {							/* games				nogame								*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .notDetected-2HEmAp .lastPlayed-3aHvxk {
	color: var(--header-secondary);
}
#app-mount .activeGame-3ncS55 .removeGame-3Le1LJ {
	background-image: none;
}
#app-mount .activeGame-3ncS55 .removeGame-3Le1LJ::after {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	background: var(--header-primary);
	-webkit-mask: url(https://discord.com/assets/eb69ec9fdd30653a3ade1ab501a7cd3d.svg) center no-repeat;
}

#app-mount .addGamePopout-3yePJc {							/* games				add game popout						*/
	background-color: transparent;
}
.addGamePopout-3yePJc::before,
.addGamePopout-3yePJc::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.addGamePopout-3yePJc::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.addGamePopout-3yePJc::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.15));
	backdrop-filter: blur(var(--popoutblur));
}
#app-mount .addGamePopout-3yePJc .cancelButton-1vsI8S {
	color: var(--header-primary);
}

.preview-rua1rr {											/* appearance			preview								*/
	background-color: rgba(var(--transparencycolor), .2);
	border-color: rgba(var(--transparencycolor), .2);
}

#app-mount .item-3eFBNF {									/* languagesettings		row									*/
	border-radius: 5px;
	box-shadow: 0 1px 0 0 var(--background-modifier-accent);
}
.item-3eFBNF:hover {
	background-color: rgba(var(--transparencycolor), .2);
}
.item-3eFBNF.selected-2DeaDa {
	background-color: rgba(var(--transparencycolor), .4);
}


/* ~~~~		12.		GUILDSETTINGS					~~~~ */

.container-20TyK0 {											/* settings				confirmnotice						*/
	position: relative;
	backdrop-filter: blur(var(--backgroundblur));
}
.container-20TyK0[style*="background-color: rgba(248, 249, 249"],
.container-20TyK0[style*="background-color: rgba(32, 34, 37"] {
	background-color: rgba(var(--transparencycolor), .7) !important;
}
.container-20TyK0[style*="background-color: rgba(248, 249, 249"] .message-3C6JQ1,
.container-20TyK0[style*="background-color: rgba(32, 34, 37"] .message-3C6JQ1 {
	color: var(--header-primary) !important;
}
.container-20TyK0[style*="background-color: rgba(248, 249, 249"] .resetButton-jFzA0U span[style],
.container-20TyK0[style*="background-color: rgba(32, 34, 37"] .resetButton-jFzA0U span[style] {
	color: var(--header-primary) !important;
}
.container-20TyK0::before {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
	pointer-events: none;
	z-index: -1;
}

.roles-34RIpY {												/* rolesettings			intro roles							*/
	z-index: 2;
}
.profileCard-1j58Ju {										/* rolesettings			intro profile						*/
	position: relative;
	z-index: 1;
}
.profileCard-1j58Ju::before,
.profileCard-1j58Ju::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.profileCard-1j58Ju::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.profileCard-1j58Ju::after {
	backdrop-filter: blur(var(--popoutblur));
}
.sidebar-3K3Z4C {											/* rolesettings			sidebar								*/
	background-color: rgba(var(--transparencycolor), .1);
	border: none;
}
.container-3EtAkD {											/* rolesettings			everyone role						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.container-3EtAkD:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
img[src="/assets/cef02719c12d8aaf38894c16dca7fbe6.svg"] {	/* rolesettings			addrolebutton						*/
	-webkit-mask: url(https://discord.com/assets/cef02719c12d8aaf38894c16dca7fbe6.svg);
	background: currentColor;
	object-position: -999999px -999999px;
}
.settingCard-xZSDjS {										/* rolesettings			setting card						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.settingCard-xZSDjS.active-3EK-ed {							/* rolesettings			setting card active					*/
	background-color: rgba(var(--transparencycolor), .3);
}
.cardContent-1-5hym {										/* rolesettings			setting card header					*/
	background-color: rgba(var(--transparencycolor), .2);
}
.cardFolder-3H4uH4 {										/* rolesettings			setting card body					*/
	background-color: transparent;
}
.group-LWHoGI {												/* rolesettings			permissions group					*/
	border-color: rgb(var(--transparencycolor), .4);
}
.item-4m-12I {												/* rolesettings			permissions item					*/
	background: rgb(var(--transparencycolor), .2);
}
.item-4m-12I:hover {
	background: rgb(var(--transparencycolor), .4);
}
.passthrough--fbdFR.selected-3jieYB {						/* rolesettings			permissions passthrough selected	*/
	background: rgb(var(--accentcolor));
}
.icon-2DGsye {												/* rolesettings			everyone role icon					*/
	background-color: rgba(var(--transparencycolor), .4);
}
.titleContainer-3fPic2,										/* rolesettings			roles list header					*/
.header-JUTO-g {											/* rolesettings			perms list header					*/
	background-color: transparent;
}
.titleElevated-eN3exl,
.stickyHeaderElevated-dNSSrJ {
	box-shadow: none;
}
.header-JUTO-g::before,
.header-JUTO-g::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	pointer-events: none;
	z-index: -1;
}
.header-JUTO-g::before {
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
}
.header-JUTO-g::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha)));
	backdrop-filter: blur(var(--backgroundblur));
}
.roleDot-2a4Pv7 {											/* rolesettings			role dot							*/
	border: none;
}
.roleRow-3LoHQ6:hover:not(.roleRowDisableHover-2TXfy-) {	/* rolesettings			role row							*/
	background-color: rgba(var(--transparencycolor), .2);
}
.roleRow-3LoHQ6:hover:not(.roleRowDisableHover-2TXfy-) .circleButton-33AIyY {
	background-color: rgba(var(--transparencycolor), .2);
}
.roleRow-3LoHQ6:hover:not(.roleRowDisableHover-2TXfy-) .circleButton-33AIyY:hover {
	background-color: rgb(var(--accentcolor));
}
.roleRow-3LoHQ6:before,
.roleRow-3LoHQ6:last-child:after {
	background-color: var(--background-modifier-accent);
}
.memberRow-1FhJgR:hover {									/* rolesettings			member row							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .colorPickerSwatch-RTUGRR.noColor-1Oln62 {		/* rolesettings			colorswatch nocolor					*/
	border-color: rgba(var(--textbrightest), .3);
}
#app-mount .colorPickerSwatch-RTUGRR.noColor-1Oln62 .colorPickerDropperFg-Lureab {
	fill: var(--header-primary);
}
#app-mount .colorPickerSwatch-RTUGRR.noColor-1Oln62 polyline {
	stroke: var(--header-primary);
}
.previewContainer-1xQAsw {									/* rolesettings			preview								*/
	border: none;
}
.messageContainer-3a6gLR {									/* rolesettings			preview message						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.theme-light .messageContainer-3a6gLR {
	display: none;
}
.addMemberRow-KVhQFf.selectedRow-1SAgVL {					/* rolesettings			add member row						*/
	background-color: rgba(var(--transparencycolor), .2);
}

#app-mount .emojiAliasInput-1y-NBz .emojiInput-1aLNse {		/* emojisettings		nameinput							*/
	background-color: rgba(var(--transparencycolor), .1);
}

#app-mount .auditLog-1NVAY0 {								/* auditlogs			logitem								*/
	border-color: rgba(var(--transparencycolor), .1);
	color: var(--text-muted);
}
#app-mount .headerClickable-zGQJz3,							/* auditlogs			loginner							*/
#app-mount .headerDefault-1e6yjj {
	background-color: rgba(var(--transparencycolor), .2);
	color: var(--header-secondary);
}
#app-mount .headerExpanded-1-zwDr {
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--header-secondary);
}
#app-mount .divider-M3saWq {								/* auditlogs			loginnerdivider						*/
	background-color: var(--background-modifier-accent);
}
#app-mount .changeDetails-1kMZqI {							/* auditlogs			logdetails							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .userHook-3R3zjr {								/* auditlogs			userhook							*/
	color: var(--header-primary);
}
#app-mount .auditLog-1NVAY0 strong {						/* auditlogs			targets								*/
	color: var(--header-primary);
}
#app-mount .timestamp-147bcs {								/* auditlogs			timestamp							*/
	color: var(--text-muted);
}
#app-mount .expandForeground-1nZ4VR {						/* auditlogs			expandarrow							*/
	stroke: var(--header-secondary);
}
.themeOverrideLight-bdYR2N.icon-2PiQ65,						/* auditlogs			logicon								*/
.themeOverrideDark-3-xxHI.icon-2PiQ65,
#app-mount .icon-2PiQ65 {
	background: none !important;
}
.icon-2PiQ65::before {
	content: "";
	position: absolute;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	background: var(--header-primary);
}
.icon-2PiQ65.applicationCommand-3YMgNf::before {
	-webkit-mask: url(https://discord.com/assets/561a626f671b8fd8f0c2e85c97df9b04.svg);
}
.icon-2PiQ65.targetAll-21RPfg::before {
	-webkit-mask: url(https://discord.com/assets/22fd0ab3562af24ea964465bb65531aa.svg);
}
.icon-2PiQ65.targetBan-qwvck2::before {
	-webkit-mask: url(https://discord.com/assets/fd541825b6853aaae233ad9d83e05a18.svg);
}
.icon-2PiQ65.targetChannel-1NWbC5::before {
	-webkit-mask: url(https://discord.com/assets/528ae525a9823affbcd2a35bd20573b0.svg);
}
.icon-2PiQ65.targetEmoji-2T6Ze4::before {
	-webkit-mask: url(https://discord.com/assets/858ab2bdee17ca226df85e23263bcf3a.svg);
}
.icon-2PiQ65.targetGuild-pvPVWS::before {
	-webkit-mask: url(https://discord.com/assets/448b698d906ab4d93b609282595a1c9d.svg);
}
.icon-2PiQ65.targetGuildScheduledEvent-330pb3::before {
	-webkit-mask: url(https://discord.com/assets/7093e58edcd5202a129a6e4fbf427c6d.svg);
}
.icon-2PiQ65.targetIntegration-j5Mnwy::before {
	-webkit-mask: url(https://discord.com/assets/993b5f52b8bd8d1c1c34cac05015c331.svg);
}
.icon-2PiQ65.targetInvite-2hFskc::before {
	-webkit-mask: url(https://discord.com/assets/d0dc8a4c8ea55b119c5c2cccf69b031f.svg);
}
.icon-2PiQ65.targetMember-2pI3Cu::before {
	-webkit-mask: url(https://discord.com/assets/e2c0846875f889524e3d60e7d25afa55.svg);
}
.icon-2PiQ65.targetMemberRole-jNaX-k::before {
	-webkit-mask: url(https://discord.com/assets/00124e254d0d86c37f6d02ec0c5b1e02.svg);
}
.icon-2PiQ65.targetMessage-WgF9Dt::before {
	-webkit-mask: url(https://discord.com/assets/aa9f9c29b51e414f0476d4388031aaf4.svg);
}
.icon-2PiQ65.targetPermission-2fNNaU::before {
	-webkit-mask: url(https://discord.com/assets/35de2007bfe0db9821881321d8b7c1fe.svg);
}
.icon-2PiQ65.targetRole-24Nm1S::before {
	-webkit-mask: url(https://discord.com/assets/9aa6e9df74888ec09885bb08341800be.svg);
}
.icon-2PiQ65.targetStageInstance-2ljqjY::before {
	-webkit-mask: url(https://discord.com/assets/dfad85fc7c072498298077f68cf006ca.svg);
}
.icon-2PiQ65.targetSticker-2BoYB9::before {
	-webkit-mask: url(https://discord.com/assets/da5f0aa4b5ccf0165b4220ba9929ea59.svg);
}
.icon-2PiQ65.targetVanityUrl-1KGkGd::before {
	-webkit-mask: url(https://discord.com/assets/bef4eebd4f9e00aabbfa7de1949c8565.svg);
}
.icon-2PiQ65.targetWebhook-3gzYYG::before {
	-webkit-mask: url(https://discord.com/assets/210ac667f45d13bc52020744f008b1ed.svg);
}
.icon-2PiQ65.targetWidget-3g4NqJ::before {
	-webkit-mask: url(https://discord.com/assets/03f717eddad9ac74a1900254625657cf.svg);
}
.icon-2PiQ65.thread-P4cm8D::before {
	-webkit-mask: url(https://discord.com/assets/c254ffdde9bc5c90c5ec5d9e11dbf382.svg);
}

#app-mount .card-o7rAq- {									/* integrationsettings	card								*/
	border-color: rgba(var(--transparencycolor), .1)
}
#app-mount .card-3IImnr {									/* integrationsettings	webhook card						*/
	border-color: rgba(var(--transparencycolor), .1)
}
#app-mount .card-1o0mns {									/* integrationsettings	apps card							*/
	border-color: rgba(var(--transparencycolor), .1)
}
#app-mount .card-11DMwv {									/* integrationsettings	follows card						*/
	border-color: rgba(var(--transparencycolor), .1)
}
.iconWrapper-lS1uig {										/* integrationsettings	icon								*/
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .footerImage-4UrEF0 {
    background-image: url(https://discord.com/assets/36d0e0bb009fa362c2533003c0af67b5.svg);
	opacity: 0.6;
}

.guildDetails-2p1NmK {										/* communitysettings	intro		details					*/
	background-color: rgba(var(--transparencycolor), .4);
}
.featureCard-1RR4Tl {										/* communitysettings	intro		featurecard				*/
	background-color: rgba(var(--transparencycolor), .3);
}
.featureIcon-3p1TC_ {										/* communitysettings	intro		featureicon				*/
	background-color: rgba(var(--transparencycolor), .3);
}
.checklistContainer-mFJZEJ {								/* communitysettings	intro		checklist				*/
	background-color: rgba(var(--transparencycolor), .3);
}
.checklistHeader-1KWcEY {									/* communitysettings	intro		checklist header		*/
	background-color: rgba(var(--transparencycolor), .3);
}

.upsellContainer-L9xv7w {									/* communitysettings	general		upsellcontainer			*/
	background-color: rgba(var(--transparencycolor), .2);
}
.upsellFooter-ZYsio_ {										/* communitysettings	general		upsellfooter			*/
	background-color: rgba(var(--transparencycolor), .2);
}

.developerPortalCtaWrapper-2XNafh {							/* communitysettings	analytics	info					*/
	background-color: rgba(var(--transparencycolor), .3);
}
.analyticsCard-2fnrVG {										/* communitysettings	analytics	card					*/
	background-color: rgba(var(--transparencycolor), .3);
}
.backgroundAccent-2YeFtZ {									/* communitysettings	analytics	error					*/
	background-color: rgba(var(--transparencycolor), .2);
}

#app-mount .card-3_CqkU {									/* communitysettings	discovery	card					*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .iconMask-30Tvqs {								/* communitysettings	discovery	icon					*/
	background-color: rgba(var(--transparencycolor), .2);
}
.perkArt-1SGWbA {											/* communitysettings	discovery	perk					*/
	background-color: rgba(var(--transparencycolor), .4);
}
.container-2w0lh0 {											/* communitysettings	discovery	checklist				*/
	background-color: rgba(var(--transparencycolor), .3);
}
.header-2Y0-A- {											/* communitysettings	discovery	checklist header		*/
	background-color: rgba(var(--transparencycolor), .3);
}

.exampleContainer-2O-nVK,									/* communitysettings	rules		example					*/
.exampleContainer-25sB-A {									/* communitysettings	welcome		example					*/
	background: transparent;
	position: relative;
}
.exampleContainer-2O-nVK > *,
.exampleContainer-25sB-A > * {
	z-index: 1;
}
.exampleContainer-2O-nVK::after,
.exampleContainer-25sB-A::after {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	background-color: rgba(var(--transparencycolor), .5);
	-webkit-mask: url(https://mwittrien.github.io/BetterDiscordAddons/Themes/_res/svgs/common/discord_window_placeholder.svg) 0 0/cover no-repeat;
}
#app-mount .exampleModal-1lRfuE,							/* communitysettings	rules		examplemodal			*/
#app-mount .exampleModal-2X2Vf8 {							/* communitysettings	welcome		examplemodal			*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	border-radius: 5px;
}
.exampleModal-1lRfuE > *,
.exampleModal-2X2Vf8 > * {
	z-index: 1;
}
.exampleModal-1lRfuE::before,
.exampleModal-2X2Vf8::before,
.exampleModal-1lRfuE::after,
.exampleModal-2X2Vf8::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
}
.exampleModal-1lRfuE::before,
.exampleModal-2X2Vf8::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.exampleModal-1lRfuE::after,
.exampleModal-2X2Vf8::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	backdrop-filter: blur(var(--popoutblur));
}

.guildSidebar-pjuGkm {										/* communitysettings	rules		example sidebar			*/
	background-color: rgba(var(--transparencycolor), .4);
	margin-right: 0 !important;
}
.content-pHpkq8 {											/* communitysettings	rules		example inner			*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .footer-11k_3m {									/* communitysettings	rules		example footer			*/
	background: transparent;
}
.exampleTextSingleLine-3bwqy5 {								/* communitysettings	rules		example line			*/
	background-color: rgba(var(--textbrightest), .3);
}

.enableContainer-1J91Aq {									/* communitysettings	rules		enablecontainer			*/
	background-color: rgba(var(--transparencycolor), .3);
}
.icon-1_mnkD {												/* communitysettings	rules		category icon			*/
	background-color: rgba(var(--transparencycolor), .2);
}
.settingsFormItem-25zW3t {									/* communitysettings	rules		form					*/
	background-color: rgba(var(--transparencycolor), .2);
}
.getStartedWrapper-2mNX-j {									/* communitysettings	rules		getstarted				*/
	background-color: rgba(var(--transparencycolor), .2);
}
.exampleRule-3gJ39X {										/* communitysettings	rules		example rule			*/
	background-color: rgba(var(--transparencycolor), .4);
}
.rulesTextAreaInput-asSkdy {								/* communitysettings	rules		edit rule				*/
	border-color: rgba(var(--transparencycolor), .3);
}
.rulesTextAreaInput-asSkdy:hover:not(:focus) {
	border-color: rgb(var(--transparencycolor));
}
.editCircle-2uL_D3 {										/* communitysettings	rules		editcirle				*/
	background-color: rgba(var(--transparencycolor), .4);
}
.editButton-2SLR4j {										/* communitysettings	rules		editbutton				*/
	background-color: rgba(var(--transparencycolor), .4);
}
.editButton-2SLR4j:hover {
	background-color: rgba(var(--transparencycolor), .6);
}
.formFieldWrapper-2LV3S6,
.settingsFormFieldWrapper-U99c9i {							/* communitysettings	rules		form field				*/
	background-color: rgba(var(--transparencycolor), .2);
	border-color: rgba(var(--transparencycolor), .2);
}

.editCircle-ityklj {										/* communitysettings	welcome		editcirle				*/
	background-color: rgba(var(--transparencycolor), .4);
}
.optionContainer-1FtykV {									/* communitysettings	welcome		exampleoption			*/
	background-color: rgba(var(--transparencycolor), .3);
}
.enableContainer-6E-puu {									/* communitysettings	welcome		previewheader			*/
	background-color: rgba(var(--transparencycolor), .4);
}
.previewContainer-1SS3uO {									/* communitysettings	welcome		previewcontainer		*/
	background-color: rgba(var(--transparencycolor), .2);
}
.welcomeChannel-1rFrIO {									/* communitysettings	welcome		welcomechannel			*/
	background-color: rgba(var(--transparencycolor), .4);
}
.channelIcon-1eKmlw {										/* communitysettings	welcome		channelicon			s	*/
	background-color: rgba(var(--transparencycolor), .4);
}

.descriptionBox-1EKQKL {									/* templatesettings		descriptionbox						*/
	background-color: rgba(var(--transparencycolor), .3);
}

#app-mount .tierHeaderLocked-30MLlO {						/* boostsettings		tierheaderlocked					*/
	background-color: rgba(var(--transparencycolor), .4);
	color: var(--header-secondary);
}
#app-mount .tierHeaderUnlocked-1OpOLf {						/* boostsettings		tierheaderunlocked					*/
	background-color: rgba(var(--transparencycolor), .5);
}
#app-mount .tierCloseClose-T256RA {							/* boostsettings		tiercloseclose						*/
	color: var(--header-primary);
}
#app-mount .tierBody-1d3UiS {								/* boostsettings		tierbody							*/
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--header-secondary);
}
#app-mount .tierInProgress-1vFUnw {							/* boostsettings		tiermilestone						*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .background-3xJH_4 {								/* boostsettings		tierbar	(settings)					*/
	color: rgba(var(--transparencycolor), .3);
}

#app-mount .member-1q7VfX {									/* membersettings		membercard							*/
	box-shadow: 0 1px 0 0 var(--background-modifier-accent);
}
#app-mount .member-1q7VfX .name-8yzEIY {					/* membersettings		membercardname						*/
	color: var(--header-primary);
}
#app-mount .member-1q7VfX .tag-1YGWN9 {						/* membersettings		membercardtag						*/
	color: var(--text-muted);
}
#app-mount .member-1q7VfX .roleWrapper-1Hde_V {				/* membersettings		rolewrapper							*/
	color: rgba(var(--textbrightest),.8);
}
#app-mount .actionButton-1YKTU0 {							/* membersettings		addrolebutton						*/
	border-color: var(--header-secondary);
	color: var(--header-secondary);
}
#app-mount .member-1q7VfX .overflowIconFg-QMRRFI {			/* membersettings		3-dot icon							*/
	fill: var(--header-primary);
}
#app-mount .member-1q7VfX .ownerHelpIcon-3ItaBx {			/* membersettings		help icon							*/
	color: var(--header-primary);
}

#app-mount .overflowRolesPopout-1Puiuq,						/* membersettings		roleoverflow popout					*/
#app-mount .overflowRolesPopoutArrow-2R7g3K {
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .2), 0 2px 10px 0 rgba(var(--transparencycolor), .2);
	border: none;
	border-radius: 3px;
	overflow: hidden;
}
.overflowRolesPopout-1Puiuq::before,
.overflowRolesPopoutArrow-2R7g3K::before,
.overflowRolesPopout-1Puiuq::after,
.overflowRolesPopoutArrow-2R7g3K::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.overflowRolesPopout-1Puiuq::before,
.overflowRolesPopoutArrow-2R7g3K::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.overflowRolesPopout-1Puiuq::after,
.overflowRolesPopoutArrow-2R7g3K::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.1));
	backdrop-filter: blur(var(--popoutblur));
}
.overflowRolesPopoutHeaderIcon-2LIuSc path {
	fill: var(--header-secondary);
}
.overflowRolesPopoutHeaderText-3HyHGv {
	color: var(--header-secondary);
}

#app-mount .inviteSettingsInviteRow-1rZeIM {				/* invitesettings		invitecard							*/
	box-shadow: 0 1px 0 0 var(--background-modifier-accent);
}

#app-mount .bannedUser-1IalTM {								/* bansettings			bancard								*/
	box-shadow: 0 1px 0 0 var(--background-modifier-accent);
}
#app-mount .bannedUser-1IalTM .username-1b3MVI {			/* invitesettings		username							*/
	color: var(--header-primary);
}
#app-mount .bannedUserModal-3RJCOV .reasonHeader-2etdjy {	/* invitesettings		banmodalreasonheader				*/
	color: var(--text-normal);
}
#app-mount .bannedUser-1IalTM .username-1b3MVI .discrim-oGb-FO,
#app-mount .bannedUserModal-3RJCOV .reason-YbfGC6,			/* invitesettings		banmodalreason						*/
#app-mount .bannedUserModal-3RJCOV .userDiscrim-1D2NlF {	/* invitesettings		discriminator						*/
	color: var(--text-muted);
}


/* ~~~~		13.		MODALS							~~~~ */

.layer-1Ixpg3:nth-child(1),
.withLayer-2VVmpp:nth-child(1) {
	z-index: 1002;
}
.layer-1Ixpg3:nth-child(2),
.withLayer-2VVmpp:nth-child(2) {
	z-index: 1003;
}
.layer-1Ixpg3:nth-child(3),
.withLayer-2VVmpp:nth-child(3) {
	z-index: 1004;
}
.layer-1Ixpg3:nth-child(4),
.withLayer-2VVmpp:nth-child(4) {
	z-index: 1005;
}
.layer-1Ixpg3:nth-child(5),
.withLayer-2VVmpp:nth-child(5) {
	z-index: 1006;
}
.layer-1Ixpg3:nth-child(6),
.withLayer-2VVmpp:nth-child(6) {
	z-index: 1007;
}
.layer-1Ixpg3:nth-child(7),
.withLayer-2VVmpp:nth-child(7) {
	z-index: 1008;
}
.layer-1Ixpg3:nth-child(8),
.withLayer-2VVmpp:nth-child(8) {
	z-index: 1009;
}
.layer-1Ixpg3:nth-child(9),
.withLayer-2VVmpp:nth-child(9) {
	z-index: 1010;
}

#app-mount .root-g14mjS,									/* modal				container (foldersettings)			*/
#app-mount .modal-2RrUKJ {									/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	border-radius: 5px;
}
.root-g14mjS > *,
.modal-2RrUKJ > * {
	z-index: 1;
}
.root-g14mjS::before,
.modal-2RrUKJ::before,
.root-g14mjS::after,
.modal-2RrUKJ::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.root-g14mjS::before,
.modal-2RrUKJ::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.root-g14mjS::after,
.modal-2RrUKJ::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	backdrop-filter: blur(var(--popoutblur));
}
.root-g14mjS .modal-2RrUKJ::before,
.modal-3Crloo::before,
.root-g14mjS .modal-2RrUKJ::after,
.modal-3Crloo::after {
	display: none;
}
.header-1zd7se > .wrapper-1HSdhi:first-child {
	flex: 1 0 auto;
}
#app-mount .separator-2lLxgC {
	box-shadow: 0 1px 0 0 rgba(var(--transparencycolor),.3), 0 1px 2px 0 rgba(var(--transparencycolor),.3);
}
#app-mount .modalTextContainer-1FUO2W {						/* modal				text file						*/
	background-color: rgba(var(--transparencycolor), .5);
	border: none;
}
#app-mount .footer-31IekZ {									/* modal				footer							*/
	background-color: rgba(var(--transparencycolor), .2);
	box-shadow: none;
	z-index: 0;
}
#app-mount .footer-3Zgy_M {									/* modal				footer info						*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .close-1mLglB {									/* modal				closebutton						*/
	z-index: 2;
}

.tabBarContainer-sCZC4w {									/* modal				tabbarcontainer					*/
	border-top-color: rgba(var(--transparencycolor), .3);
}
#app-mount .modal-6GHvdM .tabBarContainer-sCZC4w {
	background: rgba(var(--transparencycolor), .2);
	box-shadow: 0 2px 3px 0 rgba(var(--transparencycolor), .1);
}

#app-mount .separator-3TK_-B {
	box-shadow: 0 1px 0 0 rgba(var(--transparencycolor),.3), 0 1px 2px 0 rgba(var(--transparencycolor),.3);
}
#app-mount .divider-3APUjw {
	border-color: var(--background-modifier-accent);
}

#app-mount .subHeader-2z6h5Z {
	color: var(--header-secondary);
}
#app-mount .sectionBody-7I2eAN,
#app-mount .subHeader-1mr1LG {
	color: var(--header-secondary);
}

#app-mount .message-1F58Gs {
	color: var(--header-secondary);
}
#app-mount .secondaryButton-197mr8 {
	color: var(--header-primary);
}
#app-mount .imageUpgrade-moI_hv {
	background-image: url(https://discord.com/assets/81ded87ebac6f9d55e8624a3e5167c8f.svg);
}
#app-mount .imageCancel-2x4k_k {
	background: url(https://discord.com/assets/03863b539aec443327ca2ffc51a89dac.svg);
}
#app-mount .imageUnclaimed-5nJyYs {
	background-image: url(https://discord.com/assets/3b65c741e596bc0979f7ba0c42de6fff.svg);
	opacity: .5;
}
#app-mount .imageUnverified-2NLnW6 {
	background-image: url(https://discord.com/assets/e260177e5165e6789e30b9592df75424.svg);
	opacity: .5;
}

#app-mount .divider-MRAL1L {
	border-color: var(--background-modifier-accent);
}
#app-mount .backButtonColor-5k5ViL {
	color: var(--header-primary);
}
#app-mount .checkboxLabel-NbUiJx {
	color: var(--header-secondary);
}

/* ----		13.1.	USERMODAL						----- */

#app-mount .root-8LYsGj {									/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: hidden;
}
.root-8LYsGj::before,
.root-8LYsGj::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.root-8LYsGj::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.root-8LYsGj::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}
#app-mount .root-8LYsGj .topSection-13QKHs {				/* modal				topsection							*/
	background-color: rgba(var(--transparencycolor), .2);
}
.root-8LYsGj .banner-1YaD3N {								/* modal				banner								*/
	-webkit-mask: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="2400" height="240" viewBox="0 0 2400 240" fill="none"><path fill="black" d="M 0 0 L 0 240 L 16 240 A 69 69 0 0 1 85 172 A 69 69 0 0 1 152 240 L 2400 240 L 2400 0 L 0 0 z"/></svg>') bottom left no-repeat;
}
.root-8LYsGj .avatar-3QF_VA {								/* modal				avatar								*/
	background-color: transparent;
	border-color: transparent;
	box-sizing: content-box;
}
#app-mount .body-1Ukv50 {									/* modal				body								*/
	background-color: transparent;
}
.listRow-2nO1T6:hover {
	background-color: rgba(var(--transparencycolor), .2);
}
.emptyIcon-uKVxYR {											/* body					emptypic							*/
	opacity: .5;
}

/* ----		13.2.	GUILDADD/CREATION				----- */

.container-x8Y1ix,											/* create modal			item								*/
.guildRow-3fJnG6 {											/* hub modal			item								*/
	background-color: rgb(var(--transparencycolor), .2);
	border: none;
}
.container-x8Y1ix:hover,
.guildRow-3fJnG6:hover {
	background-color: rgb(var(--transparencycolor), .4);
}
.text-PdAsFQ,												/* create modal			text								*/
.guildName-3RzJ_H {											/* hub modal			text								*/
	color: var(--header-secondary);
}
.container-x8Y1ix:hover .text-PdAsFQ,
.guildRow-3fJnG6:hover .guildName-3RzJ_H {
	color: var(--header-primary);
}
.arrow-2yY1Tm,												/* create modal			arrow								*/
.guildName-3RzJ_H ~ img {									/* hub modal			arrow								*/
	object-position: -999999px -999999px;
	-webkit-mask: url(https://discord.com/assets/69a0ea5dbf79a129c81a0cb171b60b7a.svg) center/cover no-repeat;
	background: var(--header-secondary);
}
.container-x8Y1ix:hover .arrow-2yY1Tm,
.guildRow-3fJnG6:hover .guildName-3RzJ_H ~ img {
	background: var(--header-primary);
}
.input-m1-Y7Q {												/* modal				invite input						*/
	background: transparent;
}
.inputInner-1Z3Tui {										/* modal				invite input inner					*/
	border: 1px solid var(--deprecated-text-input-border);
}

/* ----		13.3.	REGIONSELECTMODAL				---- */

#app-mount .regionSelectModal-12e-57 {						/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: hidden;
}
.regionSelectModal-12e-57::before,
.regionSelectModal-12e-57::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.regionSelectModal-12e-57::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.regionSelectModal-12e-57::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	backdrop-filter: blur(var(--popoutblur));
}
#app-mount .regionSelectModal-12e-57 .regionSelectModalOption-2DSIZ3 {
	background-color: rgba(var(--transparencycolor), .2);
	border-color: rgba(var(--transparencycolor), .1);
}
#app-mount .regionSelectModal-12e-57 .regionSelectModalOption-2DSIZ3:hover {
	background-color: rgba(var(--transparencycolor), .3);
}

#app-mount .regionSelect-3lf4eE.regionSelectLoading-34I21m {
	border: 1px solid var(--header-secondary);
}
#app-mount .regionSelect-3lf4eE button {
	border: 1px solid var(--header-secondary);
}
#app-mount .regionSelect-3lf4eE .regionSelectInner-24f4Ce {
	border: 1px solid var(--header-secondary);
}
#app-mount .regionSelectModal-12e-57 .regionSelectModalFooter-20C5iA {
	color: var(--text-muted);
}
#app-mount .regionSelectName-2-2FWh {
	color: var(--text-muted);
}
#app-mount .regionSelectModal-12e-57 .regionSelectModalOption-2DSIZ3:hover .regionSelectName-2-2FWh {
	color: var(--text-normal);
}
#app-mount .regionSelect-3lf4eE:hover button {
	color: var(--header-primary);
}
#app-mount .container-1s4HBn.hover-2AGf5p {
	border-color: var(--deprecated-text-input-border-hover);
}
#app-mount .flag-16iIBd.vip-3pFIN8::after {
	border-color: rgba(var(--transparencycolor), .5);
}

/* ----		13.4.	UPLOADMODAL						---- */

#app-mount .uploadModal-2ie9O_ {							/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	border-radius: 10px;
}
.uploadModal-2ie9O_::before,
.uploadModal-2ie9O_::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 10px;
	pointer-events: none;
	z-index: -1;
}
.uploadModal-2ie9O_::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.uploadModal-2ie9O_::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	backdrop-filter: blur(var(--popoutblur));
}

.uploadModalIn-2w48Zf .uploadDropModal-13Kd20 {
	width: unset;
}
.uploadModalIn-2w48Zf .uploadDropModal-13Kd20 .inner-rBP-MS .title-3ChJ_v,
.uploadModalIn-2w48Zf .uploadDropModal-13Kd20 .inner-rBP-MS .instructions-272j2A {
	text-shadow: 1px 1px var(--textshadow);
}
.uploadModal-2ie9O_ .inner-zqa7da {							/* modal				channeltextarea						*/
	background-color: rgba(var(--transparencycolor), .3);
}
.uploadModal-2ie9O_ .footer-VCsJQY {						/* modal				footer								*/
	background-color: rgba(var(--transparencycolor), .2);
	box-shadow: none;
}
.uploadModal-2ie9O_ .inner-rBP-MS .file-163EuR .icon-HW4tZ-.image-2ssF8k {
	box-shadow: 0 2px 8px rgba(var(--transparencycolor), .4);
}

/* ----		13.5.	KEYBOARDSHORTCUTSMODAL			---- */

#app-mount .keyboardShortcutsModal-2CRmCm {					/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: hidden;
}
.keyboardShortcutsModal-2CRmCm::before,
.keyboardShortcutsModal-2CRmCm::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.keyboardShortcutsModal-2CRmCm::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.keyboardShortcutsModal-2CRmCm::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	backdrop-filter: blur(var(--popoutblur));
}
#app-mount .modalTitle-2skSKy {								/* modal				title								*/
	color: var(--header-primary);
}
#app-mount .modalSubtitle-2lx7qk {							/* modal				subtitle							*/
	border-color: var(--background-modifier-accent);
	color: var(--text-normal);
}
#app-mount .keyboardShortcutList-3VFAYS .keybindGroup-39HP2U .keybindDescription-oXh6w_ {
	color: var(--header-secondary);
}
#app-mount .keybindShortcut-3zF1P9 {
	color: var(--header-primary);
}
#app-mount .keybindShortcut-3zF1P9 span {
	background-color: var(--text-muted);
	border: 1px solid rgba(0, 0, 0, .4);
	box-shadow: inset 0 -4px 0 rgba(0, 0, 0, .4);
	color: var(--header-primary);
}
#app-mount .keybindShortcut-3zF1P9 span:active {
	box-shadow: inset 0 -2px 0 rgba(0, 0, 0, .6);
	border: 1px solid rgb(0, 0, 0);
	color: var(--header-secondary);
}
#app-mount .keybindShortcut-3zF1P9 span .bindArrow-EmK4SC g {
	fill: var(--header-primary);
}
#app-mount .keybindShortcut-3zF1P9 span:active .bindArrow-EmK4SC g {
	fill: var(--header-secondary);
}
#app-mount .keybindShortcutTipsSelect-2FpxFp:last-of-type::before {
	background-color: var(--interactive-muted);
}
#app-mount .tabButton-1hJ4oW {
	background-color: var(--text-muted);
	border: 1px solid rgb(0, 0, 0, .4);
	border-radius: 4px;
	box-shadow: inset 0 -4px 0 rgb(0, 0, 0, .4);
	color: var(--header-primary);
}
#app-mount .tabButton-1hJ4oW rect[fill="#4F545C"],
#app-mount .tabButton-1hJ4oW path[fill="#36393F"] {
	display: none;
}

/* ----		13.6.	QUICKSWITCHER					---- */

#app-mount .quickswitcher-pKcM9U {							/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: hidden;
}
.quickswitcher-pKcM9U::before,
.quickswitcher-pKcM9U::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.quickswitcher-pKcM9U::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.quickswitcher-pKcM9U::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	backdrop-filter: blur(var(--popoutblur));
}
.scroller-2qwVWY {
	background-color: transparent;
}
#app-mount .input-3r5zZY {									/* modal				input								*/
	background-color: rgba(var(--transparencycolor), .4);
	box-shadow: 0 2px 10px 0 rgba(var(--transparencycolor), .3);
}
#app-mount .resultFocused-3aIoYe {							/* modal				resultfocused						*/
	background-color: rgba(var(--transparencycolor), .2);
}

/* ----		13.7.	INVITEMODAL/GROUPCREATE			---- */

#app-mount .contentWrapper-3oy4Xo {								/* modal				guildinvitemodal				*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: hidden;
}
.contentWrapper-3oy4Xo::before,
.contentWrapper-3oy4Xo::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.contentWrapper-3oy4Xo::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.contentWrapper-3oy4Xo::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	backdrop-filter: blur(var(--popoutblur));
}

#app-mount .friendSelected-3cwmD7,								/* modal				groupdmrow						*/
#app-mount .inviteRow-3vmB7i:hover {							/* modal				guildrow						*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .friend-8ZraY7,										/* modal				groupdmrow						*/
#app-mount .inviteRowName-3H4s_c {								/* modal				username						*/
	color: var(--header-secondary);
}
#app-mount .friendSelected-3cwmD7,
#app-mount .inviteRow-3vmB7i:hover .inviteRowName-3H4s_c {
	color: var(--header-primary);
}
#app-mount .checkBoxLabel-16BK2g,
#app-mount .footerText-2QLGHU,
#app-mount .subTitle-3TUjmF,
#app-mount .subtitle-3v29zT,
#app-mount .subText-1CcYgq {
	color: var(--header-secondary);
}
.tag-15zcD_ {													/* modal				added user						*/
	background-color: rgb(var(--accentcolor));
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}
.pill-qMtBTq {
	background-color: rgba(var(--transparencycolor), .5);
}

/* ----		13.8.	LOGINSCREEN						---- */

#app-mount .wrapper-25sY58 {								/* login				wrapper								*/
	background: transparent;
}
.wrapper-25sY58::before,									/* login				winbuttonshadow						*/
.wrapper-25sY58 .rightSplit-24Bqk0,							/* login				background							*/
.wrapper-25sY58 .canvas-2dBZRV {							/* login				movingshadow						*/
	display: none;
}
#app-mount .authBox-1HR6Ha {								/* login				modal body							*/
	background-color: transparent;
	box-shadow: none;
	color: var(--text-muted);
	position: relative;
	overflow: hidden;
}
#app-mount .authBox-1HR6Ha.authBoxExpanded-AN2aH1 {			/* login				modal body expanded					*/
	background-color: rgba(var(--transparencycolor), .5);
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
}
#app-mount .navRow-dG-XX8 {									/* modal				modal footer						*/
	background-color: rgba(var(--transparencycolor), .2);
}

/* ----		13.9.	TERMACCEPTMODAL					---- */

#app-mount .modal-DRZfgq {									/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: hidden;
}
.modal-DRZfgq::before,
.modal-DRZfgq::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.modal-DRZfgq::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.modal-DRZfgq::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	backdrop-filter: blur(var(--popoutblur));
}

[style*="/assets/a13cfdd7220132fff399a76c3ed64519.svg"],	/* modal				image								*/
[src*="/assets/a13cfdd7220132fff399a76c3ed64519.svg"] {
	filter: brightness(85%) invert(100%);
	opacity: 0.7;
}

#app-mount .ack-3sCuAV {									/* modal				acklabel							*/
	color: var(--header-secondary);
}
#app-mount .buttonContainer-28osRq {						/* modal				footer								*/
	background-color: rgba(var(--transparencycolor), .2);
	box-shadow: none;
}

/* ----		13.10.	DOWNLOADAPPMODAL				---- */

#app-mount .downloadApps-14IgKV {							/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: hidden;
}
.downloadApps-14IgKV::before,
.downloadApps-14IgKV::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.downloadApps-14IgKV::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.downloadApps-14IgKV::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	backdrop-filter: blur(var(--popoutblur));
}
.downloadApps-14IgKV .header-1lOVWt {
	color: var(--text-normal);
}
.downloadApps-14IgKV .footer-2TRYcZ {
	color: var(--text-muted);
}
.downloadApps-14IgKV .platforms-15zUsJ .platform-1ZMvDu {
	border-color: var(--header-secondary);
}
.downloadApps-14IgKV .platforms-15zUsJ .platform-1ZMvDu p {
	color: var(--header-secondary);
}
.downloadApps-14IgKV .platforms-15zUsJ .platform-1ZMvDu .downloadButton-2XskEc {
	background-color: var(--header-secondary);
}
.downloadApps-14IgKV .platforms-15zUsJ .platform-1ZMvDu.active-1j5w_A .downloadButton-2XskEc {
	text-shadow: 1px 1px var(--textshadow);
}

/* ----		13.11.	GUILDBOOSTMODAL					---- */

#app-mount .perksModal-CLcR1c {								/* modal				wrapper								*/
	background-color: transparent;
}
.carouselContainer-2-vIZS {									/* modal				scrollercontainer					*/
	-webkit-mask: linear-gradient(to right, rgba(0,0,0,0) 0px, rgba(0,0,0,1) 60px, rgba(0,0,0,1) calc(100vw - 60px), rgba(0,0,0,0) 100vw);
}
.carouselGradientEdge-2W94ou {								/* modal				scrollergradient					*/
	display: none;
}
#app-mount .subscriberCount-3iRh_w {						/* modal				subcount							*/
	color: var(--header-secondary);
}
#app-mount .subscriberCount-3iRh_w strong {
	color: var(--text-normal);
}
#app-mount .moreSubscribers-2FZuij {						/* modal				suboverflow							*/
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--header-primary)
}

#app-mount .subscribersPopout-3lkZNO {						/* subpopout			container							*/
	background-color: transparent;
	box-shadow: 0 2px 10px rgba(var(--transparencycolor), .2);
	overflow: hidden;
}
.subscribersPopout-3lkZNO::before,
.subscribersPopout-3lkZNO::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.subscribersPopout-3lkZNO::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.subscribersPopout-3lkZNO::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.35));
	backdrop-filter: blur(var(--popoutblur));
}
#app-mount .subscribersPopoutUser-3Az2Dc {					/* subpopout			users								*/
	color: var(--header-secondary);
}

#app-mount .ctaBar-Nhk8yY {									/* current boost stats	container							*/
	position: relative;
	background-color: rgba(var(--transparencycolor), .4);
	background-image: none;
}
#app-mount .ctaBar-Nhk8yY::before {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	background-color: rgb(var(--accentcolor));
	-webkit-mask: url(https://discord.com/assets/94ff6fdc535b6ecb7b1bc54f2dd56a10.svg);
}
.guildIcon-3raYf3 {											/* current boost stats	guild icon							*/
	background-color: rgba(var(--transparencycolor), .2);
}

#app-mount .perk-2WeBWW {									/* modal				perkcard							*/
	background-color: rgba(var(--transparencycolor), .4);
}

#app-mount .headerLogo-2M4f14 {
	color: var(--header-primary);
}
#app-mount .tierHeaderLocked-3ItHYn {						/* modal				tierheaderlocked 					*/
	background-color: rgba(var(--transparencycolor), .4);
	color: var(--text-muted);
}
#app-mount .tierLock-1uBqZ0 {								/* modal				tierlock 							*/
	color: var(--interactive-muted);
}
#app-mount .tierHeaderUnlocked-1IvR2R {						/* modal				tierheaderunlocked 					*/
	background-color: rgba(var(--transparencycolor), .5);
}
#app-mount .tierBody-3ju-rc {								/* modal				tierbody 							*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .tierMarkerBackground-G8FoN4 {					/* modal				tiermilestone 						*/
	background: transparent;
}
#app-mount .tierMarkerInProgress-2Tdxjz {
	background: rgba(var(--transparencycolor), .3) !important;
}
#app-mount .selectedTier-24Xj0k .tierMarker-Vw1C95 {
	box-shadow: 0 4px 8px rgba(var(--transparencycolor), .24);
}
#app-mount .tierMarkerLabelText-1wk8KK:not(.isAccomplished-2NcqRT):hover {
	background: rgba(var(--transparencycolor), .3);
}
#app-mount .barBackground-unEPDT {							/* modal				tierbar 								*/
	background: linear-gradient(to right, rgba(0,0,0,0) 0%, rgba(0,0,0,0) 3%, rgba(var(--transparencycolor), .3) 3%, rgba(var(--transparencycolor), .3) 30.2%, rgba(0,0,0,0) 30.2%, rgba(0,0,0,0) 36.2%, rgba(var(--transparencycolor), .3) 36.2%, rgba(var(--transparencycolor), .3) 63.5%, rgba(0,0,0,0) 63.5%, rgba(0,0,0,0) 69.5%, rgba(var(--transparencycolor), .3) 69.5%, rgba(var(--transparencycolor), .3) 96.7%, rgba(0,0,0,0) 96.7%, rgba(0,0,0,0) 100%);
}
.barSecondary-VouwoY {
	background-color: rgb(var(--accentcolor));
}
.wrapper-3nSjSv .heading-4znNKq {							/* modal				boostaddwrapper header						*/
	text-shadow: 1px 1px var(--textshadow);
}
.tier-1EY-yj {												/* modal				boostaddwrapper tier						*/
	background-color: rgb(var(--transparencycolor), .3);
}
#app-mount .giftIcon-2kmx1K {								/* modal				gifticon							*/
	color: var(--header-secondary);
	margin: 0 18px;
}
#app-mount .button-f2h6uQ .giftIcon-2kmx1K {
	color: currentColor;
}
#app-mount .badgeIconWithoutSubscribers-1hjTfX {
	color: var(--text-muted);
}
#app-mount .tierPill-1yRO48 {
	background: rgba(var(--transparencycolor), .3);
	color: var(--header-primary);
}
#app-mount .tierPillStar-34rvoJ {
	color: var(--header-primary);
}
#app-mount .tierPillGem-3zcO2T {
	color: var(--interactive-muted);
}
#app-mount .tierPill-3gJ0eN {
	background: rgba(var(--transparencycolor), .3);
	color: var(--header-primary);
}
#app-mount .perk-2WeBWW {
	background: rgba(var(--transparencycolor), .2);
}

.header-1F6gxU {											/* prebuy popout		header								*/
	background: rgba(var(--transparencycolor), .3);
	padding-bottom: 10px;
	margin-bottom: 10px;
}
#app-mount .iconWrapper-2_MXbk {							/* prebuy popout		amount icon wrapper					*/
	background: rgba(var(--transparencycolor), .3);
}
.icon-2TbMdT:hover {										/* prebuy popout		amount icon							*/
	background: rgb(var(--accentcolor));
}
.upsellFooter-6EgwMe {										/* prebuy popout		footer details						*/
	background: rgba(var(--transparencycolor), .3);
}
.perksList-1vtwXn {											/* prebuy popout		perkslist							*/
	background: rgba(var(--transparencycolor), .3);
}

#app-mount .selectGuild-1Ygl76:hover {
	background-color: rgba(var(--transparencycolor), .3);
}

/* ----		13.12.	REACTIONSMODAL					---- */

#app-mount .scroller-2GkvCq {								/* modal				sidebar								*/
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .reactors-1VXca7 {								/* modal				list								*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .reactionDefault-1Sjj1f:hover {					/* modal				reaction							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .reactionSelected-1aMb2K {
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .remove-19AQn_ {									/* modal				remove								*/
	color: var(--interactive-normal);
}
#app-mount .remove-19AQn_:hover {
	background-color: rgba(var(--transparencycolor), .4);
	color: var(--interactive-hover);
}
#app-mount .discriminator-1DCM-o {							/* modal				discriminator						*/
	color: var(--text-muted);
}

/* ----		13.13.	GUILDTEMPLATEMODAL				---- */

.ctaSection-3LqbxQ {										/* modal				ctasection							*/
	background-color: transparent;
}
.formSection-23ecNl {										/* modal				formsection							*/
	background-color: transparent;
}

.usagePill-16kKHu {											/* modal				usagepill 1							*/
	background-color: rgba(var(--transparencycolor), .3);
}
.usagePill-P-Cmcv {											/* modal				usagePill 2							*/
	background-color: rgba(var(--transparencycolor), .3);
}

.channelsWrapper-51IUFR {									/* modal				channelswrapper						*/
	background-color: rgba(var(--transparencycolor), .3);
}

.rolesWrapper-1LLZrU {										/* modal				roleswrapper							*/
	background-color: rgba(var(--transparencycolor), .3);
}

#app-mount .role-2mCo-N {									/* modal				role								*/
	border-color: rgba(var(--textbrighter), .6);
	border-radius: 5px;
	padding: 0 5px;
	position: relative;
}
#app-mount .role-2mCo-N[style*="border-color: rgba(185, 187, 190, .6)"] {
	border-color: rgba(var(--textbrighter), .6) !important;
}
#app-mount .role-2mCo-N .roleName-3kJr77 {					/* modal				rolename							*/
	color: rgb(var(--textbrightest));
	margin: 0;
	font-weight: normal;
	position: relative;
	height: 20px;
	line-height: 20px;
	z-index: 1000;
	pointer-events: none;
}
#app-mount .role-2mCo-N .roleCircle-1ER2zO {				/* modal				rolecircle							*/
	position: absolute;
	background-color: rgb(var(--textbrighter));
	border-radius: 3px;
	opacity: 0.3;
	height: 100%;
	width: 100%;
	margin: 0;
	left: 0;
	top: 0;
}
#app-mount .role-2mCo-N .roleCircle-1ER2zO[style*="background-color: rgb(185, 187, 190)"] {
	background-color: rgb(var(--textbrighter)) !important;
}
#app-mount .role-2mCo-N .roleIcon-29epUq {
	z-index: 1;
}

/* ----		13.14.	GUILDWELCOMEMODAL				---- */

.optionContainer-yOpaLq {									/* modal				option								*/
	background-color: rgba(var(--transparencycolor), .2);
}
.optionContainer-yOpaLq:hover {
	background-color: rgba(var(--transparencycolor), .4);
}

/* ----		13.15.	GUILDRULESMODAL					---- */

.guildSidebar-UHnQqs {										/* modal				sidebar								*/
	background-color: rgba(var(--transparencycolor), .4);
}
.modal-2TOYtq {												/* modal				inner								*/
	background-color: rgba(var(--transparencycolor), .2);
}

/* ----		13.16.	GUILDFEEDBACKMODAL				---- */

.root-cw9rWQ {												/* modal				items								*/
	background-color: transparent;
	border-radius: 0;
}
.option-1O-Hwt {											/* modal				item								*/
	background-color: rgb(var(--transparencycolor), .2);
	border: none;
	border-radius: 8px;
	margin-bottom: 8px;
}
.option-1O-Hwt:hover {
	background-color: rgb(var(--transparencycolor), .4);
}

/* ----		13.17.	SCREENSHAREMODAL				---- */

#app-mount .sourceThumbnail-3n4cjJ {						/* modal				preview tiles						*/
	background-color: rgba(var(--transparencycolor), .4);
	box-shadow: 0 2px 5px rgba(var(--transparencycolor), .2), 0 0 0 1px rgba(var(--transparencycolor), .6);
}
.card-1SdQ2- {
	background-color: rgba(var(--transparencycolor), .2);
	border-color: rgba(var(--transparencycolor), .4);
}
#app-mount .item-2OyinQ {
	border-color: rgba(var(--transparencycolor), .4);
}
.selectorButton-3sW6Qm:not(.selectorButtonSelected-3Z0WNU) {
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .userListOverflow-2GkVmP {
	background: rgba(var(--transparencycolor), .5);
}

/* ----		13.18.	PHONEVERIFICATIONMODAL			---- */

.phoneField-3NAPDv {
	background-color: rgba(var(--transparencycolor), .2);
}
.phoneField-3NAPDv .inputField-1iYysB {
	background-color: transparent;
}
.phoneFieldPopout-3O-1C3 {
	position: absolute !important;
}

/* ----		13.19.	NOTIFICATIONSMODAL				---- */

#app-mount .channelName-IPB6B3 {
	color: var(--header-primary);
}
#app-mount .guildName-1kreI8,
#app-mount .override-1sK4r0,
#app-mount .overrideHighlight-3f-yyO {
	color: var(--header-secondary);
}
#app-mount .override-1sK4r0:hover {
	background-color: rgba(var(--backgroundtertiary),.1);
}
#app-mount .overrideHighlight-3f-yyO,
#app-mount .overrideHighlight-3f-yyO:hover {
	background-color: rgba(var(--backgroundtertiary),.3);
}
#app-mount .checkboxContainer-1NbL2v::before {
	background-color: rgba(var(--backgroundtertiary),.6);
}
#app-mount .overridePlaceholder-1nDEsX {
	border: 1px dashed var(--background-floating);
}

/* ----		13.20.	DISCOVERYENTRYMODAL				---- */

.checkboxWrapper-2fDzaA.row-31nALW {
	background-color: rgba(var(--transparencycolor),.2);
}
.checkboxWrapper-2fDzaA.row-31nALW:hover:not(.checked-1pZh2h) {
	background-color: rgba(var(--transparencycolor),.4);
}
.checkboxWrapper-2fDzaA.row-31nALW.checked-1pZh2h {
	background-color: rgb(var(--accentcolor));
}
.checkboxWrapper-2fDzaA.row-31nALW.checked-1pZh2h .colorStandard-21JIj7 {
	color: var(--header-primary);
}

/* ----		13.21.	NITROFEATUREMODAL				---- */

#app-mount .cardImageBackground-1zqQ8d {
	background: #000;
	opacity: 0.5;
}
#app-mount .cardInfo-62VDSb {
	background: rgba(var(--transparencycolor),.4);
}


/* ~~~~		14.		POPOUTS							~~~~ */

.layer-2aCOJ3:nth-child(1) {
	z-index: 1002;
}
.layer-2aCOJ3:nth-child(2) {
	z-index: 1003;
}
.layer-2aCOJ3:nth-child(3) {
	z-index: 1004;
}
.layer-2aCOJ3:nth-child(4) {
	z-index: 1005;
}
.layer-2aCOJ3:nth-child(5) {
	z-index: 1006;
}
.layer-2aCOJ3:nth-child(6) {
	z-index: 1007;
}
.layer-2aCOJ3:nth-child(7) {
	z-index: 1008;
}
.layer-2aCOJ3:nth-child(8) {
	z-index: 1009;
}
.layer-2aCOJ3:nth-child(9) {
	z-index: 1010;
}

#app-mount .loadingPopout-1feYe_,							/* loading popout											*/
#app-mount .container-18GwIk,								/* browser popout											*/
#app-mount .themedPopout-1TrfdI {							/* themed popout											*/
	background-color: transparent;
	border: none;
	border-radius: 5px;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	color: var(--header-primary);
	position: relative;
}
.loadingPopout-1feYe_::before,
.container-18GwIk::before,
.themedPopout-1TrfdI::before,
.loadingPopout-1feYe_::after,
.container-18GwIk::after,
.themedPopout-1TrfdI::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.loadingPopout-1feYe_::before,
.container-18GwIk::before,
.themedPopout-1TrfdI::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.loadingPopout-1feYe_::after,
.container-18GwIk::after,
.themedPopout-1TrfdI::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}

.selected-22ukbQ,											/* popout				combobox selected					*/
.selected-22ukbQ:hover {
	background-color: rgb(var(--accentcolor));
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}
#app-mount .divider-MRAL1L {								/* popout				divider								*/
	border-color: var(--background-modifier-accent);
}

/* ----		14.1.	CONTEXTMENU						---- */

.styleFlexible-x0_sIC,										/* contextmenu			flexible							*/
.styleFixed-2_NfVL,											/* contextmenu			fixed								*/
.submenu-1apzyU {											/* contextmenu			submenu								*/
	background: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
}
.styleFlexible-x0_sIC::before,
.styleFixed-2_NfVL::before,
.submenu-1apzyU::before,
.styleFlexible-x0_sIC::after,
.styleFixed-2_NfVL::after,
.submenu-1apzyU::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 4px;
	pointer-events: none;
	z-index: -1;
}
.styleFlexible-x0_sIC::before,
.styleFixed-2_NfVL::before,
.submenu-1apzyU::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.styleFlexible-x0_sIC::after,
.styleFixed-2_NfVL::after,
.submenu-1apzyU::after {
	background: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.3));
	backdrop-filter: blur(var(--popoutblur));
}
.submenu-1apzyU {
	position: relative;
}
.container-3AL15u {											/* contextmenu			searchbar							*/
	background-color: rgba(var(--transparencycolor), .2);
}
.item-1OdjEX.colorDefault-CDqZdO.focused-3qFvc8,
.item-1OdjEX.colorDefault-CDqZdO:hover:not(.hideInteraction-2jPGL_) {
	background-color: rgba(var(--transparencycolor), .2) !important;
}
.item-1OdjEX.colorDanger-3n-KnP.focused-3qFvc8,
.item-1OdjEX.colorDanger-3n-KnP:hover:not(.hideInteraction-2jPGL_) {
	background-color: rgba(var(--dangercolor), .2) !important;
}
.item-1OdjEX.colorBrand-3cPPsm.focused-3qFvc8,
.item-1OdjEX.colorBrand-3cPPsm:hover:not(.hideInteraction-2jPGL_),
.item-1OdjEX.colorDefault-CDqZdO.focused-3qFvc8[id="user-settings-cog-Subscriptions"],
.item-1OdjEX.colorDefault-CDqZdO:hover:not(.hideInteraction-2jPGL_)[id="user-settings-cog-Subscriptions"],
.item-1OdjEX.colorDefault-CDqZdO.focused-3qFvc8[id="user-settings-cog-Discord_Nitro"],
.item-1OdjEX.colorDefault-CDqZdO:hover:not(.hideInteraction-2jPGL_)[id="user-settings-cog-Discord_Nitro"] {
	background-color: rgba(var(--accentcolor), .2) !important;
}
.item-1OdjEX.colorPremium-vwmYZQ.focused-3qFvc8,
.item-1OdjEX.colorPremium-vwmYZQ:hover:not(.hideInteraction-2jPGL_),
.item-1OdjEX.colorDefault-CDqZdO.focused-3qFvc8[id="user-settings-cog-Nitro_Server_Boost"],
.item-1OdjEX.colorDefault-CDqZdO:hover:not(.hideInteraction-2jPGL_)[id="user-settings-cog-Nitro_Server_Boost"],
.item-1OdjEX.colorDefault-CDqZdO.focused-3qFvc8[id="guild-context-guild-settings--GUILD_PREMIUM"],
.item-1OdjEX.colorDefault-CDqZdO:hover:not(.hideInteraction-2jPGL_)[id="guild-context-guild-settings--GUILD_PREMIUM"] {
	background-color: rgba(var(--accentcolor2), .2) !important;
}
#app-mount .item-1OdjEX .checkbox-hADx5o {					/* contextmenu			checkbox 							*/
	color: rgb(var(--accentcolor));
}
#app-mount .item-1OdjEX.colorDanger-3n-KnP .checkbox-hADx5o {
	color: rgb(var(--dangercolor));
}
#app-mount .item-1OdjEX .check-3HZJs4 {						/* contextmenu			checkmark 							*/
	color: #fff;
	stroke: var(--textshadow);
}
.button-1zW0-r {											/* contextmenu			quick reaction button				*/
	background-color: rgba(var(--transparencycolor), .3);
}
.button-1zW0-r:hover {
	background-color: rgb(var(--accentcolor));
}

/* ----		14.2.	USERPOPOUT						---- */

.userPopout-2j1gM4 {										/* popout				container							*/
	background: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
}
.userPopout-2j1gM4::before,
.userPopout-2j1gM4::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.userPopout-2j1gM4::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.userPopout-2j1gM4::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}
#app-mount .headerTop-3GPUSF,								/* popout				header inner						*/
#app-mount .activity-1gTu-L,								/* popout				activity							*/
#app-mount .aboutMeSection-PUghFQ {							/* popout				about me section					*/
	background: transparent;
	border: transparent;
}
#app-mount .activity-1gTu-L {
	padding: 0 16px 16px;
}
.userPopout-2j1gM4 .banner-1YaD3N {							/* popout				banner								*/
	-webkit-mask: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="2400" height="120" viewBox="0 0 2400 120" fill="none"><path fill="black" d="M 0 0 L 0 120 L 16 120 A 46 46 0 0 1 62 76 A 46 46 0 0 1 108 120 L 2400 120 L 2400 0 L 0 0 z"/></svg>') bottom left no-repeat;
}
.userPopout-2j1gM4 .avatar-2Vndt_,							/* popout				avatar								*/
.userPopout-2j1gM4 .avatarWrapper {							/* popout				status everywhere					*/
	background-color: transparent;
	border-color: transparent;
	box-sizing: content-box;
}

#app-mount .body-2wLx-E,									/* popout				body								*/
#app-mount .bodyInnerWrapper-2bQs1k,						/* popout				body inner							*/
#app-mount .footer-3naVBw {									/* popout				footer								*/
	background-color: transparent;
	color: var(--header-secondary);
}

.root-jbEB5E {												/* body					roles								*/
	max-height: 100px;
	overflow-x: hidden;
	overflow-y: scroll;
}
#app-mount .root-jbEB5E::-webkit-scrollbar {
	width: 4px;
}
#app-mount .role-2TIOKu {									/* body					role								*/
	border-color: rgba(var(--textbrighter), .6);
	border-radius: 5px;
	padding: 0 5px;
	position: relative;
}
#app-mount .role-2TIOKu[style*="border-color: rgba(185, 187, 190, .6)"] {
	border-color: rgba(var(--textbrighter), .6) !important;
}
#app-mount .role-2TIOKu .roleName-2ZJJYR {					/* body					rolename							*/
	color: rgb(var(--textbrightest));
	margin: 0;
	font-weight: normal;
	position: relative;
	height: 20px;
	line-height: 20px;
	z-index: 1000;
	pointer-events: none;
}
#app-mount .role-2TIOKu .roleCircle-1EgnFN {				/* body					rolecircle							*/
	position: absolute;
	background-color: rgb(var(--textbrighter));
	border-radius: 3px;
	opacity: 0.3;
	height: 100%;
	width: 100%;
	margin: 0;
	left: 0;
	top: 0;
}
#app-mount .role-2TIOKu .roleCircle-1EgnFN[style*="background-color: rgb(185, 187, 190)"] {
	background-color: rgb(var(--textbrighter)) !important;
}
#app-mount .role-2TIOKu .roleCircle-1EgnFN:not(:empty):hover {
	opacity: 1;
	z-index: 2000;
	cursor: pointer;
}
#app-mount .role-2TIOKu .roleIcon-29epUq {
	z-index: 1;
}

.textarea-_59yqs:focus {									/* body					note 								*/
	background-color: rgba(var(--transparencycolor), .2);
}

.wumpusWrapper-2-V9io {										/* footer				wumpus new user 					*/
	margin-top: 27px;
}
#app-mount .wumpusTooltip-mj7eo0 {
	background-color: rgb(var(--accentcolor));
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}
#app-mount .wumpusTooltip-mj7eo0::after {
	border-color: transparent rgb(var(--accentcolor)) transparent transparent;
}

/* ----		14.3.	EMOJIPICKER						---- */

.contentWrapper-3vHNP2,										/* picker				expression wrapper					*/
.emojiPicker-6YCk8a,										/* picker				inner								*/
.diversitySelectorOptions-3DhNYs {							/* picker				diversityselector					*/
	background: transparent;
	box-shadow: 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	overflow: hidden;
}
.contentWrapper-3vHNP2::before,
.emojiPicker-6YCk8a::before,
.diversitySelectorOptions-3DhNYs::before,
.contentWrapper-3vHNP2::after,
.emojiPicker-6YCk8a::after,
.diversitySelectorOptions-3DhNYs::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.contentWrapper-3vHNP2::before,
.emojiPicker-6YCk8a::before,
.diversitySelectorOptions-3DhNYs::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.contentWrapper-3vHNP2::after,
.emojiPicker-6YCk8a::after,
.diversitySelectorOptions-3DhNYs::after {
	background: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}
.diversitySelectorOptions-3DhNYs::before,
.diversitySelectorOptions-3DhNYs::after {
	border-radius: 5px;
}
.emojiPickerInExpressionPicker-2nOwH8 .emojiPicker-6YCk8a {
	box-shadow: unset;
}
.emojiPickerInExpressionPicker-2nOwH8 .emojiPicker-6YCk8a::after,
.emojiPickerInExpressionPicker-2nOwH8 .emojiPicker-6YCk8a::before {
	display: none;
}

.diversityEmojiItem-2bgZKv:hover {							/* picker				diversityemoji						*/
	background-color: rgb(var(--accentcolor));
}

.navButtonActive-1EqC5l {									/* picker				navbuttonactive						*/
	background-color: rgb(var(--accentcolor));
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}

.wrapper-22rqw6 {											/* picker				sidebar								*/
	background-color: rgba(var(--transparencycolor), .2);
}

.guildIcon-2SUGiq {											/* picker				guildicon							*/
	background-color: rgba(var(--transparencycolor), .2);
}

.categoryItemDefaultCategory-3haEDq:first-child,
.categoryItemDefaultCategory-3haEDq:first-child + .categoryItemDefaultCategory-3haEDq,
.stickerCategoryRecent-1WVWrj {
	margin-bottom: 8px;
}
.categoryItemDefaultCategory-3haEDq:hover,					/* picker				categoryitem						*/
.stickerCategory-2f6iSo:hover,								/* picker				stickercategoryitem					*/
.stickerCategoryShopWrapper-3EnJdQ:hover .stickerCategoryShop-d5zC3B {
	background-color: rgba(var(--transparencycolor), .3);
}
.categoryItemDefaultCategorySelected-2YeRUu,				/* picker				categoryitem selected				*/
.categoryItemDefaultCategorySelected-2YeRUu:hover,		
.stickerCategorySelected-2uaMAG,							/* picker				stickercategoryitem selected		*/
.stickerCategorySelected-2uaMAG:hover {
	background-color: rgb(var(--accentcolor));
}
.categoryItemDefaultCategorySelected-2YeRUu svg,			/* picker				categoryitem selected				*/
.categoryItemDefaultCategorySelected-2YeRUu:hover svg,
.stickerCategorySelected-2uaMAG svg,						/* picker				stickercategoryitem selected		*/
.stickerCategorySelected-2uaMAG:hover svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}

.unicodeShortcut-3N8oDe,									/* picker				unicodeemojis shortcut				*/
.stickerCategoryShopWrapper-3EnJdQ {						/* picker				unicodeemojis shortcut				*/
	background-color: transparent;
	border: none;
	overflow: hidden;
	z-index: 100;
}
.unicodeShortcut-3N8oDe::before,
.stickerCategoryShopWrapper-3EnJdQ::before,
.unicodeShortcut-3N8oDe::after,
.stickerCategoryShopWrapper-3EnJdQ::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.unicodeShortcut-3N8oDe::before,
.stickerCategoryShopWrapper-3EnJdQ::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.unicodeShortcut-3N8oDe::after,
.stickerCategoryShopWrapper-3EnJdQ::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.35));
	backdrop-filter: blur(var(--popoutblur));
}

.inspector-DFKXwB {											/* picker				emojiinfowrapper					*/
	background-color: rgba(var(--transparencycolor), .2);
}

#app-mount .wrapper-1NNaWG {								/* picker				categoryheader						*/
	background: transparent;
	position: static;
}

#app-mount .imageLoading-2uloYN {							/* picker				emoji loading						*/
	background: rgba(var(--transparencycolor), .3);
	border-radius: 10px;
}
.emojiItem-277VFM.emojiItemSelected-2Lg50V {				/* picker				emoji selected						*/
	background-color: rgb(var(--accentcolor));
}
.emojiItemDisabled-3VVnwp {									/* picker				emoji disabled						*/
	filter: none;
	cursor: no-drop;
}
.emojiItemDisabled-3VVnwp > * {
	filter: grayscale(1);
}

.shape-2kfO2v {												/* picker				sticker loading						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.feature-1nRVr5 {											/* picker				sticker feature						*/
	background: transparent;
}

.stickerInspected-mwnU6w .stickerBackground-2XECKi {		/* picker				sticker focused						*/
	background-color: rgb(var(--accentcolor));
}
.viewAllBackground-3Bn1vh {									/* picker				sticker view all					*/
	background-color: rgba(var(--transparencycolor), .2);
}
.viewAll-1MwRpl:hover .viewAllBackground-3Bn1vh,
.viewAllInspected-25Y7ds .viewAllBackground-3Bn1vh {
	background-color: rgba(var(--transparencycolor), .4);
}

.premiumPromo-1eKAIB {										/* picker				premium warning						*/
	background-color: transparent;
	opacity: 1;
}
.premiumPromo-1eKAIB::before,
.premiumPromo-1eKAIB::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	opacity: 0.9;
	pointer-events: none;
	z-index: -1;
}
.premiumPromo-1eKAIB::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.premiumPromo-1eKAIB::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.29));
	backdrop-filter: blur(var(--popoutblur));
}
.premiumPromoClose-Nuntxy {
	-webkit-mask: url(https://discord.com/assets/f815a774c2b98d3109293a4e2afb733c.svg) 50% 50% no-repeat;
	background: var(--interactive-normal);
}
.premiumPromoClose-Nuntxy:hover {
	background: var(--interactive-hover);
}
.premiumPromoClose-Nuntxy:active {
	background: var(--interactive-active);
}
#app-mount .categoryItemDefaultCategorySelected-2YeRUu .categoryIcon-2cYeku,
#app-mount .categoryItemDefaultCategorySelected-2YeRUu:hover .categoryIcon-2cYeku {
	color: var(--interactive-active);
}

#app-mount .focused-q9B2e4,									/* gifpicker			result								*/
#app-mount .result-3OpoO7:hover {
	box-shadow: 0 11px 22px 1px rgba(var(--transparencycolor), .3);
}
#app-mount .placeholder-2Mfkde {
	background: rgba(var(--textdarkest),.6);
}
#app-mount .endContainer-3FEUTM::after {
	background-image: url(https://discord.com/assets/0c735bf91232f2a2266e6ba9d6753565.svg);
	opacity: 0.6;
}
#app-mount .endText-3HHsVy {
	color: var(--header-secondary);
}
#app-mount .emptyHintCard-3Btf0V {
	background-color: rgba(var(--transparencycolor), .2);
	color: var(--header-secondary);
}
#app-mount .backButton-3D5utk {								/* gifpicker			backbutton							*/
	color: var(--interactive-normal);
}
#app-mount .backButton-3D5utk:hover {
	color: var(--interactive-hover);
}
#app-mount .backButton-3D5utk:active {
	color: var(--interactive-active);
}


/* ----		14.4.	PINS/MENTIONS					---- */

.messagesPopoutWrap-3zryHW,								/* popout				wrapper								*/
.container-2ebMPP {										/* popout				wrapper	(inbox)						*/
	background-color: transparent;
	box-shadow: 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	overflow: hidden;
}
.messagesPopoutWrap-3zryHW > *,
.container-2ebMPP > * {
	z-index: 1000;
}
.messagesPopoutWrap-3zryHW::before,
.container-2ebMPP::before,
.messagesPopoutWrap-3zryHW::after,
.container-2ebMPP::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.messagesPopoutWrap-3zryHW::before,
.container-2ebMPP::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.messagesPopoutWrap-3zryHW::after,
.container-2ebMPP::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}
#app-mount .messagesPopout-eVzQcI {							/* popout				innerwrap							*/
	background-color: transparent;
}

.themedPopout-1TrfdI .header-2Kf7Yu {
	box-shadow: 0 2px 3px 0 rgba(var(--transparencycolor), .1);
}
.header-1w9Q93 {											/* popout				header								*/
	background-color: rgba(var(--transparencycolor), .2);
	box-shadow: 0 2px 3px 0 rgba(var(--transparencycolor), .2);
}

.themedPopout-1TrfdI .footer-1K57q_ {
	background-color: rgba(var(--transparencycolor), .1);
}
.footer-5ji8u1 {											/* popout				footer								*/
	background-color: rgba(var(--transparencycolor), .2);
}

.messageGroupWrapper-1jf_7C {
	background-color: transparent;
	border: none;
	overflow: visible;
	padding: 11px 10px 10px 10px;
}
.messageGroupWrapper-1jf_7C + .messageGroupWrapper-1jf_7C::before {
	content: "";
	border-top: 1px solid var(--background-modifier-accent);
	position: absolute;
	top: -3px;
	left: 0;
	width: 100%;
}
.messageGroupWrapper-1jf_7C .contentCozy-3XX413 {
	overflow: hidden;
}
.actionButtons-2mNSAB {										/* popout				actionbuttonscontainer				*/
	top: 4px;
	right: 14px;
}
.jumpButton-1V_1FA,											/* popout				jumpbutton (mentions)				*/
.jumpButton-1ZwI_j {										/* popout				jumpbutton (pins)					*/
	background-color: rgba(var(--transparencycolor), .4);
}
.jumpButton-1V_1FA:hover,
.jumpButton-1ZwI_j:hover {
	background-color: rgb(var(--accentcolor));
}
.jumpButton-1V_1FA + .jumpButton-1V_1FA,
.jumpButton-1ZwI_j + .jumpButton-1ZwI_j {
	margin-left: 2px;
}
.messageGroupWrapper-1jf_7C:hover .actionButtons-2mNSAB .closeButton-17RIVZ {
	opacity: 1;
}
.hasMoreButton-1MELpI {										/* popout				hasmorebutton						*/
	background-color: rgba(var(--transparencycolor), .2);
	border: none;
}

.image-t6rLT3 {												/* popout				emptyimage							*/
	opacity: 0.6;
}

															/* popout				active tab							*/
#app-mount .header-145e10 .tabBar-1qdMr5 .tab-TRrPC8.active-1grPyy {
	background-color: rgb(var(--accentcolor));
}
.secondary-2bzKEX,											/* popout				header button						*/
.tertiary-1e-lAP,											/* popout				message button						*/
.collapseButton-3V3Cqh {									/* popout				collapse button						*/
	background-color: rgba(var(--transparencycolor), .2);
}
.secondary-2bzKEX:hover,
.tertiary-1e-lAP:hover,
.collapseButton-3V3Cqh:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
.collapseButton-3V3Cqh {
	position: static;
	margin-left: 12px;
	border-radius: 32px;
	box-sizing: border-box;
	cursor: pointer;
	flex-shrink: 0;
	height: 32px;
	min-height: 32px;
	width: 32px;
	min-width: 32px;
	padding: 8px;
	transform: unset !important;
}
.collapseButton-3V3Cqh.collapsed-b6uSCG svg {
	transform: rotate(-90deg);
}

.channelHeader-DFRX8q {										/* popout				channelheader						*/
	background-color: rgba(var(--transparencycolor), .4);
	padding-right: 16px;
	border-radius: 5px 5px 0 0;
	position: static;
}
.channelHeader-DFRX8q:only-child {
	border-radius: 0;
}
.messageContainer-3VTXBC,									/* popout				messagecontainer					*/
.messages-23can0 {											/* popout				messagecontainer (inbox)			*/
	background-color: rgba(var(--transparencycolor), .2);
	border-radius: 0;
}
.messageContainer-3VTXBC:last-child,
.messages-23can0:last-child {
	border-radius: 0 0 5px 5px;
}

.tutorial-Nb3Zz5 {											/* popout				tutorial (inbox)					*/
	background-color: rgba(var(--transparencycolor), .4);
}
.tutorialIcon-25VF3Q {										/* popout				tutorial (inbox)					*/
	background-color: rgba(var(--transparencycolor), .4);
}

/* ----		14.5.	SEARCHPOPOUT					---- */

#app-mount .container-2McqkF {								/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	overflow: hidden;
	position: relative;
}
.container-2McqkF::before,
.container-2McqkF::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.container-2McqkF::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.container-2McqkF::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}
#app-mount .queryContainer-ZunrLZ {
	border-bottom-color: var(--background-modifier-accent);
	color: var(--header-secondary);
}
#app-mount .queryContainer-ZunrLZ strong {
	color: var(--header-primary);
}
#app-mount .focused-2FU0YH {
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .resultsGroup-1BPR25::before {
	border-top-color: var(--background-modifier-accent);
}
#app-mount .resultsGroup-1BPR25 .header-3A13BX,
#app-mount .resultsGroup-1BPR25 .plusIcon-2V7coV,
#app-mount .resultsGroup-1BPR25 .searchClearHistory-2Be-92,
#app-mount .resultsGroup-1BPR25 .searchLearnMore-7__o_n a {
	color: var(--text-normal);
}
#app-mount .resultsGroup-1BPR25 .header-3A13BX,
#app-mount .resultsGroup-1BPR25 .plusIcon-2V7coV {
	color: var(--text-normal);
}
#app-mount .option-ayUoaq::after {
	display: none;
}
#app-mount .option-ayUoaq:hover,
#app-mount .option-ayUoaq.selected-rZcOL- {
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .option-ayUoaq:hover::before,
#app-mount .option-ayUoaq.selected-rZcOL-::before {
	background-color: rgb(var(--accentcolor));
	border-radius: 3px;
	width: 34px;
}
#app-mount .option-ayUoaq:hover .plusIcon-2V7coV,
#app-mount .option-ayUoaq.selected-rZcOL- .plusIcon-2V7coV {
	color: white;
	opacity: 1;
}
#app-mount .option-ayUoaq .answer-2fBfuP,
#app-mount .option-ayUoaq .nonText-3_4gtu,
#app-mount .option-ayUoaq strong {
	color: var(--text-normal);
}
#app-mount .option-ayUoaq .filter-5YbOzJ {
	color: var(--text-muted);
}
#app-mount .option-ayUoaq.user-23VtPS .displayedNick-2dDbfG {
	color: var(--text-normal);
}
#app-mount .option-ayUoaq.user-23VtPS .displayUsername-14aOpK {
	color: var(--interactive-muted);
}
#app-mount .searchOption-351dTI .filter-5YbOzJ {
	color: var(--text-normal);
}
#app-mount .searchOption-351dTI .answer-2fBfuP {
	color: var(--text-muted);
}
#app-mount .searchResultChannelCategory-3cL8uG,
#app-mount .searchResultChannelIcon-1Il1Qo {
	color: var(--text-muted);
}

#app-mount .calendarPicker-sDhzdi .react-datepicker {
	background: transparent;
}
#app-mount .calendarPicker-sDhzdi .react-datepicker__day:not(.react-datepicker__day--outside-month) {
	border-color: rgba(var(--transparencycolor), .5);
}
#app-mount .calendarPicker-sDhzdi .react-datepicker__day--outside-month {
	background: rgba(var(--transparencycolor), .5);
	border-color: transparent;
}
#app-mount .calendarPicker-sDhzdi .react-datepicker__header,
#app-mount .calendarPicker-sDhzdi .react-datepicker__month-container,
#app-mount .calendarPicker-sDhzdi .react-datepicker__day--disabled:not(.react-datepicker__day--outside-month) {
	background: rgba(var(--transparencycolor), .2);
}
#app-mount .calendarPicker-sDhzdi .react-datepicker__header {
	padding-bottom: 5px;
}
#app-mount .calendarPicker-sDhzdi .react-datepicker__navigation {
	background: transparent;
	border-color: rgba(var(--textbrightest), .5);
	top: 30px;
}
#app-mount .calendarPicker-sDhzdi .react-datepicker__navigation::before {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	-webkit-mask: url(https://discord.com/assets/7619529e87dad31fd2ae83d9b9583e49.svg) center/6px 12px no-repeat;
	background-color: rgb(var(--textbrightest));
}
#app-mount .calendarPicker-sDhzdi .react-datepicker__navigation--previous {
	left: 30px;
}
#app-mount .calendarPicker-sDhzdi .react-datepicker__navigation--next {
	right: 30px;
}
#app-mount .calendarPicker-sDhzdi .react-datepicker__current-month {
	border-color: transparent;
	padding: 10px 0;
}
#app-mount .calendarPicker-sDhzdi .react-datepicker__current-month,
#app-mount .calendarPicker-sDhzdi .react-datepicker__day-name,
#app-mount .calendarPicker-sDhzdi .react-datepicker__day:not(.react-datepicker__day--disabled):hover,
#app-mount .calendarPicker-sDhzdi .react-datepicker__day:not(.react-datepicker__day--disabled):not(.react-datepicker__day--outside-month),
#app-mount .calendarPicker-sDhzdi .datePickerHint-17MnA8 .hint-3D5yHh,
#app-mount .calendarPicker-sDhzdi .datePickerHint-17MnA8 .hintValue-1x-flY {
	color: var(--header-primary);
}
#app-mount .calendarPicker-sDhzdi .react-datepicker__day--disabled:not(.react-datepicker__day--outside-month) {
	color: var(--header-secondary);
}
#app-mount .calendarPicker-sDhzdi .react-datepicker__day--outside-month {
	color: var(--text-muted);
}
#app-mount .datePicker-70cO23 .datePickerHint-17MnA8 {
	margin: 0;
	padding: 20px;
	display: flex;
	justify-content: center;
	border-top-color: var(--background-modifier-accent);
}
#app-mount .datePicker-70cO23 .datePickerHint-17MnA8 .hint-3D5yHh {
	color: var(--text-normal);
}
#app-mount .datePicker-70cO23 .datePickerHint-17MnA8 .hintValue-1x-flY {
	color: var(--header-primary);
}
#app-mount .datePicker-70cO23 .datePickerHint-17MnA8 .hintValue-1x-flY:hover {
	text-shadow: 1px 1px var(--textshadow);
}

/* ----		14.6.	COLORPICKER						---- */

#app-mount .colorPickerCustom-1swUKF {						/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
}
.colorPickerCustom-1swUKF::before,
.colorPickerCustom-1swUKF::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.colorPickerCustom-1swUKF::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.colorPickerCustom-1swUKF::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.35));
	backdrop-filter: blur(var(--popoutblur));
}

/* ----		14.7.	ADDROLE							---- */

#app-mount .container-2O1UgZ,								/* popout				userpopout							*/
#app-mount .container-1S70rv {								/* popout				channelsettings						*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	width: 300px;
}
.container-2O1UgZ::before,
.container-2O1UgZ::after,
.container-1S70rv::before,
.container-1S70rv::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.container-2O1UgZ::before,
.container-1S70rv::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.container-2O1UgZ::after,
.container-1S70rv::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.1));
	backdrop-filter: blur(var(--popoutblur));
}
.focused-qp-W9B,
.item-1BCeuB:hover:not(.disabled-Mmpvl7),
.row-1Ib2uD.selected-1IWCoj .rowInner-3uonq8,
.row-1Ib2uD:hover .rowInner-3uonq8 {
	background: rgba(var(--transparencycolor), .4);
}
#app-mount .container-1S70rv .header-3i_Csh {
	background: rgba(var(--transparencycolor), .2);
}
#app-mount .container-1S70rv .input-2lpFVz {
	color: var(--header-primary);
}
#app-mount .container-1S70rv .sectionTag-28mLyE {
	background: transparent;
}
.autocompleteShadow-2nfsSy,
.autocompleteArrowWrapper-Kr4DnW,
.autocompleteHeaderBackground-3u7TwO {
	display: none;
}


/* ----		14.8.	EVERYONEMENTION					---- */

#app-mount .everyonePopout-nEbJY3 {							/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.everyonePopout-nEbJY3::before,
.everyonePopout-nEbJY3::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.everyonePopout-nEbJY3::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.everyonePopout-nEbJY3::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.1));
	backdrop-filter: blur(var(--popoutblur));
}
#app-mount .header-3_S6dz {
	color: var(--header-primary);
}
#app-mount .body-2iXqIL {
	color: var(--header-secondary);
}
#app-mount .body-2iXqIL .animation-3GofIz {
	opacity: .5;
}
#app-mount .buttonHint-2OxJB8 {
	color: var(--text-muted);
}
#app-mount .buttonHint-2OxJB8 strong {
	color: var(--header-secondary);
}
#app-mount .footer-2aTx0s {
	background-color: rgba(var(--transparencycolor), .2);
	color: var(--text-muted);
}
#app-mount .footer-2aTx0s strong {
	color: var(--header-secondary);
}


/* ----		14.9.	CHANNELFOLLOW					---- */

#app-mount .header-13P3fr {
	background: rgba(var(--transparencycolor), .3);
}
#app-mount .separator-3gy7tq {
	box-shadow: 0 1px 0 0 rgba(var(--transparencycolor), .3), 0 1px 2px 0 rgba(var(--transparencycolor), .3);
}
.channelContainer-3YAhb_ {
	background-color: rgba(var(--transparencycolor), .3);
}
.channel-k2TVLQ {
	background-color: rgba(var(--transparencycolor), .3);
}
.channelContainer-3YAhb_ .channel-k2TVLQ {
	background-color: transparent;
}

/* ----		14.10.	CHANNELFOLLOWINFO				---- */

#app-mount .guildPopout-G6M0fK {							/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.guildPopout-G6M0fK::before,
.guildPopout-G6M0fK::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.guildPopout-G6M0fK::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.guildPopout-G6M0fK::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.1));
	backdrop-filter: blur(var(--popoutblur));
}

/* ----		14.11.	EMOJIINFO						---- */

#app-mount .popoutContainer-2wbmiM {						/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.popoutContainer-2wbmiM::before,
.popoutContainer-2wbmiM::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.popoutContainer-2wbmiM::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.popoutContainer-2wbmiM::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	backdrop-filter: blur(var(--popoutblur));
}

.emojiSection-3QtaWO {										/* popout				emojisection						*/
	background-color: transparent;
}

.guildSection-2Zyzy8 {										/* popout				emojisection						*/
	background-color: rgba(var(--transparencycolor), .2);
}

.loading-1lSwpg {											/* popout				loading placeholder					*/
	background: rgba(var(--transparencycolor), .3);
}

/* ----		14.12.	STREAMPREVIEW					---- */

#app-mount .streamPreview-3qoMP4 {							/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.streamPreview-3qoMP4::before,
.streamPreview-3qoMP4::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.streamPreview-3qoMP4::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.streamPreview-3qoMP4::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	backdrop-filter: blur(var(--popoutblur));
}

#app-mount .previewContainer-21fFBz	{						/* popout				preview								*/
	background-color: rgba(var(--transparencycolor), .2);
}

/* ----		14.13.	STREAMINFO						---- */

#app-mount .container-8Futzw {								/* modal				container							*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: visible !important;
}
.container-8Futzw::before,
.container-8Futzw::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.container-8Futzw::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.container-8Futzw::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	backdrop-filter: blur(var(--popoutblur));
}

/* ----		14.14.	PUBLICGUILDANNOUNCEMENT			---- */

#app-mount .popout-AVsFMl {									/* popout				wrapper								*/
	background-color: transparent;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	border: none;
	border-radius: 3px;
	overflow: hidden;
	position: relative;
}
.popout-AVsFMl::before,
.popout-AVsFMl::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.popout-AVsFMl::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.popout-AVsFMl::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	backdrop-filter: blur(var(--popoutblur));
}

/* ----		14.15.	RTCSTATUSPOPOUT					---- */

#app-mount .container-1ILvLB {								/* RTCpopout												*/
	background-color: transparent;
	border: none;
	border-radius: 5px;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	color: var(--header-primary);
	position: relative;
	width: 260px;
}
.container-1ILvLB::before,
.container-1ILvLB::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.container-1ILvLB::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.container-1ILvLB::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}
#app-mount .container-1ILvLB .header-2C89wJ {
	background-color: rgba(var(--transparencycolor), .2);
	color: var(--header-primary);
}
#app-mount .container-1ILvLB canvas {
	background-color: rgb(var(--transparencycolor));
	padding: 5px;
	border-radius: 5px;
}
#app-mount .container-1ILvLB section {
	background-color: transparent;
}
#app-mount .container-1ILvLB section p {
	color: var(--header-primary);
}
#app-mount .container-1ILvLB section strong {
	color: var(--header-primary);
}
#app-mount .debugButton-OTfjlB {
	color: var(--header-secondary);
}
#app-mount .krispLogo-aWHaan {
	-webkit-mask: url(https://discord.com/assets/c28317e203e00b2d7390d5ece2399228.svg) center/contain no-repeat;
	background-color: var(--header-primary);
}

/* ----		14.16.	PHONE-/EMAILVALIDATION			---- */

#app-mount .input-3NIgDw {
	background-color: rgba(var(--transparencycolor), .2);
	color: var(--header-primary);
}
#app-mount .phoneFieldPopout-h7c9mt .countryName-3dA1Xv {
	color: var(--header-secondary);
}
#app-mount .phoneFieldPopout-h7c9mt .countryCode-2RFA3i {
	color: var(--header-primary);
}
#app-mount .activityInviteEducationArrow-1Avyhe {
	-webkit-mask: url(https://discord.com/assets/ba018cf9baa19824316dc4c2beb080a4.svg) center/contain no-repeat;
	background: var(--header-primary);
}

#app-mount .emailVerificationModal-D8InhA .title-3Z7qoP {
	color: var(--header-primary);
}
#app-mount .emailVerificationModal-D8InhA .body-2WAVf7 {
	color: var(--text-muted);
}

#app-mount .verification-2oQUwN .image-cLINxN {
	background-image: url(https://discord.com/assets/c290235278e128e94ae5ac37e58c5cbb.svg);
	opacity: .5;
}
#app-mount .verification-2oQUwN .title-rdZnFE {
	color: var(--header-primary);
}
#app-mount .verification-2oQUwN .body-2IbMjQ,
#app-mount .verification-2oQUwN .footer-3YDDp6 {
	color: var(--header-secondary);
}
#app-mount .verificationBlock-xhj3fR {
	background-color: rgba(var(--transparencycolor), .1);
	border: 1px solid rgba(var(--transparencycolor), .3);
}
#app-mount .verificationBlock-xhj3fR:hover {
	background-color: rgba(var(--transparencycolor), .2);
	border-color: rgb(var(--transparencycolor));
}
#app-mount .verificationBlock-xhj3fR .image-cLINxN.email-1Zyyoj {
	background-image: url(https://discord.com/assets/cefc9c14adce616059f519c581331b32.svg);
	opacity: .5;
}
#app-mount .verificationBlock-xhj3fR .image-cLINxN.phone-2wue_- {
	background-image: url(https://discord.com/assets/ca452f5271ebcc7132db59f60a2a9cfe.svg);
	opacity: .5;
}
#app-mount .verificationBlock-xhj3fR .body-2IbMjQ {
	color: var(--header-secondary);
}

/* ----		14.17.	QUICKSELECTPOPOUT				---- */

#app-mount .quickSelectPopout-2F0PXw,						/* quickselect												*/
#app-mount .popoutList-10IFAa {								/* listpopout												*/
	background-color: transparent;
	border: none;
	border-radius: 5px;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	color: var(--header-primary);
	position: relative;
}
.quickSelectPopout-2F0PXw::before,
.popoutList-10IFAa::before,
.quickSelectPopout-2F0PXw::after,
.popoutList-10IFAa::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.quickSelectPopout-2F0PXw::before,
.popoutList-10IFAa::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.quickSelectPopout-2F0PXw::after,
.popoutList-10IFAa::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}
#app-mount .selectableItem-3-fmiM {
	color: var(--header-primary);
}
#app-mount .selectableItem-3-fmiM:hover {
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .quickSelectPopoutOption-2E2UmS:hover {
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .quickSelectPopoutOption-2E2UmS.selected-2xg679 {
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .popoutListEmpty-3MWXtE {
	color: var(--header-primary);
}
#app-mount .quickSelectArrow-1dOOHb {
	-webkit-mask: url(https://discord.com/assets/f58cf3b8fc79e9d671ab649ab37651a9.svg) 50% no-repeat;
	background: var(--interactive-normal);
}

/* ----		14.18.	WARNINGPOPOUT					---- */

#app-mount .contentWarningPopout-WKdbDG {					/* popout													*/
	background-color: transparent;
	border: none;
	border-radius: 5px;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
}
.contentWarningPopout-WKdbDG::before,
.contentWarningPopout-WKdbDG::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.contentWarningPopout-WKdbDG::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.contentWarningPopout-WKdbDG::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}
#app-mount .body-2rDNbs {
	color: var(--header-secondary);
}
#app-mount .header-DRA95Q {
	color: var(--header-primary);
}

/* ----		14.18.	ACTIVETHREADLISTPOPOUT			---- */

#app-mount .popout-TdhJ6Z {					/* popout													*/
	background-color: transparent;
	border: none;
	border-radius: 5px;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
}
.popout-TdhJ6Z::before,
.popout-TdhJ6Z::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
.popout-TdhJ6Z::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.popout-TdhJ6Z::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}


/* ~~~~		15.		GENERAL							~~~~ */

::selection {												/* selection												*/
	background: rgb(var(--accentcolor));
}
.highlight {
	background: rgb(var(--accentcolor));
}

#app-mount .elevationLow-26BbEG, #app-mount .elevationLow-3aiJPL, .lightElevationLow-1QzqDT, .darkElevationLow-2LO4eN {
	box-shadow: 0 1px 5px 0 rgba(var(--transparencycolor), .3);
}
#app-mount .elevationHigh-3KUiqj, #app-mount .elevationHigh-28Pty4, .lightElevationHigh-3gER0h, .darkElevationHigh-1BaD2i {
	box-shadow: 0 2px 10px 0 rgba(var(--transparencycolor), .3);
}
#app-mount .elevationBorderLow-3_3rXL, #app-mount .elevationBorderLow-2_BGCd, .lightElevationBorderLow-2Ysl3H, .darkElevationBorderLow-34oHrM {
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 1px 5px 0 rgba(var(--transparencycolor), .3);
}
#app-mount .elevationBorderHigh-3drnJX, #app-mount .elevationBorderHigh-1s5JCj, .lightElevationBorderHigh-3wutCI, .darkElevationBorderHigh-8ZYNYM {
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
}

#app-mount .breadcrumbWrapper-3rpYiO {						/* breadcrumbs			wrapper							*/
	color: rgba(var(--textbrightest),.3);
}
#app-mount .activeBreadcrumb-2xVic0 {						/* breadcrumbs			active							*/
	color: rgba(var(--textbrightest),.6);
}

/* ----		15.1.	TEXT							---- */

.description-1u9Qui {
	color: var(--header-secondary);
}

#app-mount h1.title-338goq,
#app-mount h2.title-338goq {
	color: var(--header-primary);
}
#app-mount h3.title-338goq {
	color: var(--text-normal);
}
#app-mount h4.title-338goq,
#app-mount h5.title-338goq,
#app-mount h6.title-338goq {
	color: var(--header-secondary);
}

#app-mount .text-27cdrj,
#app-mount .title-2CL_z0 {
	color: var(--text-muted);
}

#app-mount .title-338goq {
	color: var(--header-secondary);
}

#app-mount .markdown-19oyJN {
	color: var(--text-normal);
}
#app-mount .markdown-19oyJN th {
	background-color: var(--background-tertiary);
	border-color: var(--interactive-muted);
	color: var(--header-primary);
}
#app-mount .markdown-19oyJN td {
	border-color: var(--interactive-muted);
}
#app-mount .markdown-19oyJN tr {
	border-color: var(--interactive-muted);
	color: var(--header-secondary);
}
#app-mount .markdown-19oyJN tr:nth-child(2n) {
	background-color: var(--background-secondary);
}
#app-mount .markdown-19oyJN .blockquote-2mppuN {
	border-left-color: var(--interactive-muted);
}
#app-mount .markdown-19oyJN code {
	background-color: var(--background-secondary);
}
#app-mount .markdown-19oyJN .codeInline-1RFl81 {
	color: var(--text-normal);
}

/* ----		15.2.	BUTTONS							---- */

.btn-115Sr0.btnPrimary-7AVO-X,
.lookFilled-yCfaCM.hoverBrand-9W5Bs0.hasHover-26V98q:hover,
.lookFilled-yCfaCM.hoverBrandNew-2zxGm3.hasHover-26V98q:hover,
.lookFilled-yCfaCM.colorBrand-I6CyqQ:not(.buttonColor-3bP3fX):not([style*="background-color"]),
.lookFilled-yCfaCM.colorBrandNew-2-gGsS:not(.buttonColor-3bP3fX):not([style*="background-color"]) {
	text-shadow: 1px 1px var(--textshadow);
}
.lookFilled-yCfaCM.hoverBrand-9W5Bs0.hasHover-26V98q:hover svg,
.lookFilled-yCfaCM.hoverBrandNew-2zxGm3.hasHover-26V98q:hover svg,
.lookFilled-yCfaCM.colorBrand-I6CyqQ:not(.buttonColor-3bP3fX):not([style*="background-color"]) svg,
.lookFilled-yCfaCM.colorBrandNew-2-gGsS:not(.buttonColor-3bP3fX):not([style*="background-color"]) svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}

#app-mount .lookInverted-2mDUMi.colorPrimary-2AuQVo .spinnerItem-3dCJpG {
	background-color: rgb(var(--textdarkest));
}
#app-mount .lookOutlined-3yKVGo.colorPrimary-2AuQVo .spinnerItem-3dCJpG,
#app-mount .lookLink-15mFoz.colorPrimary-2AuQVo .spinnerItem-3dCJpG {
	background-color: rgb(var(--textdarkest));
}

#app-mount .lookFilled-yCfaCM.colorPrimary-2AuQVo:hover,
#app-mount .lookFilled-yCfaCM.hoverPrimary-2hqNIm.hasHover-26V98q:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .lookFilled-yCfaCM.colorPrimary-2AuQVo:active,
#app-mount .lookFilled-yCfaCM.hoverPrimary-2hqNIm.hasHover-26V98q:active {
	background-color: rgba(var(--transparencycolor), .6);
}
#app-mount .lookFilled-yCfaCM.colorPrimary-2AuQVo,
#app-mount .lookFilled-yCfaCM.colorPrimary-2AuQVo:disabled {
	background-color: rgba(var(--transparencycolor), .2);
	color: #FFF;
}

#app-mount .lookInverted-2mDUMi.colorPrimary-2AuQVo:hover,
#app-mount .lookInverted-2mDUMi.hoverPrimary-2hqNIm.hasHover-26V98q:hover {
	background-image: linear-gradient(0deg, rgba(0, 0, 0, .1), rgba(0, 0, 0, .1));
}
#app-mount .lookInverted-2mDUMi.colorPrimary-2AuQVo:active,
#app-mount .lookInverted-2mDUMi.hoverPrimary-2hqNIm.hasHover-26V98q:active {
	background-image: linear-gradient(0deg, rgba(0, 0, 0, .2), rgba(0, 0, 0, .2));
}
#app-mount .lookInverted-2mDUMi.colorPrimary-2AuQVo,
#app-mount .lookInverted-2mDUMi.colorPrimary-2AuQVo:disabled {
	background-color: #FFF;
	color: rgba(var(--textdarkest));
}

#app-mount .lookOutlined-3yKVGo.hoverPrimary-2hqNIm.hasHover-26V98q:hover {
	border-color: rgba(var(--textdarkest), .6);
}
#app-mount .lookOutlined-3yKVGo.hoverPrimary-2hqNIm.hasHover-26V98q:active {
	background-color: rgba(var(--textdarkest), .1);
	border-color: rgb(var(--textdarkest));
}
#app-mount .lookOutlined-3yKVGo.colorPrimary-2AuQVo,
#app-mount .lookOutlined-3yKVGo.colorPrimary-2AuQVo:disabled {
	border-color: rgba(var(--textdarkest), .1);
	color: rgb(var(--textdarkest));
}

#app-mount .lookLink-15mFoz.colorPrimary-2AuQVo {
	color: rgb(var(--textdarkest));
}
#app-mount .lookLink-15mFoz.colorPrimary-2AuQVo:hover .contents-3ca1mk,
#app-mount .lookLink-15mFoz.hoverPrimary-2hqNIm.hasHover-26V98q:hover .contents-3ca1mk {
	background-image: linear-gradient(0deg, transparent, transparent 1px, rgb(var(--textdarkest)) 0, rgb(var(--textdarkest)) 2px, transparent 0);
	color: rgb(var(--textdarkest));
}

#app-mount .borderPrimary-1ygM7_ {
	border-color: rgb(var(--textdarkest)); !important;
}

#app-mount .lookInverted-2mDUMi.colorTransparent-13Bvvi .spinnerItem-3dCJpG {
	background-color: rgba(var(--textbrightest),.1);
}
#app-mount .lookFilled-yCfaCM.colorTransparent-13Bvvi .spinnerItem-3dCJpG,
#app-mount .lookOutlined-3yKVGo.colorTransparent-13Bvvi .spinnerItem-3dCJpG,
#app-mount .lookLink-15mFoz.colorTransparent-13Bvvi .spinnerItem-3dCJpG {
	background-color: rgb(var(--textbrightest));
}

#app-mount .lookFilled-yCfaCM.colorTransparent-13Bvvi:hover,
#app-mount .lookFilled-yCfaCM.hoverTransparent-1F6BzX.hasHover-26V98q:hover {
	background-color: rgba(var(--textbrightest),.05);
}
#app-mount .lookFilled-yCfaCM.colorTransparent-13Bvvi:active,
#app-mount .lookFilled-yCfaCM.hoverTransparent-1F6BzX.hasHover-26V98q:active  {
	background-color: rgba(var(--textbrightest),.01);
}
#app-mount .lookFilled-yCfaCM.colorTransparent-13Bvvi,
#app-mount .lookFilled-yCfaCM.colorTransparent-13Bvvi:disabled {
	background-color: rgba(var(--textbrightest),.1);
	color: rgb(var(--textbrightest));
}

#app-mount .lookInverted-2mDUMi.colorTransparent-13Bvvi:hover,
#app-mount .lookInverted-2mDUMi.hoverTransparent-1F6BzX.hasHover-26V98q:hover {
	background-color: rgba(var(--textbrightest),.05);
}
#app-mount .lookInverted-2mDUMi.colorTransparent-13Bvvi:active,
#app-mount .lookInverted-2mDUMi.hoverTransparent-1F6BzX.hasHover-26V98q:active {
	background-color: rgba(var(--textbrightest),.1);
}
#app-mount .lookInverted-2mDUMi.colorTransparent-13Bvvi,
#app-mount .lookInverted-2mDUMi.colorTransparent-13Bvvi:disabled  {
	background-color: rgb(var(--textbrightest));
	color: rgba(var(--textbrightest),.1);
}

#app-mount .lookOutlined-3yKVGo.hoverTransparent-1F6BzX.hasHover-26V98q:hover {
	background-color: rgba(var(--textbrighter),.1);
	border-color: rgb(var(--textbrightest));
}
#app-mount .lookOutlined-3yKVGo.hoverTransparent-1F6BzX.hasHover-26V98q:active {
	background-color: rgba(var(--textbrightest),.1);
	border-color: rgb(var(--textbrightest));
}
#app-mount .lookOutlined-3yKVGo.colorTransparent-13Bvvi,
#app-mount .lookOutlined-3yKVGo.colorTransparent-13Bvvi:disabled {
	background-color: transparent;
	color: rgb(var(--textbright));
}

#app-mount .lookLink-15mFoz.colorTransparent-13Bvvi {
	color: rgb(var(--textbright));
}
#app-mount .lookLink-15mFoz.colorTransparent-13Bvvi:hover .contents-3ca1mk,
#app-mount .lookLink-15mFoz.hoverTransparent-1F6BzX.hasHover-26V98q:hover .contents-3ca1mk {
	background-image: linear-gradient(0deg, transparent,transparent 1px,rgb(var(--textbrighter)) 0,rgb(var(--textbrighter)) 2px,transparent 0);
	color: rgb(var(--textbright));
}

#app-mount .borderTransparent-2P3AAk {
	border-color: rgb(var(--textbrightest)) !important;
}

/* ----		15.3.	INPUTS							---- */

.input-2g-os5 {												/* valueinput			bordered							*/
	background-color: rgba(var(--transparencycolor), .1);
	border-color: rgba(var(--transparencycolor), .3);
}
.input-2g-os5:hover:not(:focus) {
	border-color: rgb(var(--transparencycolor));
}
.textInput-3g8y92 {											/* textinput												*/
	background-color: rgba(var(--transparencycolor), .1);
}
.textInput-3g8y92 .input-2g-os5 {
	background: transparent;
}

#app-mount .prefixInput-w72mM6 {
	background-color: rgba(0,0,0,.1);
	border-color: rgba(0,0,0,.3);
}
#app-mount .prefixInput-w72mM6:hover {
	border-color: rgba(0,0,0,.6);
}
#app-mount .prefixInputInput-yS14_1 {
	color: var(--header-primary);
}
#app-mount .prefixInputInput-yS14_1::-webkit-input-placeholder,
#app-mount .prefixInputInput-yS14_1::-moz-placeholder,
#app-mount .prefixInputInput-yS14_1:-ms-input-placeholder,
#app-mount .prefixInputInput-yS14_1::placeholder {
	color: var(--text-muted);
}
#app-mount .prefixInputPrefix-20KCc9 {
	color: var(--text-muted);
}

#app-mount .maxLength-IdVNmX {
	color: var(--text-muted);
}

#app-mount .copyInput-3AbKWB {
	background-color: var(--deprecated-text-input-bg);
}
#app-mount .copyInputDefault-3jiMHw {
	border-color: var(--deprecated-text-input-border);
}
#app-mount .hiddenMessage-3QNvPt,
#app-mount .inputDefault-1AaKiD {
	color: var(--header-primary);
}
#app-mount .hiddenMessage-3QNvPt::placeholder,
#app-mount .inputDefault-1AaKiD::placeholder {
	color: rgba(var(--textbrightest),.3);
}

.container-2nx-BQ {											/* checkboxswitch											*/
	background-color: rgba(var(--transparencycolor), .3) !important;
}
.container-2nx-BQ rect[fill] {
	fill: var(--header-primary) !important;
}
.container-2nx-BQ path[fill] {
	fill: rgb(var(--transparencycolor)) !important;
}

#app-mount .item-2idW98 {									/* radiogroup			container							*/
	background-color: rgba(var(--transparencycolor), .2);
}
#app-mount .item-2idW98:hover {
	background-color: rgba(var(--transparencycolor), .4);
}
#app-mount .item-2idW98[aria-checked=true] .radioBar-3w9XY- {
	background: rgb(var(--accentcolor));
}
#app-mount .item-2idW98[aria-checked=true] .radioBar-3w9XY- .radioIconForeground-2BMavi {
	color: var(--header-primary);
}
#app-mount .item-2idW98 .radioBar-3w9XY-[style*="--radio-bar-accent-color"] {
	background: var(--radio-bar-accent-color);
	border: unset;
	color: var(--header-primary);
}
#app-mount .item-2idW98[aria-checked=false]:hover .radioBar-3w9XY-[style*="--radio-bar-accent-color"] {
	background: var(--radio-bar-accent-color) linear-gradient(to right, rgba(255, 255, 255, .2), rgba(255, 255, 255, .2));
}

#app-mount .checkboxContainer-1NbL2v::before {				/* checkbox				container							*/
	background-color: rgba(var(--textdarker), .3);
}
#app-mount .checkbox-f1HnKB {								/* checkbox				inner								*/
	border-color: rgb(var(--textdark));
}
#app-mount .checkbox-f1HnKB.checked-1pZh2h {				/* checkbox				checked								*/
	background-color: rgb(var(--textbrightest));
	border-color: rgb(var(--textbrightest));
}
#app-mount .checkbox-f1HnKB.checked-1pZh2h.round-1RSG-3 {	/* checkbox				roundchecked						*/
	background-color: rgb(var(--accentcolor)) !important;
	border-color: rgb(var(--accentcolor)) !important;
}
#app-mount .checkbox-f1HnKB.checked-1pZh2h.round-1RSG-3 svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}
#app-mount .checkbox-f1HnKB.checked-1pZh2h.round-1RSG-3 path[fill] {
	fill: #fff;
}
.checkboxMute-1erNeD::before {
	background-color: rgba(var(--transparencycolor), .2);
}

#app-mount .bar-1Bhnl9 {									/* slider				backgroundbar						*/
	background-color: rgba(var(--transparencycolor), .3);
}
.grabber-2GQyvM {											/* slider				grabber								*/
	background-color: var(--header-primary);
	border-color: var(--header-primary);
	box-shadow: 0 3px 1px 0 rgba(var(--transparencycolor), .05), 0 2px 2px 0 rgba(var(--transparencycolor), .1), 0 3px 3px 0 rgba(var(--transparencycolor), .05);
}
#app-mount .markValue-2U_-UG {								/* slider				markvalue							*/
	color: var(--text-muted);
}
#app-mount .defaultValue-19SZ-q .markValue-2U_-UG {
	color: #43b581;
}
#app-mount .markDash-yk2kJ- {
	background: transparent;
	color: rgba(var(--transparencycolor), .3);
}
#app-mount .defaultValue-19SZ-q .markDash-yk2kJ- {
	color: #43b581;
}
#app-mount .markDash-yk2kJ-::before,
#app-mount .markDash-yk2kJ-::after {
	content: "";
	position: absolute;
	background: currentColor;
	height: 8px;
	width: 2px;
}
#app-mount .markDash-yk2kJ-::before {
	top: 14px;
}
#app-mount .markDash-yk2kJ-::after {
	top: 30px;
}
#app-mount .bubble-3we2di {									/* slider				bubble								*/
	background-color: rgb(var(--accentcolor));
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}
#app-mount .bubble-3we2di::before {
	border-top-color: rgb(var(--accentcolor));
}

#app-mount .container-30qY7E {								/* hotkeyinput			container							*/
	background-color: rgba(var(--transparencycolor), .1);
	border-color: rgba(var(--transparencycolor), .3);
}
#app-mount .editIcon-e7sZ3b {								/* hotkeyinput			editicon							*/
	-webkit-mask: url(https://discord.com/assets/860396b3ff3fa1c4ae355bebfabadecb.svg) center/cover no-repeat;
	background: var(--header-primary);
}
#app-mount .container-1_EVMa .button-ZJ9ZzX {
	background-color: rgba(var(--transparencycolor),.3) !important;
	color: var(--header-primary) !important;
}
#app-mount .container-1_EVMa.recording-3ny5_E .button-ZJ9ZzX {
	background-color: rgba(var(--dangercolor),.1) !important;
	color: rgb(var(--dangercolor)) !important;
}

.select-1YfRS9 [class*="css-"][class*="-container"] {		/* select				container							*/
	background-color: transparent;
}
.lookFilled-1GseHa.select-1Ia3hD,
.select-1YfRS9 [class*="css-"][class*="-control"] {
	background-color: rgba(var(--transparencycolor), .1);
	border-color: rgba(var(--transparencycolor), .3);
}
.lookFilled-1GseHa.select-1Ia3hD:hover {
	border-color: rgb(var(--transparencycolor));
}
.lookFilled-1GseHa.select-1Ia3hD:hover.open-1FRZsK,
.lookFilled-1GseHa.open-1FRZsK {
	border-color: rgb(var(--transparencycolor)) rgb(var(--transparencycolor)) rgba(var(--transparencycolor), .3);
}
.lookFilled-1GseHa.select-1Ia3hD .searchInput-3pIoTy {
	background: transparent;
}
.select-1Ia3hD,
.select-1YfRS9 [class*="css-"][class*="-control"] {
	background-color: var(--deprecated-text-input-bg);
	border-color: var(--deprecated-text-input-border);
	color: var(--text-normal);
}
.select-1YfRS9 [class*="css-"][class*="-control"]:hover,
.select-1YfRS9 [class*="css-"][class*="-control"]:not(:last-child) {
	border-color: var(--deprecated-text-input-border-hover);
}
.select-1YfRS9.languageSelector-1hjSyO [class*="css-"][class*="-control"] {
	background-color: rgba(var(--transparencycolor), .3);
}
.select-1YfRS9 [class*="css-"][class*="-singleValue"],
.select-1YfRS9 [class*="css-"][class*="-placeholder"],
.select-1YfRS9 [class*="css-"][class*="-indicatorContainer"] {
	color: var(--text-normal);
}
.option-2eIyOn,
#app-mount .optionNormal-12VR9V,
.css-1gfjib6-option,
.css-1yz4bi9-option,
.css-ru8b0x-option,
.css-1yz4bi9-option {
	background-color: rgba(var(--transparencycolor), .1);
	color: var(--interactive-normal);
}
.option-2eIyOn:hover,
#app-mount .optionNormal-12VR9V:hover,
.css-pkcurw-option,
.css-rzbxvl-option,
.css-1qxn4c5-option,
.css-rzbxvl-option {
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--interactive-hover);
}
.option-2eIyOn[aria-selected=true],
#app-mount .optionActive-KkAdqq,
.css-1gxgi19-option,
.css-1ba14n5-option,
.css-6qzljd-option,
.css-1ba14n5-option {
	background-color: rgba(var(--transparencycolor), .5);
	color: var(--interactive-active);
}
.selectedIcon-19TbzU {
	color: var(--interactive-active);
}
.role-3ulsK-:hover {
	background-color: rgba(var(--transparencycolor), .2);
}
.popout-1KHNAq::-webkit-scrollbar {
	display: none;
}
.popout-1KHNAq,
.container-3LUQwT,
.select-1YfRS9 > [class*="css-"][class*="-container"] > [class*="css-"][class*="-menu"] {
	background-color: transparent;
	border: 1px solid rgba(var(--transparencycolor), .3);
	box-shadow: 0px 1px 5px 0px rgba(var(--transparencycolor), .3);
	overflow: hidden;
}
.popout-1KHNAq::before,
.popout-1KHNAq.scrollerBase-_bVAAt .content-2a4AW9::before,
.container-3LUQwT::before,
.select-1YfRS9 > [class*="css-"][class*="-container"] > [class*="css-"][class*="-menu"]::before,
.popout-1KHNAq::after,
.popout-1KHNAq.scrollerBase-_bVAAt .content-2a4AW9::after,
.container-3LUQwT::after,
.select-1YfRS9 > [class*="css-"][class*="-container"] > [class*="css-"][class*="-menu"]::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
.popout-1KHNAq::before,
.popout-1KHNAq.scrollerBase-_bVAAt .content-2a4AW9::before,
.container-3LUQwT::before,
.select-1YfRS9 > [class*="css-"][class*="-container"] > [class*="css-"][class*="-menu"]::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.popout-1KHNAq::after,
.popout-1KHNAq.scrollerBase-_bVAAt .content-2a4AW9::after,
.container-3LUQwT::after,
.select-1YfRS9 > [class*="css-"][class*="-container"] > [class*="css-"][class*="-menu"]::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	backdrop-filter: blur(var(--popoutblur));
}
.popout-1KHNAq.scrollerBase-_bVAAt::before,
.popout-1KHNAq.scrollerBase-_bVAAt::after {
	display: none;
}

/* ----		15.4.	SEARCHBARS						---- */

.container-1SX9VC,											/* searchbar			inner								*/
.container-2oNtJn {
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .searchBox-pyIJJj .searchBoxInput-P0mWHW::placeholder {
	color: var(--text-muted);
}
#app-mount .searchIcon-34RNw9 {
	color: var(--text-muted);
}
#app-mount .filterLabel-3-eQ3i {
	color: var(--header-secondary);
}
#app-mount .searchBox-pyIJJj {
	background-color: rgba(var(--transparencycolor), .3);
	box-shadow: 0 2px 5px 0 rgba(var(--transparencycolor), .2);
}

/* ----		15.5.	TAGS							---- */

.botTagRegular-kpctgU:not([style]) {						/* bottag				regular								*/
	text-shadow: 1px 1px var(--textshadow);
}
.botTagRegular-kpctgU:not([style]) svg {
	filter: drop-shadow(1px 1px var(--textshadow));
}

.base-3IDx3L[style*="var(--bdfdb-blurple)"],				/* numberbadge												*/
.base-3IDx3L[style*="background-color: rgb(88, 101, 242)"],
.base-3IDx3L[style*="background-color: rgb(114, 137, 218)"] {
	text-shadow: 1px 1px var(--textshadow);
}

.iconBadge-2wi9r4 {											/* iconbadge												*/
	background-color: rgba(var(--transparencycolor), .3);
}

/* ----		15.6.	ICONS							---- */

.emptySearchImage-1qOMLW,									/* empty search												*/
.image-20MDYu {												/* no peoples/webhooks/etc.									*/
	opacity: 0.6;
}

#app-mount .gameIcon-1mDo1J {								/* activity icon											*/
	background-color: rgba(var(--textbrightest), .1);
	color: var(--header-primary);
}

#app-mount .invalidPoop--w1123 {							/* erroricon			invalidpoop							*/
	background-color: rgba(var(--transparencycolor), .3);
	opacity: 0.7;
}
#app-mount .guildIconExpired-2BFmZC {						/* erroricon			expiredguild						*/
	background-color: rgba(var(--transparencycolor), .3);
	opacity: 0.7;
}

/* ----		15.7.	SCROLLBARS						---- */

::-webkit-scrollbar,
#app-mount ::-webkit-scrollbar {
	width: 8px;
	height: 8px;
}
#app-mount .scroller-3vODG7::-webkit-scrollbar {
	width: 6px;
	height: 6px;
}
#app-mount .scroller-Pcwd3e::-webkit-scrollbar,
#app-mount .scrollbar-3vVt8d::-webkit-scrollbar,
#app-mount .scroller-2PSBSf::-webkit-scrollbar {
	width: 4px;
	height: 4px;
}
::-webkit-scrollbar,
::-webkit-scrollbar-track,
::-webkit-scrollbar-track-piece,
#app-mount ::-webkit-scrollbar,
#app-mount ::-webkit-scrollbar-track,
#app-mount ::-webkit-scrollbar-track-piece {
	border-color: transparent !important;
	background: transparent !important;
}
::-webkit-scrollbar-thumb,
#app-mount ::-webkit-scrollbar-thumb {
	border-radius: 10px;
	border: none;
	background-color: rgb(var(--accentcolor)) !important;
}
.none-2-_0dP::-webkit-scrollbar-corner,
.none-2-_0dP::-webkit-scrollbar-thumb,
.none-2-_0dP::-webkit-scrollbar-track,
.none-2-_0dP::-webkit-scrollbar {
	display: none;
}

/* ----		15.8.	NOTIFICATIONBAR					---- */

.base-2jDfDU .notice-2HEN-u powercord-announcement {
	border-radius: 0;
}
#app-mount .notice-2FJMB4 {
	box-shadow: 0 1px 5px 0 rgba(var(--transparencycolor), .3);
}
#app-mount .notice-12Koq- {
	background-color: rgba(var(--transparencycolor), .6);
}
.noticeBrand-3nQBC_ {
	text-shadow: 1px 1px var(--textshadow);
}
.noticeBrand-3nQBC_ .button-1MICoQ {
	box-shadow: 1px 1px var(--textshadow);
	text-shadow: 1px 1px var(--textshadow);
}

/* ----		15.9.	TOOLTIPS						---- */

.headerText-1e7ZU0,
.bodyText-3yi6Dj {
	color: #fff;
}
#app-mount .tooltip-16UpTB,
#app-mount .tooltip-1_vJJI,
#app-mount .tooltip-14MtrL {
	box-shadow: 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	color: #fff;
}
#app-mount .guildNameText-74xXQn {
	color: #fff;
}
#app-mount .muteText-1DPH3L {
	color: #bbb;
}
#app-mount .tooltip-16UpTB,
#app-mount .tooltip-1_vJJI,
#app-mount .tooltipPrimary-3qLMbS,
#app-mount .tooltipGrey-lpLZjh,
#app-mount .tooltipBlack-vMYxvw {
	background-color: rgb(var(--accentcolor));
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}
#app-mount .tooltipPrimary-3qLMbS .note-e4Jh6_,
#app-mount .tooltipGrey-lpLZjh .note-e4Jh6_,
#app-mount .tooltipBlack-vMYxvw .note-e4Jh6_ {
	color: #bbb;
}
#app-mount .tooltipPrimary-3qLMbS .tooltipPointer-3L49xb,
#app-mount .tooltipGrey-lpLZjh .tooltipPointer-3L49xb,
#app-mount .tooltipBlack-vMYxvw .tooltipPointer-3L49xb {
	border-top-color: rgb(var(--accentcolor));
}
#app-mount .tooltipPointer-1KkjI2,
#app-mount .tooltipPointer-1awMxk {
	border-right-color: rgb(var(--accentcolor));
}
.emptyUser-2FDCJv {
	background: rgba(var(--transparencycolor), .5);
}
.moreUsers-_v6T-L {
	background: rgba(var(--transparencycolor), .5);
}


/* ~~~~		16.		BDSUPPORT						~~~~ */

html .bd-toast {
	background-color: rgb(var(--accentcolor));
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}
html .bd-toast.icon {
	background-image: none !important;
}
html .bd-toast.icon::before {
	content: "";
	position: absolute;
	top: 0;
	right: 0;
	bottom: 0;
	left: 0;
	background: #fff !important;
	-webkit-mask: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg"><path fill="black" d=""/></svg>') center/cover no-repeat;
}
html .bd-toast.toast-danger.icon::before,
html .bd-toast.toast-error.icon::before {
	-webkit-mask: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="black" d="M12 2C6.47 2 2 6.47 2 12s4.47 10 10 10 10-4.47 10-10S17.53 2 12 2zm5 13.59L15.59 17 12 13.41 8.41 17 7 15.59 10.59 12 7 8.41 8.41 7 12 10.59 15.59 7 17 8.41 13.41 12 17 15.59z"/></svg>') 6px 50%/20px 20px no-repeat;
}
html .bd-toast.toast-info.icon::before {
	-webkit-mask: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="black" d="M 12 2 C 6.48 2 2 6.48 2 12 s 4.48 10 10 10 10-4.48 10-10 S 17.52 2 12 2 z m 1 15 h -2 v -6 h 2 v 6 z m 0-8 h -2 V 7 h 2 v 2 z"/></svg>') 6px 50%/20px 20px no-repeat;
}
html .bd-toast.toast-success.icon::before {
	-webkit-mask: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path fill="black" d="M 12 2 C 6.48 2 2 6.48 2 12 s 4.48 10 10 10 10-4.48 10-10 S 17.52 2 12 2 z m -2 15 l -5-5 1.41-1.41 L 10 14.17 l 7.59-7.59 L 19 8 l -9 9 z"/></svg>') 6px 50%/20px 20px no-repeat;
}
html .bd-toast.toast-warning.icon::before,
html .bd-toast.toast-warn.icon::before {
	-webkit-mask: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="black" d="M 1 21 h 22 L 12 2 1 21 z m 12-3 h -2 v -2 h 2 v 2 z m 0-4 h -2 v -4 h 2 v 4 z"/></svg>') 6px 50%/20px 20px no-repeat;
}

#app-mount .fav {
	background: var(--interactive-active);
	width: 16px;
	height: 16px;
	padding: 0;
	-webkit-mask: url(https://mwittrien.github.io/BetterDiscordAddons/Themes/_res/svgs/common/fav_star_empty.svg) center/contain no-repeat;
}
#app-mount .fav:hover,
#app-mount .fav.active {
	background: #faa61a;
}
#app-mount .fav.active {
	-webkit-mask: url(https://mwittrien.github.io/BetterDiscordAddons/Themes/_res/svgs/common/fav_star.svg) center/contain no-repeat;
}

#app-mount .bd-tab-item:hover {
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .bd-tab-item.selected {
	background-color: rgb(var(--accentcolor));
	color: #fff;
	text-shadow: 1px 1px var(--textshadow);
}

#app-mount .bd-server-card {								/* pubslayer			guildcard							*/
	background-color: rgba(var(--transparencycolor), .3);
}
#app-mount .bd-server-icon {								/* pubslayer			guildicon							*/
	background-color: rgba(var(--transparencycolor), .2);
	border-color: transparent;
}
#app-mount .bd-server-card:hover,
#app-mount .bd-server-icon:hover {
	background-color: rgba(var(--transparencycolor), .4);
}

.bd-switch-body {											/* bd switch												*/
	--switch-color: rgb(var(--transparencycolor));
	background-color: rgba(var(--transparencycolor), .3);
}

.bd-select .bd-select-options {								/* bd select			popout								*/
	background-color: transparent;
	border: none;
	border-radius: 4px;
	box-shadow: rgba(var(--transparencycolor), .3) 0px 2px 5px 0px;
	box-sizing: border-box;
	padding: 6px 8px;
	margin-left: -9px;
}
.bd-select .bd-select-options::before,
.bd-select .bd-select-options::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 4px;
	pointer-events: none;
	z-index: -1;
}
.bd-select .bd-select-options::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
.bd-select .bd-select-options::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.3));
	backdrop-filter: blur(var(--popoutblur));
}
.bd-select .bd-select-option {								/* bd select			popout option						*/
	display: flex;
	align-items: center;
	min-height: 32px;
	border-radius: 2px;
	box-sizing: border-box;
	color: var(--interactive-normal);
	font-size: 14px;
	font-weight: 500;
	line-height: 18px;
	margin-top: 2px;
	margin-bottom: 2px;
	padding: 0 8px;
}
.bd-select .bd-select-option:hover {
	background-color: rgba(var(--transparencycolor), .2);
	color: var(--interactive-hover);
}
.bd-select .bd-select-option.selected {
	background-color: rgba(var(--transparencycolor), .3);
	color: var(--interactive-active);
}

.bd-pfbtn {													/* addonlist			folder button						*/
	text-shadow: 1px 1px var(--textshadow);
}

.bd-server-tag {											/* addonlist			public list tag						*/
	text-shadow: 1px 1px var(--textshadow);
}

.bd-addon-views .bd-view-button:hover {
	background-color: rgba(var(--transparencycolor), .3);
}

.bd-button {
	filter: drop-shadow(1px 1px var(--textshadow));
}
.bd-button.bd-button-danger {
	filter: unset;
}

.floating-window.resizable {								/* customcss editor		detached							*/
	background: rgb(var(--transparencycolor));
}
html .monaco-editor .reference-zone-widget .ref-tree .referenceMatch .highlight {
	background: rgb(var(--accentcolor));
}


/* ~~~~		17.		POWERCORDSUPPORT				~~~~ */

html .powercord-toast {
	background-color: transparent;
	border: none;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	overflow: hidden;
}
html .powercord-toast::before,
html .powercord-toast::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	border-radius: 5px;
	pointer-events: none;
	z-index: -1;
}
html .powercord-toast::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
html .powercord-toast::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}
html .powercord-toast .header {
	background-color: rgba(var(--transparencycolor), .2);
	box-shadow: 0 2px 3px 0 rgba(var(--transparencycolor), .2);
	color: var(--header-primary);
}
html .powercord-toast .contents .inner {
	background-color: rgba(var(--transparencycolor), .2);
	border: none;
	color: var(--header-secondary);
}


/* ~~~~		18.		PLUGINSUPPORT					~~~~ */

/* ----		18.1.	BDFDB							---- */

html .colorDefault-XdNdIp .bg-8df5St {
	background: transparent;
	opacity: 1;
}
html .colorDefault-XdNdIp .bg-8df5St::before,
html .colorDefault-XdNdIp .bg-8df5St::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	pointer-events: none;
	z-index: -1;
}
html .colorDefault-XdNdIp .bg-8df5St::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
html .colorDefault-XdNdIp .bg-8df5St::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.25));
	backdrop-filter: blur(var(--popoutblur));
}

/* ----		18.2.	DATEVIEWER						---- */

#app-mount #dv-mount {
	background: transparent;
	z-index: 1;
}
#app-mount #dv-mount::before,
#app-mount #dv-mount::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	pointer-events: none;
	z-index: -1;
}
#app-mount #dv-mount::before {
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
}
#app-mount #dv-mount::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + var(--memberlisttransparency) * 0.85));
	backdrop-filter: blur(var(--backgroundblur));
}
#app-mount #dv-main {
	border-top-color: rgba(var(--transparencycolor), .2);
	color: var(--header-primary);
}
#app-mount #dv-main .dv-date {
	color: var(--header-secondary);
	opacity: 1;
}

/* ----		18.3.	MEMBERCOUNT						---- */

#app-mount #MemberCount {
	background-color: transparent;
	width: calc(100% - 8px);
	margin: 0;
	line-height: 0;
	height: 30px;
}
#MemberCount::before,
#MemberCount::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	pointer-events: none;
	z-index: -1;
}
#MemberCount::before {
	background: var(--background) var(--backgroundposition)/var(--backgroundsize);
	background-attachment: fixed;
}
#MemberCount::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + var(--memberlisttransparency) * 0.85));
	backdrop-filter: blur(var(--backgroundblur));
}

/* ----		18.4.	LINENUMBERS						---- */

.hljs ol li {
	border-left-color: var(--background-modifier-accent);
}
.hljs ol li::before {
	color: rgb(var(--textdarker));
}

/* ----		18.5.	PERMISSIONVIEWER				---- */

html #permissions-modal-wrapper {								/* modal				wrapper							*/
    z-index: 1001;
}
html #permissions-modal-wrapper #permissions-modal {			/* modal				container							*/
	background-color: transparent;
	border: none;
	box-shadow: 0 0 0 1px rgba(var(--transparencycolor), .3), 0 2px 10px 0 rgba(var(--transparencycolor), .3);
	position: relative;
	overflow: hidden;
}
html #permissions-modal-wrapper #permissions-modal::before,
html #permissions-modal-wrapper #permissions-modal::after {
	content: "";
	position: absolute;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	width: unset;
	height: unset;
	pointer-events: none;
	z-index: -1;
}
html #permissions-modal-wrapper #permissions-modal::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
}
html #permissions-modal-wrapper #permissions-modal::after {
	background-color: rgba(var(--transparencycolor), calc(var(--transparencyalpha) + 0.2));
	backdrop-filter: blur(var(--popoutblur));
}
html #permissions-modal-wrapper .header {
	background-color: rgba(var(--transparencycolor), .2);
	box-shadow: 0 2px 3px 0 rgba(var(--transparencycolor), .2);
	color: var(--header-primary);
}
html #permissions-modal-wrapper .modal-body {
	background-color: transparent;
}
html #permissions-modal-wrapper .scroller-title {
	border-bottom: 1px solid rgba(var(--transparencycolor), .3);
}
html #permissions-modal-wrapper .role-side {
	background-color: rgba(var(--transparencycolor), .1);
}
html #permissions-modal-wrapper .role-item {
	color: var(--text-normal);
}
html #permissions-modal-wrapper .role-item:hover {
	background-color: rgba(var(--transparencycolor), .1);
}
html #permissions-modal-wrapper .role-item.selected {
	background-color: rgba(var(--transparencycolor), .2);
}
html #permissions-modal-wrapper .perm-side {
	background-color: transparent;
}
html #permissions-modal-wrapper .perm-item {
	box-shadow: inset 0 -1px 0 var(--background-modifier-accent);
}
html #permissions-modal-wrapper .perm-name {
	color: var(--header-secondary);
}

/* ----		18.6.	DIRECTDOWNLOAD					---- */

#files_directDownload .file {
	background-color: rgba(var(--transparencycolor), .4);
	border-color: rgba(var(--accentcolor), .2);
	border-radius: 6px 6px 0 0;
}
#files_directDownload .file svg {
	fill: var(--interactive-active);
	opacity: 0.5;
}
#files_directDownload .file svg:hover {
	opacity: 1;
}
#files_directDownload .file span {
	color: var(--header-primary);
}
#files_directDownload .file .progress-bar {
	background-color: rgb(var(--accentcolor));
}

/* ----		18.7.	BETTERFORMATINGREDUX			---- */

.innerDisabled-2mc-iF ~ .bf-toolbar {
	display: none;
}
.bf-arrow {
	-webkit-mask: url('data:image/svg+xml; utf8, <svg xmlns="http://www.w3.org/2000/svg" height="24" viewBox="0 0 24 24" width="24"><path fill="black" d="M7.41 15.41L12 10.83l4.59 4.58L18 14l-6-6-6 6z"/></svg>') center/contain no-repeat;
	background: var(--interactive-active) !important;
}
.bf-toolbar {
	background: transparent;
	overflow: hidden;
	transform: none;
	top: -50px;
}
.bf-toolbar::after {	
	content: "";
	display: block;
	position: absolute;
	width: 100%;
	height: calc(100% - 15px);
	pointer-events: none;
	left: 0px;
	top: 5px;
	background-color: rgba(var(--transparencycolor), .5);
	border-radius: 3px;
	transform: translate(0, 55px);
	transition: all 200ms ease;
	z-index: 200;
}
.bf-toolbar.bf-visible::after,
.bf-toolbar.bf-hover:hover::after {
	transform: translate(0, 0);
	transition: all 200ms cubic-bezier(0,0,0,1);
}
.bf-toolbar::before {
	background: var(--popout) var(--popoutposition)/var(--popoutsize);
	background-attachment: fixed;
	filter: blur(var(--popoutblur));
	z-index: 100;
}
.theme-brand .bf-toolbar::after {
	background: rgb(var(--accentcolor)) linear-gradient(rgba(var(--transparencycolor), .2), rgba(var(--transparencycolor), .2)) !important;
}
.theme-brand .bf-toolbar::before {
	display: none;
}
.bf-toolbar > * {
	z-index: 300;
}
.bf-toolbar .format {
	color: var(--text-normal);
}
.bf-toolbar .format:hover {
	background-color: rgb(var(--accentcolor));
	color: #fff;
}

/* ----		18.8	CHANNELHISTORY					---- */

.channelHistoryButtons {
	top: 4px;
	left: 310px;
}

/* ----		18.9	CHANNELTABS						---- */

html .channelTabs-tabContainer,
html .channelTabs-favContainer {
	display: flex;
	align-items: center;
	flex-wrap: wrap;
	min-height: 28px;
	height: unset;
	overflow: hidden;
	transition: height 0.3s linear;
}
html .channelTabs-tabContainer {
	background: rgba(var(--transparencycolor), calc(0.05 + var(--guildchanneltransparency) * 2));
	box-shadow: 0 1px 0 rgba(var(--transparencycolor), .2), 0 1.5px 0 rgba(var(--transparencycolor), .05), 0 2px 0 rgba(var(--transparencycolor), .05);
	padding-top: 6px;
}
html .channelTabs-favContainer {
	background: rgba(var(--transparencycolor), calc(var(--guildchanneltransparency) * 2));
	padding-top: 3px;
	padding-bottom: 3px;
}
html .channelTabs-noFavs {
	background: transparent;
	padding: 0 6px;
}

html #channelTabs-settingsMenu {
	position: absolute;
	right: 0;
	background: rgba(var(--transparencycolor), calc(0.05 + var(--guildchanneltransparency) * 2));
	box-shadow: 0 1px 0 rgba(var(--transparencycolor), .2), 0 1.5px 0 rgba(var(--transparencycolor), .05), 0 2px 0 rgba(var(--transparencycolor), .05);
	border-radius: 0;
	min-height: 34px;
	height: unset;
	float: unset;
	cursor: pointer;
}
html #channelTabs-settingsMenu:hover rect[fill] {
	fill: white;
}
html .channelTabs-tabContainer {
	margin-right: 40px;
}
html .channelTabs-tab,
html .channelTabs-fav {
	display: flex;
	align-items: center;
	color: var(--interactive-normal);
	height: 28px;
	margin: 0 4px;
	padding: 0 4px;
	cursor: pointer;
}
html .channelTabs-tab {
	background: rgba(var(--transparencycolor), .3);
	border-radius: 5px 5px 0 0;
}
html .channelTabs-tab:not(.channelTabs-selected):hover,
html .channelTabs-fav:hover {
	background: rgba(var(--transparencycolor), .4);
	color: var(--interactive-hover);
}
html .channelTabs-tab.channelTabs-selected,
html .channelTabs-fav:active {
	background: rgb(var(--accentcolor));
	color: var(--interactive-active);
}
html .channelTabs-tab > *,
html .channelTabs-fav > *,
html .channelTabs-tab .channelTabs-mentionBadge,
html .channelTabs-fav .channelTabs-mentionBadge,
html .channelTabs-tab .channelTabs-unreadBadge,
html .channelTabs-fav .channelTabs-unreadBadge {
	position: static !important;
	transform: unset !important;
	float: unset !important;
}
html .channelTabs-tab > *:first-child {
	display: flex !important;
	align-items: center !important;
	flex: 1 1 auto !important;
}
html .channelTabs-tabIcon,
html .channelTabs-favIcon {
	display: inline-flex !important;
	position: static !important;
	margin-right: 6px !important;
}
html .channelTabs-tabIcon[src=""],
html .channelTabs-favIcon[src=""] {
	display: none !important;
}
html .channelTabs-tabName,
html .channelTabs-favName {
	display: inline-flex !important;
	position: static !important;
	margin: 0 !important;
	width: unset !important;
	font-size: 16px;
	line-height: 20px;
	font-weight: 500;
	white-space: nowrap;
}
html .channelTabs-tab .channelTabs-tabName ~ *,
html .channelTabs-fav .channelTabs-favName ~ * {
	margin: 0 0 0 4px !important;
}
html .channelTabs-closeTab,
html .channelTabs-tab.channelTabs-selected .channelTabs-closeTab {
	position: static;
	background: rgba(var(--transparencycolor), .3);
	color: var(--interactive-hover);
	border-radius: 50%;
	width: 14px;
	height: 14px;
	min-width: 14px;
	min-height: 14px;
	font-size: 14px;
	line-height: unset;
}
html .channelTabs-closeTab:hover {
	background: rgb(237, 66, 69) !important;
	color: var(--interactive-active) !important;
}
html .channelTabs-newTab {
	position: static;
	display: flex;
	justify-content: center;
	align-items: center;
	background: rgba(var(--transparencycolor), .3);
	color: var(--interactive-hover);
	padding: 0;
	width: 22px;
	height: 22px;
}
html .channelTabs-newTab:hover {
	background: rgb(var(--accentcolor));
	color: var(--interactive-active);
}

/* ----		18.10	TYPINGINDICATOR					---- */

html .typingindicator-guild,
html .typingindicator-dms,
html .typingindicator-folder {
	background: rgb(var(--transparencycolor), .2);
	border: 4px solid rgb(var(--transparencycolor), .2);
	box-shadow: unset;
	right: 8px;
	bottom: -5px;
	padding: 2px 0;
}

/* ----		18.11	BADGESEVERYWHERE				---- */

.inner-dA0J42:not(.colored-1armap) .badge-7CsdQq:not(.indicator-cY1-b4) {
	background: #fff;
}
.badgesChat-f_cbR8 .inner-dA0J42:not(.colored-1armap) .badge-7CsdQq:not(.indicator-cY1-b4),
.badgesList-Aw_p52 .inner-dA0J42:not(.colored-1armap) .badge-7CsdQq:not(.indicator-cY1-b4),
.badgesSettings-ychoGn .inner-dA0J42:not(.colored-1armap) .badge-7CsdQq:not(.indicator-cY1-b4) {
	background: var(--header-secondary);
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeStaff-3BXdTO {
	-webkit-mask: url(https://discord.com/assets/7cfd90c8062139e4804a1fa59f564731.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgePartner-j6Lwhr {
	-webkit-mask: url(https://discord.com/assets/a0e288a458c48dfcf548dadc277e42e6.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeHypesquad-12E2P6 {
	-webkit-mask: url(https://discord.com/assets/3a050fcc884255231b99b7033c776070.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse1-3rBtjf {
	-webkit-mask: url(https://discord.com/assets/1115767aed344e96a27a12e97718c171.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse2-2oU04B {
	-webkit-mask: url(https://discord.com/assets/d3478c6bd5cee0fc600e55935ddc81aa.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse3-1DoJkv {
	-webkit-mask: url(https://discord.com/assets/2a085ed9c86f3613935a6a8667ba8b89.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse1Winner-3wCl80 {
	-webkit-mask: url(https://discord.com/assets/75f75c3142b8d44ea7052c2bcb9a9043.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse2Winner-AS5bXe {
	-webkit-mask: url(https://discord.com/assets/d4a8fe68fc5f40c8a778f858881a7b84.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeHypeSquadOnlineHouse3Winner-2CwwQi {
	-webkit-mask: url(https://discord.com/assets/5dc48a7859a00e7d95ad8382156aab84.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeEarlySupporter-2ng_jL {
	-webkit-mask: url(https://discord.com/assets/ce15562552e3d70c56d5408cfeed2ffd.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgePremium-1KDZYC {
	-webkit-mask: url(https://discord.com/assets/379d2b3171722ef8be494231234da5d1.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeVerifiedDeveloper-195KfD {
	-webkit-mask: url(https://discord.com/assets/785d81fdbedd133e213da693aba98774.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeBugHunterLevel1-dbEzVz {
	-webkit-mask: url(https://discord.com/assets/df26f079738a4dcd07cbce6eb3c957f1.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileBadgeBugHunterLevel2-3TUciC {
	-webkit-mask: url(https://discord.com/assets/16def052b03d75dac0ed9234c5d6a880.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl1-3oI9tx {
	-webkit-mask: url(https://discord.com/assets/24e49184598820f274e62293349a2e43.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl2-r6nJHT {
	-webkit-mask: url(https://discord.com/assets/cc73fba5c2e9b70752bbd1db35a1b9c3.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl3-38s3Dj {
	-webkit-mask: url(https://discord.com/assets/a4c3939a9b03274246df9b144fcd86cf.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl4-2NXrsI {
	-webkit-mask: url(https://discord.com/assets/d01bee8a9b41bd9dda26a43221b2e7e8.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl5-3XIa2K {
	-webkit-mask: url(https://discord.com/assets/a99def5f819c077e5e5061cab741b7e6.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl6-3e3sxW {
	-webkit-mask: url(https://discord.com/assets/2cfb317f3db3963d8ded9a97ee967bac.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl7-1dVhQT {
	-webkit-mask: url(https://discord.com/assets/278736f579d810b11ddf308cb598b19e.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl8-1kXdFr {
	-webkit-mask: url(https://discord.com/assets/38e40f25802a0fdf480d9b855a37a2f3.svg) center/contain no-repeat;
}
.inner-dA0J42:not(.colored-1armap) .profileGuildSubscriberlvl9-1d6zav {
	-webkit-mask: url(https://discord.com/assets/cfbc2d8ceacfacf07850f986c8165195.svg) center/contain no-repeat;
}


/* ~~~~		19.		UPDATENOTICE					~~~~ */

html:only-child > head + body > div#app-mount.appMount-2yBXZl > div.app-3xd6d0 > div.app-2CXKsg::before {
	content: "Your Version of  Discord is outdated. Please download the newest Version:	https://mwittrien.github.io/downloader/?theme=BasicBackground" !important;
	display: var(--version1_0_5, block) !important;
	background-color: #4a90e2 !important;
	box-shadow: 0 1px 5px 0 rgba(var(--transparencycolor), .3) !important;
	color: var(--header-primary) !important;
	flex-grow: 0 !important;
	flex-shrink: 0 !important;
	font-size: 14px !important;
	font-weight: 500 !important;
	height: 36px !important;
	line-height: 36px !important;
	opacity: 1 !important;
	padding-left: 4px !important;
	padding-right: 28px !important;
	position: relative !important;
	text-align: center !important;
	visibility: unset !important;
	white-space: pre !important;
	top: 0 !important;
	left: 0 !important;
	bottom: unset !important;
	right: unset !important;
	max-width: unset !important;
	min-width: unset !important;
	max-height: unset !important;
	min-height: unset !important;
	transform: unset !important;
	animation: unset !important;
	z-index: 101 !important;
	pointer-events: none !important;
}


/* ~~~~		20.		WATERMARK						~~~~ */

html:only-child > head + body > div#app-mount.appMount-2yBXZl > div.typeWindows-2-g3UY.titleBar-1it3bQ.horizontalReverse-2QssvL.flex-3BkGQD.directionRowReverse-HZatnx.justifyStart-2Mwniq.alignStretch-Uwowzr > div.wordmark-2u86JB {
	display: block !important;
	position: absolute !important;
	max-width: unset !important;
	min-width: unset !important;
	width: 55px !important;
	max-height: unset !important;
	min-height: unset !important;
	height: 16px !important;
	margin: 0 !important;
	padding: 3px 9px 3px !important;
	top: 0 !important;
	left: 0 !important;
	bottom: unset !important;
	right: unset !important;
	opacity: 1 !important;
	visibility: visible !important;
	transform: unset !important;
	animation: unset !important;
}
html:only-child > head + body > div#app-mount.appMount-2yBXZl > div.typeWindows-2-g3UY.titleBar-1it3bQ.horizontalReverse-2QssvL.flex-3BkGQD.directionRowReverse-HZatnx.justifyStart-2Mwniq.alignStretch-Uwowzr > div.wordmark-2u86JB > * {
	display: none !important;
}
html:only-child > head + body > div#app-mount.appMount-2yBXZl > div.typeWindows-2-g3UY.titleBar-1it3bQ.horizontalReverse-2QssvL.flex-3BkGQD.directionRowReverse-HZatnx.justifyStart-2Mwniq.alignStretch-Uwowzr > div.wordmark-2u86JB::before {
	content: "" !important;
	background: rgb(125,125,125) !important;
	-webkit-mask: url('data:image/svg+xml; utf8, <svg width="55" height="19" version="1.1" xmlns="http://www.w3.org/2000/svg"><path fill="black" d="M3.57642276,0.141304348 L0,0.141304348 L0,4.22826087 L2.38069106,6.40217391 L2.38069106,2.43478261 L3.66260163,2.43478261 C4.47052846,2.43478261 4.86910569,2.83695652 4.86910569,3.4673913 L4.86910569,6.5 C4.86910569,7.13043478 4.49207317,7.55434783 3.66260163,7.55434783 L0,7.55434783 L0,9.85869565 L3.57642276,9.85869565 C5.49390244,9.86956522 7.29288618,8.90217391 7.29288618,6.66304348 L7.29288618,3.39130435 C7.29288618,1.13043478 5.49390244,0.141304348 3.57642276,0.141304348 Z M22.3310976,6.67391304 L22.3310976,3.32608696 C22.3310976,2.11956522 24.4640244,1.83695652 25.1103659,3.05434783 L27.0817073,2.23913043 C26.3168699,0.510869565 24.8949187,0 23.7207317,0 C21.803252,0 19.9073171,1.13043478 19.9073171,3.32608696 L19.9073171,6.67391304 C19.9073171,8.88043478 21.803252,10 23.6776423,10 C24.8841463,10 26.3276423,9.39130435 27.1247967,7.81521739 L25.0134146,6.82608696 C24.4963415,8.17391304 22.3310976,7.84782609 22.3310976,6.67391304 Z M15.8030488,3.7826087 C15.0597561,3.61956522 14.5642276,3.34782609 14.5319106,2.88043478 C14.575,1.75 16.2878049,1.7173913 17.2896341,2.79347826 L18.8731707,1.55434783 C17.8821138,0.326086957 16.7617886,0 15.598374,0 C13.8424797,0 12.1404472,1 12.1404472,2.91304348 C12.1404472,4.77173913 13.5408537,5.76086957 15.0813008,6 C15.8676829,6.10869565 16.7402439,6.42391304 16.7186992,6.97826087 C16.654065,8.02173913 14.5426829,7.9673913 13.5839431,6.7826087 L12.0650407,8.23913043 C12.9591463,9.40217391 14.1764228,10 15.3182927,10 C17.074187,10 19.0239837,8.9673913 19.0993902,7.08695652 C19.2071138,4.69565217 17.5050813,4.09782609 15.8030488,3.7826087 Z M8.59634146,9.85869565 L11.0093496,9.85869565 L11.0093496,0.141304348 L8.59634146,0.141304348 L8.59634146,9.85869565 Z M49.2835366,0.141304348 L45.7071138,0.141304348 L45.7071138,4.22826087 L48.0878049,6.40217391 L48.0878049,2.43478261 L49.3589431,2.43478261 C50.1668699,2.43478261 50.5654472,2.83695652 50.5654472,3.4673913 L50.5654472,6.5 C50.5654472,7.13043478 50.1884146,7.55434783 49.3589431,7.55434783 L45.6963415,7.55434783 L45.6963415,9.85869565 L49.2727642,9.85869565 C51.1902439,9.86956522 52.9892276,8.90217391 52.9892276,6.66304348 L52.9892276,3.39130435 C53,1.13043478 51.2010163,0.141304348 49.2835366,0.141304348 Z M31.7353659,0 C29.753252,0 27.7819106,1.09782609 27.7819106,3.33695652 L27.7819106,6.66304348 C27.7819106,8.89130435 29.7640244,10 31.7569106,10 C33.7390244,10 35.7103659,8.89130435 35.7103659,6.66304348 L35.7103659,3.33695652 C35.7103659,1.10869565 33.7174797,0 31.7353659,0 Z M33.2865854,6.66304348 C33.2865854,7.35869565 32.5109756,7.7173913 31.7461382,7.7173913 C30.9705285,7.7173913 30.1949187,7.36956522 30.1949187,6.66304348 L30.1949187,3.33695652 C30.1949187,2.61956522 30.9489837,2.23913043 31.7030488,2.23913043 C32.4894309,2.23913043 33.2865854,2.58695652 33.2865854,3.33695652 L33.2865854,6.66304348 Z M44.3605691,3.33695652 C44.3067073,1.05434783 42.7770325,0.141304348 40.8056911,0.141304348 L36.9815041,0.141304348 L36.9815041,9.86956522 L39.4268293,9.86956522 L39.4268293,6.77173913 L39.8577236,6.77173913 L42.0768293,9.85869565 L45.0930894,9.85869565 L42.4861789,6.52173913 C43.6495935,6.15217391 44.3605691,5.14130435 44.3605691,3.33695652 Z M40.8487805,4.65217391 L39.4268293,4.65217391 L39.4268293,2.43478261 L40.8487805,2.43478261 C42.3784553,2.43478261 42.3784553,4.65217391 40.8487805,4.65217391 Z" transform="translate(1 3)"></path></svg>') center/contain no-repeat !important;
	width: 55px !important;
	height: 19px !important;
	display: inline !important;
	position: absolute !important;
	top: unset !important;
	left: unset !important;
	bottom: unset !important;
	right: unset !important;
	opacity: 1 !important;
	padding: 0 !important;
	margin: 0 !important;
	visibility: visible !important;
	transform: unset !important;
	animation: unset !important;
}
html:only-child > head + body > div#app-mount.appMount-2yBXZl > div.typeWindows-2-g3UY.titleBar-1it3bQ.horizontalReverse-2QssvL.flex-3BkGQD.directionRowReverse-HZatnx.justifyStart-2Mwniq.alignStretch-Uwowzr > div.wordmark-2u86JB::after {
	content: "" !important;
	background: rgb(125,125,125) !important;
	-webkit-mask: url('data:image/svg+xml; utf8, <svg width="242" height="19" version="1.1" xmlns="http://www.w3.org/2000/svg"><path stroke="none" fill="black" fill-rule="evenodd" transform="scale(0.6, 0.6) translate(5,4)" d="M58.488 0.690 C 54.786 0.948,52.503 3.334,52.961 6.466 C 53.321 8.926,55.135 10.509,58.186 11.025 C 60.205 11.366,61.177 12.097,60.818 13.004 C 60.260 14.412,57.255 14.154,55.679 12.564 L 55.440 12.323 55.340 12.411 C 55.125 12.602,52.767 14.824,52.768 14.836 C 52.768 14.843,52.842 14.938,52.932 15.047 C 55.188 17.761,58.434 18.568,61.663 17.218 C 63.879 16.291,65.049 14.673,65.056 12.523 C 65.066 9.499,63.520 7.999,59.581 7.209 C 57.730 6.838,56.956 6.245,57.139 5.336 C 57.409 3.990,59.424 3.729,61.092 4.823 C 61.328 4.978,61.513 5.126,61.754 5.350 L 61.902 5.489 63.269 4.436 C 64.021 3.857,64.640 3.372,64.645 3.357 C 64.668 3.286,63.905 2.499,63.488 2.164 C 62.141 1.082,60.367 0.559,58.488 0.690 M79.453 0.691 C 76.162 0.865,73.785 2.780,73.354 5.604 C 73.306 5.919,73.281 11.980,73.325 12.570 C 73.506 14.979,75.020 16.759,77.535 17.519 C 80.709 18.479,83.881 17.374,85.557 14.725 C 85.782 14.369,85.916 14.116,85.893 14.093 C 85.872 14.073,82.327 12.430,82.254 12.406 C 82.224 12.397,82.198 12.429,82.144 12.544 C 81.882 13.103,81.353 13.555,80.730 13.752 C 79.382 14.177,77.866 13.572,77.593 12.501 C 77.539 12.288,77.540 6.228,77.595 6.015 C 78.042 4.261,81.252 4.104,82.289 5.785 C 82.338 5.865,82.385 5.930,82.393 5.930 C 82.409 5.930,85.820 4.554,85.837 4.541 C 85.856 4.526,85.497 3.838,85.340 3.588 C 84.071 1.573,82.003 0.555,79.453 0.691 M122.233 0.698 C 118.928 0.954,116.621 2.860,116.252 5.640 C 116.198 6.046,116.207 12.646,116.263 13.000 C 116.678 15.665,118.768 17.446,121.919 17.818 C 124.720 18.149,127.505 16.687,128.743 14.235 L 128.815 14.092 128.669 14.026 C 128.589 13.989,127.762 13.608,126.832 13.177 C 125.902 12.747,125.135 12.395,125.129 12.395 C 125.122 12.395,125.079 12.471,125.032 12.564 C 124.149 14.321,121.136 14.341,120.519 12.593 L 120.453 12.407 120.447 9.350 C 120.442 6.713,120.445 6.267,120.476 6.106 C 120.814 4.288,124.035 4.054,125.172 5.764 C 125.233 5.855,125.288 5.930,125.294 5.930 C 125.318 5.930,128.710 4.554,128.727 4.537 C 128.750 4.515,128.506 4.030,128.302 3.691 C 127.042 1.592,124.822 0.498,122.233 0.698 M150.163 0.690 C 146.674 0.881,144.259 2.928,144.024 5.893 C 143.992 6.292,143.992 12.111,144.024 12.535 C 144.229 15.291,146.239 17.273,149.317 17.756 C 152.815 18.304,156.021 16.678,156.902 13.907 C 157.157 13.104,157.167 12.980,157.179 10.250 L 157.190 7.907 153.816 7.907 L 150.442 7.907 150.442 9.686 L 150.442 11.465 151.770 11.465 L 153.098 11.465 153.088 11.948 C 153.069 12.840,152.771 13.335,152.028 13.707 C 150.559 14.443,148.672 13.843,148.297 12.522 L 148.244 12.337 148.244 9.221 L 148.244 6.105 148.296 5.922 C 148.641 4.708,150.215 4.096,151.595 4.640 C 152.111 4.844,152.607 5.305,152.816 5.777 C 152.852 5.859,152.875 5.885,152.903 5.877 C 152.970 5.857,156.383 4.277,156.404 4.256 C 156.456 4.205,156.028 3.438,155.709 3.012 C 154.517 1.418,152.475 0.563,150.163 0.690 M180.081 0.700 C 176.707 0.925,174.383 2.695,173.857 5.442 C 173.796 5.758,173.758 12.153,173.814 12.721 C 174.112 15.773,176.906 17.847,180.721 17.847 C 184.496 17.847,187.238 15.831,187.594 12.794 C 187.645 12.357,187.645 6.177,187.593 5.740 C 187.221 2.553,184.063 0.434,180.081 0.700 M390.026 0.701 C 386.623 0.917,384.214 2.823,383.799 5.628 C 383.750 5.958,383.722 11.716,383.765 12.444 C 383.954 15.593,386.593 17.735,390.430 17.853 C 394.202 17.969,397.090 15.976,397.551 12.938 C 397.616 12.508,397.615 6.017,397.550 5.593 C 397.065 2.452,393.986 0.450,390.026 0.701 M249.326 4.333 C 249.326 7.601,249.328 7.786,249.366 7.797 C 249.389 7.803,250.338 8.626,251.477 9.625 C 252.615 10.624,253.554 11.442,253.564 11.442 C 253.574 11.442,253.581 9.871,253.581 7.952 L 253.581 4.462 254.948 4.471 C 256.262 4.479,256.321 4.481,256.495 4.530 C 257.918 4.924,257.953 6.870,256.547 7.343 L 256.360 7.405 255.366 7.414 L 254.372 7.422 254.372 8.954 L 254.372 10.486 255.413 10.494 C 256.589 10.503,256.592 10.504,257.000 10.704 C 258.198 11.291,258.196 13.081,256.998 13.659 C 256.517 13.891,256.654 13.884,252.716 13.884 L 249.326 13.884 249.326 15.744 L 249.326 17.605 252.831 17.604 C 256.414 17.604,256.877 17.595,257.522 17.512 C 260.168 17.172,261.703 15.747,262.103 13.259 C 262.394 11.447,261.566 9.707,259.993 8.829 C 259.761 8.699,259.762 8.700,259.877 8.639 C 260.813 8.141,261.456 6.960,261.452 5.744 C 261.445 3.299,259.914 1.508,257.419 1.024 C 256.765 0.897,256.875 0.901,252.959 0.890 L 249.326 0.881 249.326 4.333 M317.842 0.913 C 317.848 0.929,319.202 4.691,320.851 9.273 L 323.849 17.604 325.791 17.604 L 327.733 17.605 330.739 9.259 C 332.392 4.669,333.744 0.907,333.744 0.899 C 333.744 0.891,332.721 0.884,331.471 0.884 L 329.198 0.884 327.877 4.983 L 326.556 9.081 326.185 11.012 C 325.982 12.073,325.815 12.955,325.814 12.971 C 325.814 12.987,325.801 13.000,325.785 13.000 C 325.765 13.000,325.639 12.389,325.380 11.025 L 325.004 9.049 323.695 4.966 L 322.385 0.884 320.109 0.884 C 318.298 0.884,317.834 0.890,317.842 0.913 M354.349 4.333 C 354.349 7.601,354.351 7.786,354.390 7.797 C 354.412 7.803,355.362 8.626,356.500 9.625 C 357.638 10.624,358.578 11.442,358.587 11.442 C 358.597 11.442,358.605 9.871,358.605 7.952 L 358.605 4.462 359.971 4.471 C 361.286 4.479,361.344 4.481,361.519 4.530 C 362.941 4.924,362.976 6.870,361.570 7.343 L 361.384 7.405 360.390 7.414 L 359.395 7.422 359.395 8.954 L 359.395 10.486 360.436 10.494 C 361.613 10.503,361.615 10.504,362.023 10.704 C 363.221 11.291,363.220 13.081,362.021 13.659 C 361.541 13.891,361.678 13.884,357.739 13.884 L 354.349 13.884 354.349 15.744 L 354.349 17.605 357.855 17.604 C 361.438 17.604,361.900 17.595,362.546 17.512 C 365.191 17.172,366.726 15.747,367.126 13.259 C 367.418 11.447,366.589 9.707,365.017 8.829 C 364.784 8.699,364.785 8.700,364.900 8.639 C 365.836 8.141,366.479 6.960,366.475 5.744 C 366.468 3.299,364.938 1.508,362.442 1.024 C 361.788 0.897,361.898 0.901,357.983 0.890 L 354.349 0.881 354.349 4.333 M24.186 4.356 C 24.186 7.624,24.188 7.809,24.227 7.820 C 24.249 7.827,25.199 8.649,26.337 9.648 C 27.476 10.647,28.415 11.465,28.424 11.465 C 28.434 11.465,28.442 9.895,28.442 7.975 L 28.442 4.485 29.808 4.494 C 31.123 4.502,31.181 4.505,31.356 4.553 C 32.778 4.947,32.813 6.893,31.407 7.366 L 31.221 7.429 30.227 7.437 L 29.233 7.445 29.233 8.977 L 29.233 10.509 30.273 10.517 C 31.450 10.527,31.452 10.527,31.860 10.727 C 33.058 11.314,33.057 13.104,31.858 13.682 C 31.378 13.914,31.515 13.907,27.576 13.907 L 24.186 13.907 24.186 15.767 L 24.186 17.628 27.692 17.627 C 31.275 17.627,31.737 17.618,32.383 17.535 C 35.028 17.195,36.564 15.770,36.964 13.282 C 37.255 11.471,36.426 9.731,34.854 8.852 C 34.621 8.722,34.622 8.724,34.738 8.662 C 35.674 8.165,36.316 6.984,36.312 5.767 C 36.305 3.322,34.775 1.531,32.279 1.047 C 31.625 0.921,31.735 0.924,27.820 0.914 L 24.186 0.904 24.186 4.356 M42.922 0.925 C 42.916 0.934,41.608 4.678,40.015 9.244 C 38.423 13.811,37.113 17.565,37.104 17.587 C 37.089 17.626,37.206 17.628,39.368 17.628 C 41.519 17.628,41.649 17.626,41.660 17.587 C 41.667 17.565,41.898 16.817,42.173 15.925 C 42.449 15.034,42.674 14.298,42.674 14.292 C 42.674 14.285,43.673 14.279,44.894 14.279 L 47.114 14.279 47.346 14.994 C 47.474 15.388,47.718 16.141,47.888 16.669 L 48.198 17.628 50.473 17.628 C 52.284 17.628,52.747 17.622,52.739 17.599 C 52.734 17.583,51.390 13.821,49.754 9.238 L 46.779 0.907 44.856 0.907 C 43.798 0.907,42.928 0.915,42.922 0.925 M66.860 9.267 L 66.860 17.628 68.977 17.628 L 71.093 17.628 71.093 9.267 L 71.093 0.907 68.977 0.907 L 66.860 0.907 66.860 9.267 M103.247 9.239 C 101.649 13.821,100.337 17.583,100.331 17.599 C 100.323 17.622,100.786 17.628,102.598 17.628 L 104.875 17.628 105.348 16.099 C 105.609 15.258,105.841 14.504,105.865 14.424 L 105.909 14.279 108.128 14.279 L 110.346 14.279 110.448 14.599 C 110.504 14.775,110.747 15.528,110.989 16.273 L 111.427 17.628 113.704 17.628 C 115.516 17.628,115.980 17.622,115.971 17.599 C 115.965 17.583,114.622 13.821,112.986 9.239 L 110.012 0.908 108.081 0.908 L 106.151 0.908 103.247 9.239 M130.326 9.267 L 130.326 17.628 132.453 17.628 L 134.581 17.628 134.581 14.740 L 134.581 11.851 134.644 11.761 C 134.696 11.686,134.711 11.676,134.731 11.705 C 134.745 11.723,135.703 13.064,136.860 14.683 L 138.965 17.627 141.648 17.627 C 144.025 17.628,144.329 17.624,144.317 17.593 C 144.308 17.568,137.994 9.268,137.789 9.011 C 137.778 8.996,139.071 7.397,141.060 4.969 C 142.869 2.759,144.349 0.941,144.349 0.929 C 144.349 0.915,143.342 0.907,141.715 0.908 L 139.081 0.909 136.837 3.975 L 134.593 7.041 134.587 3.974 L 134.581 0.907 132.453 0.907 L 130.326 0.907 130.326 9.267 M159.116 9.266 L 159.116 17.628 161.256 17.628 L 163.395 17.628 163.395 14.977 L 163.395 12.326 163.762 12.326 L 164.129 12.326 166.058 14.976 L 167.988 17.626 170.625 17.627 C 172.875 17.628,173.259 17.623,173.248 17.595 C 173.241 17.577,172.224 16.288,170.987 14.730 C 169.750 13.172,168.747 11.894,168.759 11.890 C 170.569 11.276,171.641 9.837,171.917 7.651 C 172.346 4.246,170.890 1.873,167.930 1.154 C 166.981 0.924,166.973 0.924,162.785 0.913 L 159.116 0.904 159.116 9.266 M189.767 6.704 C 189.767 12.984,189.763 12.742,189.893 13.354 C 190.564 16.526,194.059 18.450,197.907 17.766 C 200.535 17.299,202.429 15.647,202.943 13.372 C 203.088 12.729,203.079 13.167,203.087 6.750 L 203.094 0.907 200.955 0.907 L 198.815 0.907 198.808 6.599 C 198.801 11.986,198.798 12.299,198.759 12.453 C 198.236 14.492,194.735 14.570,194.112 12.558 L 194.058 12.384 194.052 6.645 L 194.046 0.907 191.907 0.907 L 189.767 0.907 189.767 6.704 M205.558 9.267 L 205.558 17.628 207.674 17.628 L 209.791 17.628 209.790 14.238 L 209.790 10.849 209.526 9.285 C 209.175 7.205,209.135 7.199,210.080 9.366 L 210.797 11.012 212.694 14.320 L 214.591 17.628 216.726 17.628 L 218.860 17.628 218.860 9.267 L 218.860 0.907 216.756 0.907 L 214.651 0.907 214.651 4.682 C 214.651 7.186,214.659 8.500,214.675 8.587 C 214.747 8.973,215.111 11.338,215.102 11.354 C 215.060 11.421,214.969 11.226,214.320 9.692 L 213.610 8.012 211.600 4.465 L 209.590 0.919 207.574 0.913 L 205.558 0.907 205.558 9.267 M221.488 4.334 C 221.488 7.579,221.491 7.763,221.529 7.774 C 221.551 7.780,222.501 8.603,223.640 9.602 C 224.778 10.601,225.717 11.418,225.727 11.418 C 225.736 11.419,225.744 9.948,225.744 8.150 L 225.744 4.881 227.087 4.889 L 228.430 4.897 228.663 4.960 C 229.357 5.146,229.767 5.539,229.922 6.163 C 229.963 6.328,229.965 6.490,229.965 9.244 L 229.965 12.151 229.913 12.349 C 229.704 13.139,229.110 13.560,228.105 13.628 C 227.923 13.641,226.390 13.651,224.634 13.651 L 221.488 13.651 221.488 15.640 L 221.488 17.628 224.738 17.628 C 228.530 17.628,228.747 17.619,229.628 17.442 C 232.189 16.927,233.789 15.382,234.170 13.058 C 234.229 12.694,234.263 6.624,234.209 5.965 C 233.966 2.989,231.727 1.114,228.198 0.930 C 227.951 0.918,226.369 0.907,224.622 0.907 L 221.488 0.907 221.488 4.334 M261.518 0.936 C 261.525 0.952,262.834 3.230,264.428 5.997 L 267.326 11.030 267.326 14.329 L 267.326 17.628 269.453 17.628 L 271.581 17.628 271.581 14.331 L 271.581 11.034 274.491 6.000 C 276.091 3.232,277.406 0.953,277.412 0.937 C 277.421 0.913,276.956 0.907,274.937 0.907 L 272.450 0.907 270.952 3.953 C 270.128 5.629,269.448 7.000,269.442 6.999 C 269.435 6.999,268.756 5.628,267.932 3.953 L 266.435 0.907 263.971 0.907 C 262.009 0.907,261.509 0.913,261.518 0.936 M290.535 4.334 C 290.535 7.579,290.537 7.763,290.576 7.774 C 290.598 7.780,291.548 8.603,292.686 9.602 C 293.824 10.601,294.764 11.418,294.773 11.418 C 294.783 11.419,294.791 9.948,294.791 8.150 L 294.791 4.881 296.134 4.889 L 297.477 4.897 297.709 4.960 C 298.403 5.146,298.814 5.539,298.968 6.163 C 299.009 6.328,299.012 6.490,299.012 9.244 L 299.012 12.151 298.959 12.349 C 298.751 13.139,298.157 13.560,297.151 13.628 C 296.970 13.641,295.436 13.651,293.680 13.651 L 290.535 13.651 290.535 15.640 L 290.535 17.628 293.785 17.628 C 297.577 17.628,297.794 17.619,298.674 17.442 C 301.235 16.927,302.836 15.382,303.216 13.058 C 303.276 12.694,303.310 6.624,303.256 5.965 C 303.013 2.989,300.774 1.114,297.244 0.930 C 296.998 0.918,295.416 0.907,293.669 0.907 L 290.535 0.907 290.535 4.334 M305.512 9.267 L 305.512 17.628 311.337 17.628 L 317.163 17.628 317.163 15.616 L 317.163 13.605 313.488 13.605 L 309.814 13.605 309.814 12.372 L 309.814 11.140 313.186 11.140 L 316.558 11.140 316.558 9.302 L 316.558 7.465 313.186 7.465 L 309.814 7.465 309.814 6.186 L 309.814 4.907 313.488 4.907 L 317.163 4.907 317.163 2.907 L 317.163 0.907 311.337 0.907 L 305.512 0.907 305.512 9.267 M334.814 9.267 L 334.814 17.628 336.942 17.628 L 339.070 17.628 339.070 9.267 L 339.070 0.907 336.942 0.907 L 334.814 0.907 334.814 9.267 M341.674 9.267 L 341.674 17.628 347.198 17.628 L 352.721 17.628 352.721 15.523 L 352.721 13.419 349.326 13.419 L 345.930 13.419 345.930 7.163 L 345.930 0.907 343.802 0.907 L 341.674 0.907 341.674 9.267 M369.070 9.267 L 369.070 17.628 371.221 17.628 L 373.372 17.628 373.372 14.977 L 373.372 12.326 373.738 12.327 L 374.105 12.328 376.034 14.978 L 377.963 17.628 380.598 17.628 C 382.047 17.628,383.232 17.620,383.232 17.610 C 383.232 17.601,382.367 16.505,381.311 15.174 C 380.254 13.844,379.235 12.561,379.047 12.324 L 378.704 11.891 378.916 11.815 C 380.927 11.094,382.015 9.124,381.947 6.327 C 381.871 3.234,380.093 1.352,376.892 0.978 C 376.397 0.920,375.607 0.908,372.424 0.907 L 369.070 0.907 369.070 9.267 M87.395 4.380 C 87.395 7.647,87.398 7.832,87.436 7.843 C 87.458 7.850,88.408 8.672,89.547 9.672 C 90.685 10.671,91.624 11.488,91.634 11.488 C 91.643 11.488,91.651 9.918,91.651 7.998 L 91.651 4.508 93.017 4.517 C 94.332 4.526,94.391 4.528,94.565 4.576 C 95.987 4.971,96.023 6.916,94.616 7.389 L 94.430 7.452 93.436 7.460 L 92.442 7.468 92.442 9.000 L 92.442 10.532 93.483 10.541 C 94.659 10.550,94.662 10.550,95.070 10.750 C 96.268 11.337,96.266 13.127,95.067 13.706 C 94.587 13.937,94.724 13.930,90.785 13.930 L 87.395 13.930 87.395 15.791 L 87.395 17.651 90.901 17.651 C 94.484 17.650,94.947 17.641,95.592 17.558 C 98.238 17.219,99.773 15.793,100.173 13.306 C 100.464 11.494,99.636 9.754,98.063 8.875 C 97.831 8.745,97.832 8.747,97.947 8.686 C 98.883 8.188,99.526 7.007,99.522 5.791 C 99.514 3.345,97.984 1.554,95.488 1.071 C 94.834 0.944,94.944 0.947,91.029 0.937 L 87.395 0.927 87.395 4.380 M181.387 4.605 C 182.483 4.791,183.204 5.337,183.359 6.098 C 183.414 6.371,183.414 12.174,183.358 12.426 C 182.924 14.391,178.570 14.432,178.069 12.475 C 178.004 12.220,177.997 6.370,178.061 6.086 C 178.311 4.984,179.776 4.331,181.387 4.605 M391.352 4.603 C 392.415 4.786,393.110 5.288,393.318 6.023 C 393.384 6.258,393.384 12.254,393.318 12.488 C 392.775 14.411,388.490 14.392,388.036 12.464 C 387.983 12.238,387.982 6.267,388.035 6.057 C 388.309 4.975,389.775 4.332,391.352 4.603 M166.461 4.949 C 168.323 5.517,168.296 8.092,166.423 8.599 L 166.198 8.660 164.797 8.669 L 163.395 8.678 163.395 6.780 L 163.395 4.881 164.843 4.889 C 166.263 4.897,166.294 4.898,166.461 4.949 M376.423 4.947 C 378.081 5.414,378.313 7.706,376.779 8.453 C 376.357 8.659,376.206 8.674,374.634 8.674 L 373.372 8.674 373.372 6.778 L 373.372 4.882 374.808 4.889 C 376.199 4.896,376.250 4.898,376.423 4.947 M44.953 5.669 C 44.953 5.679,45.210 6.770,45.523 8.093 C 45.837 9.416,46.093 10.501,46.093 10.505 C 46.093 10.509,45.538 10.512,44.859 10.512 C 43.881 10.512,43.626 10.506,43.635 10.483 C 43.641 10.467,43.916 9.373,44.247 8.052 C 44.823 5.756,44.851 5.651,44.901 5.651 C 44.930 5.651,44.953 5.659,44.953 5.669 M108.742 8.052 C 109.054 9.373,109.314 10.467,109.320 10.483 C 109.328 10.506,109.073 10.512,108.093 10.512 C 107.113 10.512,106.858 10.506,106.865 10.483 C 106.871 10.467,107.147 9.373,107.478 8.052 C 108.029 5.862,108.085 5.651,108.128 5.651 C 108.171 5.651,108.222 5.849,108.742 8.052 M5.419 9.453 L 5.419 11.465 9.105 11.465 L 12.791 11.465 12.791 9.453 L 12.791 7.442 9.105 7.442 L 5.419 7.442 5.419 9.453"></path></svg>') center/contain no-repeat !important;
	width: 242px !important;
	height: 19px !important;
	display: inline !important;
	position: absolute !important;
	top: unset !important;
	left: 64px !important;
	bottom: unset !important;
	right: unset !important;
	opacity: 1 !important;
	padding: 0 !important;
	margin: 0 !important;
	visibility: visible !important;
	transform: unset !important;
	animation: unset !important;
}

html:only-child > head + body > div#app-mount.appMount-2yBXZl > div.app-3xd6d0 > div.app-2CXKsg > div.layers-OrUESM.layers-1YQhyW > div.layer-86YKbF.baseLayer-W6S8cY + div.layer-86YKbF > div.standardSidebarView-E9Pc3j::after {
	content: url('data:image/svg+xml; utf8, <svg width="400" height="18" version="1.1" xmlns="http://www.w3.org/2000/svg"><path stroke="none" fill="rgb(255, 255, 255)" fill-rule="evenodd" d="M58.488 0.690 C 54.786 0.948,52.503 3.334,52.961 6.466 C 53.321 8.926,55.135 10.509,58.186 11.025 C 60.205 11.366,61.177 12.097,60.818 13.004 C 60.260 14.412,57.255 14.154,55.679 12.564 L 55.440 12.323 55.340 12.411 C 55.125 12.602,52.767 14.824,52.768 14.836 C 52.768 14.843,52.842 14.938,52.932 15.047 C 55.188 17.761,58.434 18.568,61.663 17.218 C 63.879 16.291,65.049 14.673,65.056 12.523 C 65.066 9.499,63.520 7.999,59.581 7.209 C 57.730 6.838,56.956 6.245,57.139 5.336 C 57.409 3.990,59.424 3.729,61.092 4.823 C 61.328 4.978,61.513 5.126,61.754 5.350 L 61.902 5.489 63.269 4.436 C 64.021 3.857,64.640 3.372,64.645 3.357 C 64.668 3.286,63.905 2.499,63.488 2.164 C 62.141 1.082,60.367 0.559,58.488 0.690 M79.453 0.691 C 76.162 0.865,73.785 2.780,73.354 5.604 C 73.306 5.919,73.281 11.980,73.325 12.570 C 73.506 14.979,75.020 16.759,77.535 17.519 C 80.709 18.479,83.881 17.374,85.557 14.725 C 85.782 14.369,85.916 14.116,85.893 14.093 C 85.872 14.073,82.327 12.430,82.254 12.406 C 82.224 12.397,82.198 12.429,82.144 12.544 C 81.882 13.103,81.353 13.555,80.730 13.752 C 79.382 14.177,77.866 13.572,77.593 12.501 C 77.539 12.288,77.540 6.228,77.595 6.015 C 78.042 4.261,81.252 4.104,82.289 5.785 C 82.338 5.865,82.385 5.930,82.393 5.930 C 82.409 5.930,85.820 4.554,85.837 4.541 C 85.856 4.526,85.497 3.838,85.340 3.588 C 84.071 1.573,82.003 0.555,79.453 0.691 M122.233 0.698 C 118.928 0.954,116.621 2.860,116.252 5.640 C 116.198 6.046,116.207 12.646,116.263 13.000 C 116.678 15.665,118.768 17.446,121.919 17.818 C 124.720 18.149,127.505 16.687,128.743 14.235 L 128.815 14.092 128.669 14.026 C 128.589 13.989,127.762 13.608,126.832 13.177 C 125.902 12.747,125.135 12.395,125.129 12.395 C 125.122 12.395,125.079 12.471,125.032 12.564 C 124.149 14.321,121.136 14.341,120.519 12.593 L 120.453 12.407 120.447 9.350 C 120.442 6.713,120.445 6.267,120.476 6.106 C 120.814 4.288,124.035 4.054,125.172 5.764 C 125.233 5.855,125.288 5.930,125.294 5.930 C 125.318 5.930,128.710 4.554,128.727 4.537 C 128.750 4.515,128.506 4.030,128.302 3.691 C 127.042 1.592,124.822 0.498,122.233 0.698 M150.163 0.690 C 146.674 0.881,144.259 2.928,144.024 5.893 C 143.992 6.292,143.992 12.111,144.024 12.535 C 144.229 15.291,146.239 17.273,149.317 17.756 C 152.815 18.304,156.021 16.678,156.902 13.907 C 157.157 13.104,157.167 12.980,157.179 10.250 L 157.190 7.907 153.816 7.907 L 150.442 7.907 150.442 9.686 L 150.442 11.465 151.770 11.465 L 153.098 11.465 153.088 11.948 C 153.069 12.840,152.771 13.335,152.028 13.707 C 150.559 14.443,148.672 13.843,148.297 12.522 L 148.244 12.337 148.244 9.221 L 148.244 6.105 148.296 5.922 C 148.641 4.708,150.215 4.096,151.595 4.640 C 152.111 4.844,152.607 5.305,152.816 5.777 C 152.852 5.859,152.875 5.885,152.903 5.877 C 152.970 5.857,156.383 4.277,156.404 4.256 C 156.456 4.205,156.028 3.438,155.709 3.012 C 154.517 1.418,152.475 0.563,150.163 0.690 M180.081 0.700 C 176.707 0.925,174.383 2.695,173.857 5.442 C 173.796 5.758,173.758 12.153,173.814 12.721 C 174.112 15.773,176.906 17.847,180.721 17.847 C 184.496 17.847,187.238 15.831,187.594 12.794 C 187.645 12.357,187.645 6.177,187.593 5.740 C 187.221 2.553,184.063 0.434,180.081 0.700 M390.026 0.701 C 386.623 0.917,384.214 2.823,383.799 5.628 C 383.750 5.958,383.722 11.716,383.765 12.444 C 383.954 15.593,386.593 17.735,390.430 17.853 C 394.202 17.969,397.090 15.976,397.551 12.938 C 397.616 12.508,397.615 6.017,397.550 5.593 C 397.065 2.452,393.986 0.450,390.026 0.701 M249.326 4.333 C 249.326 7.601,249.328 7.786,249.366 7.797 C 249.389 7.803,250.338 8.626,251.477 9.625 C 252.615 10.624,253.554 11.442,253.564 11.442 C 253.574 11.442,253.581 9.871,253.581 7.952 L 253.581 4.462 254.948 4.471 C 256.262 4.479,256.321 4.481,256.495 4.530 C 257.918 4.924,257.953 6.870,256.547 7.343 L 256.360 7.405 255.366 7.414 L 254.372 7.422 254.372 8.954 L 254.372 10.486 255.413 10.494 C 256.589 10.503,256.592 10.504,257.000 10.704 C 258.198 11.291,258.196 13.081,256.998 13.659 C 256.517 13.891,256.654 13.884,252.716 13.884 L 249.326 13.884 249.326 15.744 L 249.326 17.605 252.831 17.604 C 256.414 17.604,256.877 17.595,257.522 17.512 C 260.168 17.172,261.703 15.747,262.103 13.259 C 262.394 11.447,261.566 9.707,259.993 8.829 C 259.761 8.699,259.762 8.700,259.877 8.639 C 260.813 8.141,261.456 6.960,261.452 5.744 C 261.445 3.299,259.914 1.508,257.419 1.024 C 256.765 0.897,256.875 0.901,252.959 0.890 L 249.326 0.881 249.326 4.333 M317.842 0.913 C 317.848 0.929,319.202 4.691,320.851 9.273 L 323.849 17.604 325.791 17.604 L 327.733 17.605 330.739 9.259 C 332.392 4.669,333.744 0.907,333.744 0.899 C 333.744 0.891,332.721 0.884,331.471 0.884 L 329.198 0.884 327.877 4.983 L 326.556 9.081 326.185 11.012 C 325.982 12.073,325.815 12.955,325.814 12.971 C 325.814 12.987,325.801 13.000,325.785 13.000 C 325.765 13.000,325.639 12.389,325.380 11.025 L 325.004 9.049 323.695 4.966 L 322.385 0.884 320.109 0.884 C 318.298 0.884,317.834 0.890,317.842 0.913 M354.349 4.333 C 354.349 7.601,354.351 7.786,354.390 7.797 C 354.412 7.803,355.362 8.626,356.500 9.625 C 357.638 10.624,358.578 11.442,358.587 11.442 C 358.597 11.442,358.605 9.871,358.605 7.952 L 358.605 4.462 359.971 4.471 C 361.286 4.479,361.344 4.481,361.519 4.530 C 362.941 4.924,362.976 6.870,361.570 7.343 L 361.384 7.405 360.390 7.414 L 359.395 7.422 359.395 8.954 L 359.395 10.486 360.436 10.494 C 361.613 10.503,361.615 10.504,362.023 10.704 C 363.221 11.291,363.220 13.081,362.021 13.659 C 361.541 13.891,361.678 13.884,357.739 13.884 L 354.349 13.884 354.349 15.744 L 354.349 17.605 357.855 17.604 C 361.438 17.604,361.900 17.595,362.546 17.512 C 365.191 17.172,366.726 15.747,367.126 13.259 C 367.418 11.447,366.589 9.707,365.017 8.829 C 364.784 8.699,364.785 8.700,364.900 8.639 C 365.836 8.141,366.479 6.960,366.475 5.744 C 366.468 3.299,364.938 1.508,362.442 1.024 C 361.788 0.897,361.898 0.901,357.983 0.890 L 354.349 0.881 354.349 4.333 M24.186 4.356 C 24.186 7.624,24.188 7.809,24.227 7.820 C 24.249 7.827,25.199 8.649,26.337 9.648 C 27.476 10.647,28.415 11.465,28.424 11.465 C 28.434 11.465,28.442 9.895,28.442 7.975 L 28.442 4.485 29.808 4.494 C 31.123 4.502,31.181 4.505,31.356 4.553 C 32.778 4.947,32.813 6.893,31.407 7.366 L 31.221 7.429 30.227 7.437 L 29.233 7.445 29.233 8.977 L 29.233 10.509 30.273 10.517 C 31.450 10.527,31.452 10.527,31.860 10.727 C 33.058 11.314,33.057 13.104,31.858 13.682 C 31.378 13.914,31.515 13.907,27.576 13.907 L 24.186 13.907 24.186 15.767 L 24.186 17.628 27.692 17.627 C 31.275 17.627,31.737 17.618,32.383 17.535 C 35.028 17.195,36.564 15.770,36.964 13.282 C 37.255 11.471,36.426 9.731,34.854 8.852 C 34.621 8.722,34.622 8.724,34.738 8.662 C 35.674 8.165,36.316 6.984,36.312 5.767 C 36.305 3.322,34.775 1.531,32.279 1.047 C 31.625 0.921,31.735 0.924,27.820 0.914 L 24.186 0.904 24.186 4.356 M42.922 0.925 C 42.916 0.934,41.608 4.678,40.015 9.244 C 38.423 13.811,37.113 17.565,37.104 17.587 C 37.089 17.626,37.206 17.628,39.368 17.628 C 41.519 17.628,41.649 17.626,41.660 17.587 C 41.667 17.565,41.898 16.817,42.173 15.925 C 42.449 15.034,42.674 14.298,42.674 14.292 C 42.674 14.285,43.673 14.279,44.894 14.279 L 47.114 14.279 47.346 14.994 C 47.474 15.388,47.718 16.141,47.888 16.669 L 48.198 17.628 50.473 17.628 C 52.284 17.628,52.747 17.622,52.739 17.599 C 52.734 17.583,51.390 13.821,49.754 9.238 L 46.779 0.907 44.856 0.907 C 43.798 0.907,42.928 0.915,42.922 0.925 M66.860 9.267 L 66.860 17.628 68.977 17.628 L 71.093 17.628 71.093 9.267 L 71.093 0.907 68.977 0.907 L 66.860 0.907 66.860 9.267 M103.247 9.239 C 101.649 13.821,100.337 17.583,100.331 17.599 C 100.323 17.622,100.786 17.628,102.598 17.628 L 104.875 17.628 105.348 16.099 C 105.609 15.258,105.841 14.504,105.865 14.424 L 105.909 14.279 108.128 14.279 L 110.346 14.279 110.448 14.599 C 110.504 14.775,110.747 15.528,110.989 16.273 L 111.427 17.628 113.704 17.628 C 115.516 17.628,115.980 17.622,115.971 17.599 C 115.965 17.583,114.622 13.821,112.986 9.239 L 110.012 0.908 108.081 0.908 L 106.151 0.908 103.247 9.239 M130.326 9.267 L 130.326 17.628 132.453 17.628 L 134.581 17.628 134.581 14.740 L 134.581 11.851 134.644 11.761 C 134.696 11.686,134.711 11.676,134.731 11.705 C 134.745 11.723,135.703 13.064,136.860 14.683 L 138.965 17.627 141.648 17.627 C 144.025 17.628,144.329 17.624,144.317 17.593 C 144.308 17.568,137.994 9.268,137.789 9.011 C 137.778 8.996,139.071 7.397,141.060 4.969 C 142.869 2.759,144.349 0.941,144.349 0.929 C 144.349 0.915,143.342 0.907,141.715 0.908 L 139.081 0.909 136.837 3.975 L 134.593 7.041 134.587 3.974 L 134.581 0.907 132.453 0.907 L 130.326 0.907 130.326 9.267 M159.116 9.266 L 159.116 17.628 161.256 17.628 L 163.395 17.628 163.395 14.977 L 163.395 12.326 163.762 12.326 L 164.129 12.326 166.058 14.976 L 167.988 17.626 170.625 17.627 C 172.875 17.628,173.259 17.623,173.248 17.595 C 173.241 17.577,172.224 16.288,170.987 14.730 C 169.750 13.172,168.747 11.894,168.759 11.890 C 170.569 11.276,171.641 9.837,171.917 7.651 C 172.346 4.246,170.890 1.873,167.930 1.154 C 166.981 0.924,166.973 0.924,162.785 0.913 L 159.116 0.904 159.116 9.266 M189.767 6.704 C 189.767 12.984,189.763 12.742,189.893 13.354 C 190.564 16.526,194.059 18.450,197.907 17.766 C 200.535 17.299,202.429 15.647,202.943 13.372 C 203.088 12.729,203.079 13.167,203.087 6.750 L 203.094 0.907 200.955 0.907 L 198.815 0.907 198.808 6.599 C 198.801 11.986,198.798 12.299,198.759 12.453 C 198.236 14.492,194.735 14.570,194.112 12.558 L 194.058 12.384 194.052 6.645 L 194.046 0.907 191.907 0.907 L 189.767 0.907 189.767 6.704 M205.558 9.267 L 205.558 17.628 207.674 17.628 L 209.791 17.628 209.790 14.238 L 209.790 10.849 209.526 9.285 C 209.175 7.205,209.135 7.199,210.080 9.366 L 210.797 11.012 212.694 14.320 L 214.591 17.628 216.726 17.628 L 218.860 17.628 218.860 9.267 L 218.860 0.907 216.756 0.907 L 214.651 0.907 214.651 4.682 C 214.651 7.186,214.659 8.500,214.675 8.587 C 214.747 8.973,215.111 11.338,215.102 11.354 C 215.060 11.421,214.969 11.226,214.320 9.692 L 213.610 8.012 211.600 4.465 L 209.590 0.919 207.574 0.913 L 205.558 0.907 205.558 9.267 M221.488 4.334 C 221.488 7.579,221.491 7.763,221.529 7.774 C 221.551 7.780,222.501 8.603,223.640 9.602 C 224.778 10.601,225.717 11.418,225.727 11.418 C 225.736 11.419,225.744 9.948,225.744 8.150 L 225.744 4.881 227.087 4.889 L 228.430 4.897 228.663 4.960 C 229.357 5.146,229.767 5.539,229.922 6.163 C 229.963 6.328,229.965 6.490,229.965 9.244 L 229.965 12.151 229.913 12.349 C 229.704 13.139,229.110 13.560,228.105 13.628 C 227.923 13.641,226.390 13.651,224.634 13.651 L 221.488 13.651 221.488 15.640 L 221.488 17.628 224.738 17.628 C 228.530 17.628,228.747 17.619,229.628 17.442 C 232.189 16.927,233.789 15.382,234.170 13.058 C 234.229 12.694,234.263 6.624,234.209 5.965 C 233.966 2.989,231.727 1.114,228.198 0.930 C 227.951 0.918,226.369 0.907,224.622 0.907 L 221.488 0.907 221.488 4.334 M261.518 0.936 C 261.525 0.952,262.834 3.230,264.428 5.997 L 267.326 11.030 267.326 14.329 L 267.326 17.628 269.453 17.628 L 271.581 17.628 271.581 14.331 L 271.581 11.034 274.491 6.000 C 276.091 3.232,277.406 0.953,277.412 0.937 C 277.421 0.913,276.956 0.907,274.937 0.907 L 272.450 0.907 270.952 3.953 C 270.128 5.629,269.448 7.000,269.442 6.999 C 269.435 6.999,268.756 5.628,267.932 3.953 L 266.435 0.907 263.971 0.907 C 262.009 0.907,261.509 0.913,261.518 0.936 M290.535 4.334 C 290.535 7.579,290.537 7.763,290.576 7.774 C 290.598 7.780,291.548 8.603,292.686 9.602 C 293.824 10.601,294.764 11.418,294.773 11.418 C 294.783 11.419,294.791 9.948,294.791 8.150 L 294.791 4.881 296.134 4.889 L 297.477 4.897 297.709 4.960 C 298.403 5.146,298.814 5.539,298.968 6.163 C 299.009 6.328,299.012 6.490,299.012 9.244 L 299.012 12.151 298.959 12.349 C 298.751 13.139,298.157 13.560,297.151 13.628 C 296.970 13.641,295.436 13.651,293.680 13.651 L 290.535 13.651 290.535 15.640 L 290.535 17.628 293.785 17.628 C 297.577 17.628,297.794 17.619,298.674 17.442 C 301.235 16.927,302.836 15.382,303.216 13.058 C 303.276 12.694,303.310 6.624,303.256 5.965 C 303.013 2.989,300.774 1.114,297.244 0.930 C 296.998 0.918,295.416 0.907,293.669 0.907 L 290.535 0.907 290.535 4.334 M305.512 9.267 L 305.512 17.628 311.337 17.628 L 317.163 17.628 317.163 15.616 L 317.163 13.605 313.488 13.605 L 309.814 13.605 309.814 12.372 L 309.814 11.140 313.186 11.140 L 316.558 11.140 316.558 9.302 L 316.558 7.465 313.186 7.465 L 309.814 7.465 309.814 6.186 L 309.814 4.907 313.488 4.907 L 317.163 4.907 317.163 2.907 L 317.163 0.907 311.337 0.907 L 305.512 0.907 305.512 9.267 M334.814 9.267 L 334.814 17.628 336.942 17.628 L 339.070 17.628 339.070 9.267 L 339.070 0.907 336.942 0.907 L 334.814 0.907 334.814 9.267 M341.674 9.267 L 341.674 17.628 347.198 17.628 L 352.721 17.628 352.721 15.523 L 352.721 13.419 349.326 13.419 L 345.930 13.419 345.930 7.163 L 345.930 0.907 343.802 0.907 L 341.674 0.907 341.674 9.267 M369.070 9.267 L 369.070 17.628 371.221 17.628 L 373.372 17.628 373.372 14.977 L 373.372 12.326 373.738 12.327 L 374.105 12.328 376.034 14.978 L 377.963 17.628 380.598 17.628 C 382.047 17.628,383.232 17.620,383.232 17.610 C 383.232 17.601,382.367 16.505,381.311 15.174 C 380.254 13.844,379.235 12.561,379.047 12.324 L 378.704 11.891 378.916 11.815 C 380.927 11.094,382.015 9.124,381.947 6.327 C 381.871 3.234,380.093 1.352,376.892 0.978 C 376.397 0.920,375.607 0.908,372.424 0.907 L 369.070 0.907 369.070 9.267 M87.395 4.380 C 87.395 7.647,87.398 7.832,87.436 7.843 C 87.458 7.850,88.408 8.672,89.547 9.672 C 90.685 10.671,91.624 11.488,91.634 11.488 C 91.643 11.488,91.651 9.918,91.651 7.998 L 91.651 4.508 93.017 4.517 C 94.332 4.526,94.391 4.528,94.565 4.576 C 95.987 4.971,96.023 6.916,94.616 7.389 L 94.430 7.452 93.436 7.460 L 92.442 7.468 92.442 9.000 L 92.442 10.532 93.483 10.541 C 94.659 10.550,94.662 10.550,95.070 10.750 C 96.268 11.337,96.266 13.127,95.067 13.706 C 94.587 13.937,94.724 13.930,90.785 13.930 L 87.395 13.930 87.395 15.791 L 87.395 17.651 90.901 17.651 C 94.484 17.650,94.947 17.641,95.592 17.558 C 98.238 17.219,99.773 15.793,100.173 13.306 C 100.464 11.494,99.636 9.754,98.063 8.875 C 97.831 8.745,97.832 8.747,97.947 8.686 C 98.883 8.188,99.526 7.007,99.522 5.791 C 99.514 3.345,97.984 1.554,95.488 1.071 C 94.834 0.944,94.944 0.947,91.029 0.937 L 87.395 0.927 87.395 4.380 M181.387 4.605 C 182.483 4.791,183.204 5.337,183.359 6.098 C 183.414 6.371,183.414 12.174,183.358 12.426 C 182.924 14.391,178.570 14.432,178.069 12.475 C 178.004 12.220,177.997 6.370,178.061 6.086 C 178.311 4.984,179.776 4.331,181.387 4.605 M391.352 4.603 C 392.415 4.786,393.110 5.288,393.318 6.023 C 393.384 6.258,393.384 12.254,393.318 12.488 C 392.775 14.411,388.490 14.392,388.036 12.464 C 387.983 12.238,387.982 6.267,388.035 6.057 C 388.309 4.975,389.775 4.332,391.352 4.603 M166.461 4.949 C 168.323 5.517,168.296 8.092,166.423 8.599 L 166.198 8.660 164.797 8.669 L 163.395 8.678 163.395 6.780 L 163.395 4.881 164.843 4.889 C 166.263 4.897,166.294 4.898,166.461 4.949 M376.423 4.947 C 378.081 5.414,378.313 7.706,376.779 8.453 C 376.357 8.659,376.206 8.674,374.634 8.674 L 373.372 8.674 373.372 6.778 L 373.372 4.882 374.808 4.889 C 376.199 4.896,376.250 4.898,376.423 4.947 M44.953 5.669 C 44.953 5.679,45.210 6.770,45.523 8.093 C 45.837 9.416,46.093 10.501,46.093 10.505 C 46.093 10.509,45.538 10.512,44.859 10.512 C 43.881 10.512,43.626 10.506,43.635 10.483 C 43.641 10.467,43.916 9.373,44.247 8.052 C 44.823 5.756,44.851 5.651,44.901 5.651 C 44.930 5.651,44.953 5.659,44.953 5.669 M108.742 8.052 C 109.054 9.373,109.314 10.467,109.320 10.483 C 109.328 10.506,109.073 10.512,108.093 10.512 C 107.113 10.512,106.858 10.506,106.865 10.483 C 106.871 10.467,107.147 9.373,107.478 8.052 C 108.029 5.862,108.085 5.651,108.128 5.651 C 108.171 5.651,108.222 5.849,108.742 8.052"></path></svg>') !important;
	display: inline !important;
	position: absolute !important;
	left: unset !important;
	bottom: 7px !important;
	top: unset !important;
	right: 15px !important;
	opacity: 0.3 !important;
	padding: 0 !important;
	margin: 0 !important;
	visibility: visible !important;
	transform: unset !important;
	animation: unset !important;
	pointer-events: none !important;
	z-index: -1 !important;
}
html:only-child > head + body > div#app-mount.appMount-2yBXZl > div.app-3xd6d0 > div.app-2CXKsg > div.layers-OrUESM.layers-1YQhyW > div.layer-86YKbF.baseLayer-W6S8cY + div.layer-86YKbF > div.standardSidebarView-E9Pc3j > div.sidebarRegion-1VBisG > div.sidebarRegionScroller-FXiQOh.thin-31rlnD.scrollerBase-_bVAAt.fade-1R6FHN > nav.sidebar-nqHbhN > div.side-2ur1Qk > div.info-1sUqUG {
	position: relative !important;
}
html:only-child > head + body > div#app-mount.appMount-2yBXZl > div.app-3xd6d0 > div.app-2CXKsg > div.layers-OrUESM.layers-1YQhyW > div.layer-86YKbF.baseLayer-W6S8cY + div.layer-86YKbF > div.standardSidebarView-E9Pc3j > div.sidebarRegion-1VBisG > div.sidebarRegionScroller-FXiQOh.thin-31rlnD.scrollerBase-_bVAAt.fade-1R6FHN > nav.sidebar-nqHbhN > div.side-2ur1Qk > div.info-1sUqUG::after {
	content: "BasicBackground by" !important;
	font-size: 12px !important;
	color: var(--text-muted) !important;
	cursor: pointer !important;
	display: inline !important;
	opacity: 1 !important;
	padding: 0 !important;
	margin: 0 !important;
	cursor: text !important;
	visibility: visible !important;
	position: relative !important;
	top: unset !important;
	left: unset !important;
	bottom: unset !important;
	right: unset !important;
	transform: unset !important;
	animation: unset !important;
}
html:only-child > head + body > div#app-mount.appMount-2yBXZl > div.app-3xd6d0 > div.app-2CXKsg > div.layers-OrUESM.layers-1YQhyW > div.layer-86YKbF.baseLayer-W6S8cY + div.layer-86YKbF > div.standardSidebarView-E9Pc3j > div.sidebarRegion-1VBisG > div.sidebarRegionScroller-FXiQOh.thin-31rlnD.scrollerBase-_bVAAt.fade-1R6FHN > nav.sidebar-nqHbhN > div.side-2ur1Qk > div.info-1sUqUG::before {
	content: "DevilBro" !important;
	font-size: 12px !important;
	color: rgb(var(--accentcolor)) !important;
	display: inline !important;
	opacity: 1 !important;
	padding: 0 !important;
	margin: 0 !important;
	cursor: pointer !important;
	visibility: visible !important;
	position: absolute !important;
	top: unset !important;
	left: 113px !important;
	bottom: 9px !important;
	right: unset !important;
	transform: unset !important;
	animation: unset !important;
}
