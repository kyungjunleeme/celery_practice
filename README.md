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
