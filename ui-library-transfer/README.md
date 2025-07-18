---
page_type: sample
languages:
  - javascript
products:
  - azure
  - azure-communication-services
---

# Get Started with Composites - Handle transfer request

This sample showcases how Call Composites can be used to handle transfer requests so that the call can be transferred by a Teams user to another Teams user. The current beta version can only receive transfer requests from Teams users in 1 on 1 calls.

## Prerequisites

- An Azure account with an active subscription. [Create an account for free](https://azure.microsoft.com/free/?WT.mc_id=A261C142F) .
- [Node.js](https://nodejs.org/en/) Active LTS and Maintenance LTS versions.
- An active Communication Services resource. [Create a Communication Services resource](https://docs.microsoft.com/azure/communication-services/quickstarts/create-communication-resource). You will need the endpoint value for the resource
- Two Teams users in the same tenant as the Azure account. The first Teams user should be called via ad hoc calling. During the call, the first Teams user should transfer you to the second Teams user. Note that you will need to obtain the first Teams user's id in order to call them via ad hoc calling. To learn more about ad hoc calling, go to [storybook documentation for ad hoc calling](https://azure.github.io/communication-ui-library/?path=/docs/concepts-ad-hoc-calling--docs).

## Run the code

1. Run `npm i` on the directory of the project to install dependencies
2. Swap placeholders for identifiers in the code.
   - Go to the `src` folder and find the `INPUTS.tsx` file.
   - Replace the values for the the `userIdentity` and `userToken` for the identity you created in Azure Portal in the `Prerequisites` step.
   - Replace the `participantIds` with an array of one Teams user id.
   - Update the display name to a name of your choice.
   - Save the file.
3. Run `npm run start`

Open your browser to <http://localhost:3000>. You should see the following:
![Composite Loaded State](../media/call-transfer-composite-loaded.png).

Click `Start Call` button to start the call. The following link shows a video of what the transfer process should look like when a Teams user transfers you:

[Transfer process sample video](../media/transfer-call-accepted.mp4)
