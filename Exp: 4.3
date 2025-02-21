import java.util.Scanner;
import java.util.concurrent.locks.Lock;
import java.util.concurrent.locks.ReentrantLock;

class TicketBooking extends Thread {
    private static final Lock lock = new ReentrantLock();
    private static boolean[] seats = new boolean[5]; // 5 seats for simplicity
    private int seatNumber;
    private String customerName;

    public TicketBooking(String customerName, int seatNumber, int priority) {
        this.customerName = customerName;
        this.seatNumber = seatNumber;
        this.setPriority(priority);
    }

    @Override
    public void run() {
        lock.lock();
        try {
            if (!seats[seatNumber]) {
                seats[seatNumber] = true;
                System.out.println(customerName + " successfully booked seat " + seatNumber);
            } else {
                System.out.println(customerName + " failed to book seat " + seatNumber + " (Already booked)");
            }
        } finally {
            lock.unlock();
        }
    }
}

public class TicketBookingSystem {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        TicketBooking[] bookings = new TicketBooking[5]; // Store bookings
        
        System.out.println("Welcome to the Ticket Booking System (Seats: 0-4)");

        for (int i = 0; i < 5; i++) {
            System.out.print("\nEnter Customer Name: ");
            String name = scanner.next();

            System.out.print("Enter Seat Number (0-4): ");
            int seatNumber = scanner.nextInt();
            
            if (seatNumber < 0 || seatNumber >= 5) {
                System.out.println("Invalid seat number! Try again.");
                i--; 
                continue;
            }

            System.out.print("Enter Priority (1 for VIP, 2 for Regular): ");
            int priority = scanner.nextInt();
            int threadPriority = (priority == 1) ? Thread.MAX_PRIORITY : Thread.MIN_PRIORITY;

            bookings[i] = new TicketBooking(name, seatNumber, threadPriority);
        }

        System.out.println("\nProcessing Bookings...\n");
        for (TicketBooking booking : bookings) {
            if (booking != null) {
                booking.start();
            }
        }

        scanner.close();
    }
}
