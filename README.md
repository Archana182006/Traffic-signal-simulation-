#include <stdio.h>
#include <stdlib.h>

void trafficSignal() {
    int signal;

    printf("\n===== TRAFFIC SIGNAL SIMULATION =====\n");
    printf("1. RED - STOP\n");
    printf("2. YELLOW - READY\n");
    printf("3. GREEN - GO\n");
    printf("4. EXIT\n");

    printf("\nEnter signal number: ");
    scanf("%d", &signal);

    switch (signal) {
        case 1:
            printf("\n🔴 RED LIGHT\n");
            printf("STOP! Vehicles must wait.\n");
            break;

        case 2:
            printf("\n🟡 YELLOW LIGHT\n");
            printf("GET READY! Signal is about to change.\n");
            break;

        case 3:
            printf("\n🟢 GREEN LIGHT\n");
            printf("GO! Vehicles can move.\n");
            break;

        case 4:
            printf("\nExiting Traffic Signal Simulation...\n");
            exit(0);

        default:
            printf("\nInvalid choice! Please select 1-4.\n");
    }
}

int main() {
    int choice;

    do {
        trafficSignal();

        printf("\nDo you want to continue?\n");
        printf("1. Yes\n");
        printf("2. No\n");
        printf("Enter choice: ");
        scanf("%d", &choice);

    } while (choice == 1);

    printf("\nTraffic Signal Simulation Ended.\n");

    return 0;
}
