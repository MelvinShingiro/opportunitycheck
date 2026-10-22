# OpportunityCheck deployment plan

This is the deployment plan for the future application. There is no live demo yet.

## Free hosting

Use [Streamlit Community Cloud](https://docs.streamlit.io/deploy/streamlit-community-cloud). It hosts Streamlit apps connected to GitHub for free, subject to its resource limits.

After a working implementation exists:

1. Add `app.py`, a pinned `requirements.txt`, and a small trained model artifact with documented provenance.
2. Keep raw training data, contact information, and credentials out of Git.
3. Run the automated tests and load the saved pipeline locally.
4. Sign in to [Streamlit Community Cloud](https://share.streamlit.io), choose **Create app**, and select this repository and `app.py`.
5. Select a compatible Python version, deploy, and record the resulting `streamlit.app` URL.
6. Test a cold start and the fictional demo examples from the deployed app.

Train locally and deploy only the small CPU prediction pipeline. The planned stack does not require a GPU or a paid language-model API.

Free-tier terms and resource limits can change. Check the provider's documentation when deploying. See the [official deployment instructions](https://docs.streamlit.io/deploy/streamlit-community-cloud/deploy-your-app/deploy).
