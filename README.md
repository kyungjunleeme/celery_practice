# toptal
https://www.toptal.com/python/orchestrating-celery-python-background-jobs
https://www.youtube.com/watch?v=MCs5OvhV9S4

# Many Django apps need some kind of out-of-band processing.
https://en.wikipedia.org/wiki/Out-of-band_data

# worker 내부 살펴보기
> worker 내부에서 main process만 사용된다. (확인 필요)

# serializable 관련
https://www.oddbird.net/2017/03/20/serializing-things/

# celery_practice
celery_practice
https://testdriven.io/guides/django-celery/

```shell
[2022-03-27 02:29:55,327: INFO/MainProcess] Connected to redis://redis:6379/0
[2022-03-27 02:29:55,334: INFO/MainProcess] mingle: searching for neighbors
[2022-03-27 02:29:56,357: INFO/MainProcess] mingle: all alone
[2022-03-27 02:29:56,391: WARNING/MainProcess] /usr/local/lib/python3.9/site-packages/celery/fixups/django.py:205: UserWarning: Using settings.DEBUG leads to a memory
            leak, never use this setting in production environments!
  warnings.warn('''Using settings.DEBUG leads to a memory
[2022-03-27 02:29:56,395: INFO/MainProcess] celery@a23d5debf6ea ready.
[2022-03-27 02:34:22,221: INFO/MainProcess] Received task: tasks.sample_tasks.create_task[bd43e99c-d6ca-49f0-97ea-c2d88a158544]  
[2022-03-27 02:34:22,261: INFO/ForkPoolWorker-3] Task tasks.sample_tasks.create_task[bd43e99c-d6ca-49f0-97ea-c2d88a158544] succeeded in 0.01955945800000336s: True
```

![image](https://user-images.githubusercontent.com/45473846/160268521-8dc16f55-c824-42fd-8045-b63045bad752.png)

```sh
docker-compose up -d --build --scale celery=3
```

https://github.com/docker/compose/issues/5251
https://docs.docker.com/compose/reference/scale/
https://docs.docker.com/compose/reference/up/


pytest -k means keyword

https://docs.pytest.org/en/6.2.x/usage.html#specifying-tests-selecting-tests

```
It's worth noting that in the above asserts, we used the .run method (rather than .delay) to run the task directly without a Celery worker.

```

![image](https://user-images.githubusercontent.com/45473846/160268777-76419dc6-453c-4265-b9ea-cce1311ca2b8.png)

django test 시에


client는 따로 명시해주지 않아도, 기본적으로 사용이 가능한 것으로 보임

https://docs.djangoproject.com/en/4.0/topics/testing/tools/


ㄸㅏ로 
ㄸㅏ로 명

