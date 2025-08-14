# Generative Model Output and Hallucinations

Despite employing various prompting techniques, generative models do not always produce perfectly accurate or desired results.  When an image was requested to be transformed into a pencil sketch, while the overall impression was good, subtle details like base designs and flower orientations were altered or omitted. If precise accuracy is required, generative models may fall short. A request to create a visual diagram from text resulted in an aesthetically pleasing "game card" at first glance. However, closer inspection revealed grammatical errors, nonsensical phrases, and illogical imagery.

These inaccuracies are examples of hallucinations, which occur when generative models produce inaccurate, irrelevant, or nonsensical content, whether in images or text. All generative models are prone to hallucination.

This phenomenon necessitates caution when using these models. While some outputs, like a simple email, can be easily verified by a human, larger or more fact-dependent tasks pose a significant challenge.
## Verifying Generative Model Outputs

To boost confidence in AI-generated outputs and understand their accuracy level, A human who's an expert in the field should review the outputs for important documents and tasks.When dealing with tasks that have a "right answer" and are performed repeatedly have a collection of "correct responses" for quicker verification.

> [!NOTE]
> A more unconventional method involves using another Large Language Model (LLM) or even the same model with a different prompt to evaluate the output of a generative model. 
