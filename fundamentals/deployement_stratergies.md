# Deployment Startergies

- Using the right deployment strategy is crucial for seamlessly integrating new features and updates. - It reduces the risks, avoids interruptions, and delivers a smooth user experience.

<br />

## Most popular deployment patterns:

![Image](https://res.cloudinary.com/djgwvmcdl/image/upload/v1772446683/69d2e3c9-80eb-49c2-9cd6-5f7238fc37e4.png)

- Blue/Green for safety and zero downtime
- Canary for controlled, low-risk rollouts
- Rolling for maintaining continuous operations
- Feature Toggles for flexible feature management
- A/B Testing for data-driven user insights

<br />

## Blue/Green Deployment

![Image](https://res.cloudinary.com/djgwvmcdl/image/upload/v1772445791/9721bacc-2cc9-4d14-8be5-07ca6ca921f7.png)

Maintain two seperate environments. Blue is the active. environment and green is the new environment.

Once the new environment is ready simple move the route from blue to green.

- Renowned for zero downtime, this method uses two environments, Blue and Green. One hosts the live version while the other tests the new version.
- After comprehensive testing without affecting live traffic, users are transitioned to the updated environment.
- If an issue is discovered after switching environments, it is relatively easy to switch back.
- The main challenge is the cost and complexity of managing two environments.
- Quick roll back option.
- Quite complex and cost is high because identical resources.

<br />

## Canary Deployment

Where a new version of the app gradually roll out for subset of users (20% traffic / `Canary Users`), while majority of users (80% traffic) continuinglu using old version. Then gradually switch all the users to the new version.

![Image](https://res.cloudinary.com/djgwvmcdl/image/upload/v1772446184/66467f26-2f16-4d9f-9cd6-305693bfd245.png)

- Named after canary birds in mines, it starts by rolling out changes to a small subset of users.
- This allows for monitoring performance and gathering feedback.
- If successful, you gradually extend the update to more users.
- Excels in minimizing user impact during updates due to isolation of a small set of users.
- To minimize the white scale issues.

<br />

## Rolling Deployment

![Image](https://res.cloudinary.com/djgwvmcdl/image/upload/v1772445602/74e50045-0544-4b58-a190-4d6573db1bdc.png)

New versions of the application increamentally deploy to the servers while gradually replace the old versions

- Updates software in phases, rather than all at once.
- Incrementally upgrades different segments of the system, ensuring most of it remains operational during the deployment.
- Can be ideal for critical systems that require continuous operation.
- However, it extends the total update time and might introduce temporary inconsistencies.

<br />

### Feature Flags Deployment

Let you deploy new features to the production but keep them off by default and can activate while we want.

![Image](https://res.cloudinary.com/djgwvmcdl/image/upload/v1772446364/d1efd8ab-f9da-449c-adc7-10b2d65642bc.png)

- Think of feature toggles as on-off switches for new features.
- They allow teams to deploy features quietly, turning them on for specific users when it makes sense.
- Feature toggles support strategies like canary releases and A/B testing.
- The challenge lies in managing numerous toggles, which can become complex & risk feature conflicts.

<br />

### A/B Testing Deployment

Deployment and experimentation stratergy where the two versions of the application deploy simultaniously to the different user groups.

![Image](https://res.cloudinary.com/djgwvmcdl/image/upload/v1772446505/e83ab89c-555e-4848-b701-160c536923a3.png)

- Comparable to a scientific experiment, A/B testing offers two variations of a feature to different user groups to gauge which performs better.
- It's a go-to for validating user preference and effectiveness of new features, based on concrete data like user engagement or ease of use.