# Agile Methodology applied in Test Driven Development

Testing will be integrated continuously throughout development. We plan to adopt test early, test often, ensuring each sprint includes writing, executing, and refining tests.

This follows Agile testing quadrants:

1. Unit tests for code working correctly
2. Integration tests for service interaction
3. Manual tests for user workflows

Test cases will be defined before implementing new functionality. This encourages modular design, reduces bugs, and improves maintainability. Test related tasks will be tracked on the team Kanban board alongside features.

## Tools Used

- `pytest` - Unit and Integration testing
- `Manual Testing` - End-to-end testing of the UI and API endpoints with usability tests
- `Insomnia/Bruno` - For API route validation and manual regression checks
- `CI Integration` - Automated test runs on pull requests for continuous integration best practices (GitHub Actions Docs).

## References

- [Software Development Testing](https://www.atlassian.com/agile/software-development/testing)
- [Test Driven Development](https://www.browserstack.com/guide/what-is-test-driven-development)
- [Agile testing quadrants](https://www.atlassian.com/agile/software-development/testing)
