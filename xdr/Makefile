dir_clnt.c dir_svc.c dir.h dir_xdr.c: dir.x
	rpcgen dir.x

rls: rls.c dir_clnt.c dir_xdr.c
	cc rls.c dir_clnt.c dir_xdr.c -o rls

dir_svc: dir_svc.c dir_proc.c dir_xdr.c
	cc dir_svc.c dir_proc.c dir_xdr.c -o dir_svc

all: rls dir_svc

clean:
	rm rls dir_svc
