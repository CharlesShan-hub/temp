## Summary

- Pulsar Functions can be used to provide near real-time machine learning on streaming data to produce actionable insights.

- Providing near real-time predictions requires an ML model that takes a pre-defined set of inputs, known as a feature set.

- A feature is a numeric representation of an individual aspect of an object, such as the average meal preparation time of a restaurant.

- Most features within a feature vector cannot be calculated using the data from a single message, nor can they be computed in a timely manner. Therefore, it is common to have ancillary processing compute these values in the background and store them in a low-latency data store.

- The predictive model markup language (PMML) is a standard format for representing ML models developed in a variety of languages, which helps make ML models portable.

- There is an open-source Java-based project that supports the evaluation of PMML models, which allows us to easily execute any PMML-supported model inside a Pulsar function.

- You can use other language-specific libraries to execute non-PMML models inside Pulsar Functions as well.
