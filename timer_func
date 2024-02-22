import logging
import time

log = logging.getLogger(__name__)


def timer_func(func):
    """
    A decorator that logs the execution time of the decorated function.
    """

    def _wrapper(*args, **kwargs):
        t_start = time.perf_counter()
        result = func(*args, **kwargs)
        t_end = time.perf_counter()
        message = f"Time used invoking the method, {func.__name__}: {t_end - t_start:0.4f} seconds"
        print(message)
        log.info(message)
        return result

    return _wrapper
