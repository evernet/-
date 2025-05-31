ERRORCODE=LAMBDA(Errors,
    LET(
        Remove, SUBSTITUTE(Errors, "ERROR:", ""),
        Filter, MID(Remove, 1, FIND(":", Remove) - 1),
        VALUE(Filter)
    )
);
