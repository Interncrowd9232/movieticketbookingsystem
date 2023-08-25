import java.util.ArrayList;
import java.util.List;

class SurveyQuestion {
    private String question;
    private List<String> options;

    public SurveyQuestion(String question, List<String> options) {
        this.question = question;
        this.options = options;
    }

    public String getQuestion() {
        return question;
    }

    public List<String> getOptions() {
        return options;
    }
}

class Survey {
    private List<SurveyQuestion> questions;

    public Survey() {
        questions = new ArrayList<>();
    }

    public void addQuestion(SurveyQuestion question) {
        questions.add(question);
    }

    public List<SurveyQuestion> getQuestions() {
        return questions;
    }
}

class SurveyResponse {
    private Survey survey;
    private List<String> answers;

    public SurveyResponse(Survey survey) {
        this.survey = survey;
        answers = new ArrayList<>();
    }

    public void submitResponse(String answer) {
        answers.add(answer);
    }

    public List<String> getAnswers() {
        return answers;
    }
}

public class OnlineSurveySystem {
    public static void main(String[] args) {
        // Create a survey
        Survey survey = new Survey();
        
        List<String> options = new ArrayList<>();
        options.add("Option A");
        options.add("Option B");
        options.add("Option C");

        SurveyQuestion question1 = new SurveyQuestion("What is your favorite color?", options);
        SurveyQuestion question2 = new SurveyQuestion("How often do you exercise?", options);

        survey.addQuestion(question1);
        survey.addQuestion(question2);

        // Simulate a user submitting responses
        SurveyResponse response = new SurveyResponse(survey);
        response.submitResponse("Option A");
        response.submitResponse("Option B");

        // Display survey questions and responses
        System.out.println("Survey Questions:");
        for (SurveyQuestion question : survey.getQuestions()) {
            System.out.println(question.getQuestion());
            System.out.println("Options: " + question.getOptions());
        }

        System.out.println("User Responses:");
        for (String answer : response.getAnswers()) {
            System.out.println(answer);
        }
    }
}
