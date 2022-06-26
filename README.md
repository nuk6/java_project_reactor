# java_project_reactor
1) Using Flux & Mono
```java
package com.knidhi.services;

import reactor.core.publisher.Flux;
import reactor.core.publisher.Mono;

import java.util.List;

class FluxAndMono {
    private Flux<String> fruitFlux() {
        return Flux.fromIterable(List.of("Mango", "Apple"));
    }
    private Mono<String> fruitMono() {
        return Mono.just("Mango");
    }
    public static void main(String[] args) {
        new FluxAndMono().fruitMono().subscribe(System.out::println);
    }
}
```
