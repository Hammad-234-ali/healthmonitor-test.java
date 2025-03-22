# healthmonitor-test.java
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.*;

public class HealthMonitorTest {
    @Test
    public void testDetectPhysicalIssues() {
        HealthMonitor monitor = new HealthMonitor();
        monitor.detectPhysicalIssues(200);
        assertTrue(monitor.physicalIssues.size() > 0);
    }

    @Test
    public void testDetectMentalIssues() {
        HealthMonitor monitor = new HealthMonitor();
        monitor.detectMentalIssues(7);
        assertTrue(monitor.mentalIssues.size() > 0);
    }
}
