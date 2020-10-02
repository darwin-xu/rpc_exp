msg_clnt.c msg_svc.c msg.h: msg.x
	rpcgen msg.x

rprintmsg: rprintmsg.c msg_clnt.c msg.h
	cc rprintmsg.c msg_clnt.c -o rprintmsg

msg_server: msg_proc.c msg_svc.c msg.h
	cc msg_proc.c msg_svc.c -o msg_server

all: rprintmsg msg_server

clean:
	rm rprintmsg msg_server