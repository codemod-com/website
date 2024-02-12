---
title: Bull to BullMQ
created-on: 2023-12-08T18:11:47.551Z
updated-on: 2023-12-08T18:11:47.566Z
published-on: 2023-12-08T18:11:47.574Z
f_long-description: >-
  ## Description


  This codemod provides straightforward changes to migrate from `bull` to `bullmq`. You have to manually create queue names for the existing queues in your application. You need to apply these names for the created workers in the files that previously used `.process()`.


  ## Example


  ### Before


  ```typescript

  import Queue from 'bull';

  import Redis from 'ioredis';


  export function createQueue(
  	name: string,
  	defaultJobOptions?: Partial<Queue.JobOptions>,
  ) {
  	const queue = new Queue(name, {
  		createClient(type) {
  			switch (type) {
  				case 'client':
  					return Redis.defaultClient;

  				case 'subscriber':
  					return Redis.defaultSubscriber;

  				case 'bclient':
  			    return new Redis(env.REDIS_URL);

  				default:
  					throw new Error(`Unexpected connection type: ${type}`);
  			}
  		},
  		defaultJobOptions: {
  			removeOnComplete: true,
  			removeOnFail: true,
  			...defaultJobOptions,
  		},
  	});
  	queue.on('stalled', () => {
  		Metrics.increment("bull.jobs.stalled");
  	});
  	queue.on('completed', () => {
  		Metrics.increment("bull.jobs.completed");
  	});
  	queue.on('error', () => {
  		Metrics.increment("bull.jobs.errored");
  	});
  	queue.on('failed', () => {
  		Metrics.increment("bull.jobs.failed");
  	});

  	return queue;
  }


  const queue = createQueue('queue-name');


  queue.process(
  	async function (job) {
  		const event = job.data;
  	},
  );

  ```


  ### After


  ```typescript

  import { Queue, DefaultJobOptions, QueueEvents, Worker } from "bullmq";

  import Redis from 'ioredis';


  export function createQueue(
    name: string,
    defaultJobOptions?: Partial<DefaultJobOptions>,
  ) {
      const queue = new Queue(name, {
        connection: { host: , port:  },
        defaultJobOptions: {
          removeOnComplete: true,
          removeOnFail: true,
          ...defaultJobOptions,
        }
      });
      const queueEvents = new QueueEvents(name);
      queueEvents.on('stalled', () => {
        Metrics.increment("bull.jobs.stalled");
      });
      queueEvents.on('completed', () => {
        Metrics.increment("bull.jobs.completed");
      });
      queueEvents.on('error', () => {
        Metrics.increment("bull.jobs.errored");
      });
      queueEvents.on('failed', () => {
        Metrics.increment("bull.jobs.failed");
      });

      return queue;
  }


  const queue = createQueue('queue-name');


  const worker = new Worker("unknown-name", async function (job) {
    const event = job.data;
  });

  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/bull/bullmq
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=jc8GspuivcASxKyCLsYZ0WbLRgU
f_cli-command: intuita bullmq/from-bull
f_framework: cms/framework/bullmq.md
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: Up to 5 minutes per queue with one single job. Another
  5 minutes for changing the job startup in bullmq.
f_applicability-criteria: Application running `bull` queue jobs.
f_labels:
  - cms/labels/bull-to-bullmq-migration.md
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
f_featured: false
tags: automations
layout: "[automations].html"
date: 2023-12-08T18:11:47.580Z
seo:
  title: Bull to BullMQ Migration Automation
  og:title: Bull to BullMQ Migration Automation
  description: This automation provides straightforward changes to migrate from
    `Bull` to `BullMQ`.
---
This automation provides straightforward changes to migrate from `Bull` to `BullMQ`.