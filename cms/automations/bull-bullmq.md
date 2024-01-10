---
created-on: 2024-01-10T11:59:57.224Z
f_long-description: >-
  ## Description
  

  This codemod provides straightforward changes to migrate from bull to bullmq.
  You have to manually create queue names for the existing queues in your application.
  You need to apply these names for the created workers in the files which previously used .process().
  You will have to manually specify connection details if you used `createClient` method on `new Queue()` options before. Connection details should now also be specified for and `Worker` classes.
  

  
  ### Before
  
  ```ts
  
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
  
  ```ts
  
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
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=PTOOeihWI1CDiFR6TqznRFTLmuM
f_cli-command: intuita bull/bullmq
f_framework: cms/framework/bull.md
f_applicability-criteria: "`bullmq` >= 1.0.0"
f_verified-codemod: false
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: bull-bullmq
title: Bull Vbullmq - Bull to BullMQ
f_slug-name: bull-bullmq
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~10 minutes/occurence"
tags: automations
updated-on: 2024-01-10T11:59:57.224Z
published-on: 2024-01-10T11:59:57.224Z
seo:
  title: Bull Vbullmq - Bull to BullMQ | Codemod.com Automations
  og:title: Bull Vbullmq - Bull to BullMQ | Codemod.com Automations
  twitter:title: Bull Vbullmq - Bull to BullMQ | Codemod.com Automations
  description: This codemod provides straightforward changes to migrate from bull to bullmq.
  twitter:card: This codemod provides straightforward changes to migrate from bull to bullmq.
---
This codemod provides straightforward changes to migrate from bull to bullmq.