use std::fs::File;
use std::io::{BufRead, BufReader};

fn count_lines(filename: &str) -> std::io::Result<usize> {
    let file = File::open(filename)?;
    let reader = BufReader::new(file);
    Ok(reader.lines().count())
}

fn main() {
    match count_lines("main.rs") {
        Ok(count) => println!("Line count: {}", count),
        Err(e) => eprintln!("Error: {}", e),
    }
}
