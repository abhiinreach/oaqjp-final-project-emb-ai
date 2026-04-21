import requests
import json

def emotion_detector(text_to_analyze):
    """
    Sends text to the Watson NLP Emotion Predict service and returns 
    the raw response text.
    """
    # The URL provided for the Watson NLP service
    url = 'https://sn-watson-emotion.labs.skills.network/v1/watson.runtime.nlp.v1/NlpService/EmotionPredict'
    
    # Headers required to identify the specific model
    headers = {"grpc-metadata-mm-model-id": "emotion_aggregated-workflow_lang_en_stock"}
    
    # The input JSON structure as required by the API
    input_json = { "raw_document": { "text": text_to_analyze } }
    
    # Execute the POST request
    response = requests.post(url, json=input_json, headers=headers)
    
    # Return the text attribute of the response object
    return response.text