# ✅ Day 2 Outcome

- ✔️ kubectl core commands
- ✔️ Debug skill
- ✔️ Namespace concept clear
- ✔️ GitHub cheatsheet ready




| Command            | কাজ / Purpose                                               | কখন ব্যবহার করতে হবে                                                              | কেনো দরকার                                                                                  | কিভাবে ব্যবহার / Example                                                       | ফিজিক্যাল উদাহরণ                                                                                                        |
| ------------------ | ----------------------------------------------------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------- |
| `kubectl get`      | ক্লাস্টারের রিসোর্সের **সংক্ষিপ্ত তালিকা** দেখায়            | যখন জানতে হবে **কতটি Pod, কোন Deployment, কোন Service চলছে**                      | ক্লাস্টারের সারসংক্ষেপ দেখতে এবং দ্রুত ধারণা পেতে                                           | `kubectl get pods` <br> `kubectl get deployments`                              | ধরো তুমি একটি অফিসে গিয়েছো এবং চেয়েছো **সকল কর্মচারীর নামের তালিকা** দেখতে। `kubectl get` সেই তালিকাকে সরলভাবে দেখায়। |
| `kubectl describe` | একটি রিসোর্সের **বিস্তারিত তথ্য ও স্টেট** দেখায়             | যখন **কোনো Pod বা Deployment ঠিকভাবে কাজ করছে কিনা বা সমস্যা আছে কিনা** দেখতে হবে | রিসোর্সের **status, configuration, events, warnings, errors** চেক করতে                      | `kubectl describe pod my-pod` <br> `kubectl describe deployment my-deployment` | ধরো অফিসে গিয়ে প্রতিটি কর্মচারীর **ডিটেইলস** যেমন ফোন নাম্বার, অফিস রুম, দায়িত্ব ইত্যাদি চেক করছো।                      |
| `kubectl logs`     | Pod-এর container-এর **লগ দেখায়**                            | যখন **কোনো container ঠিকমতো কাজ করছে না বা crash হচ্ছে** দেখতে হবে                | runtime errors, warnings, info messages, CrashLoopBackOff ইত্যাদি debug করতে                | `kubectl logs my-pod` <br> `kubectl logs my-pod -c my-container`               | ধরো কোনো মেশিনের ভিতরে কি হচ্ছে তা দেখতে চাও, যেমন মেশিনের **error report বা কাজের হিস্ট্রি** দেখছো।                    |
| `kubectl exec`     | Pod-এর container এর ভিতরে **command run করা বা shell খোলা** | যখন **container-এর ভিতরে কিছু পরীক্ষা বা পরিবর্তন করতে হবে**                      | container-এর ভিতরে ডিরেক্টরি, ফাইল বা কমান্ড রান করে debugging, inspection, troubleshooting | `kubectl exec my-pod -- ls /app` <br> `kubectl exec -it my-pod -- /bin/bash`   | ধরো তুমি **ক্লাসরুমে প্র্যাকটিক্যাল ল্যাবে ঢুকেছো** এবং সরাসরি কম্পিউটার চালিয়ে পরীক্ষা করছো।                           |
