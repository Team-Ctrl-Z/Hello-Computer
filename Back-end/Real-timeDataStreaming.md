Socket.IO와 실시간 데이터 스트리밍 경험
사용한 방식: WebSocket 기반 실시간 통신 (socket.io)
채팅 기능 구현을 위해 socket.io를 사용.

클라이언트는 서버에 연결 후 이벤트(chat message)를 구독하고, 서버는 수신한 메시지를 다른 클라이언트로 즉시 브로드캐스팅.

🛠️ 느낀 한계
지연(Latency) 문제
메시지가 많아지거나 서버에 부하가 걸릴 때, 메시지 수신이 눈에 띄게 느려짐.

WebSocket 연결을 강제하지 않으면 초기에 HTTP polling으로 연결되며 불필요한 지연 발생.

처리 안정성(Reliability) 문제
네트워크 불안정으로 인해 연결이 끊기는 경우, 메시지가 유실되거나 중복 수신되는 문제가 발생.

단순 송신만 구현할 경우, 수신 여부를 알 수 없어 신뢰성 저하.

💡 문제 해결을 위해 적용한 설계
WebSocket 강제 연결: socket.io 초기 연결 설정 시 transports: ['websocket'] 옵션을 사용하여 불필요한 polling 과정을 생략.

Ack(수신 확인) 처리: 메시지 전송 시 서버로부터 ack를 받아, 실패 시 재전송하거나 오류를 핸들링.

자동 재연결 설정: 네트워크 끊김 발생 시 일정 횟수까지 재접속을 시도하도록 설정.

메시지 ID 관리: 수신 메시지에 고유 ID를 부여하여 중복 수신을 필터링.

✅ 적용 효과 (체감한 변화)
네트워크가 일시적으로 불안정해도, 자동 복구 덕분에 사용자 경험이 크게 훼손되지 않음.

수신 확인(Ack)과 중복 처리 덕분에, 메시지 신뢰성이 크게 향상됨.

채팅 응답 속도 개선(지연 최소화)으로 대화 흐름이 자연스러워짐.

