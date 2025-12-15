#ifndef ANALYTICS_WORKER_H
#define ANALYTICS_WORKER_H

#include <iostream>
#include <string>
#include <unordered_map>

class AnalyticsWorker {
public:
    void init(const std::string& configPath);
    void run();
    void stop();

protected:
    std::unordered_map<std::string, std::string> _config;
    bool _running;
};

#endif // ANALYTICS_WORKER_H