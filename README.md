# 키친포스

## 퀵 스타트

```sh
cd docker
docker compose -p kitchenpos up -d
```

## 요구 사항

### 상품

- 상품을 등록할 수 있다.
- 상품의 가격이 올바르지 않으면 등록할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 이름이 올바르지 않으면 등록할 수 없다.
    - 상품의 이름에는 비속어가 포함될 수 없다.
- 상품의 가격을 변경할 수 있다.
- 상품의 가격이 올바르지 않으면 변경할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 가격이 변경될 때 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 크면 메뉴가 숨겨진다.
- 상품의 목록을 조회할 수 있다.

### 메뉴 그룹

- 메뉴 그룹을 등록할 수 있다.
- 메뉴 그룹의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴 그룹의 이름은 비워 둘 수 없다.
- 메뉴 그룹의 목록을 조회할 수 있다.

### 메뉴

- 1 개 이상의 등록된 상품으로 메뉴를 등록할 수 있다.
- 상품이 없으면 등록할 수 없다.
- 메뉴에 속한 상품의 수량은 0 이상이어야 한다.
- 메뉴의 가격이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴는 특정 메뉴 그룹에 속해야 한다.
- 메뉴의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 이름에는 비속어가 포함될 수 없다.
- 메뉴의 가격을 변경할 수 있다.
- 메뉴의 가격이 올바르지 않으면 변경할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴를 노출할 수 있다.
- 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 높을 경우 메뉴를 노출할 수 없다.
- 메뉴를 숨길 수 있다.
- 메뉴의 목록을 조회할 수 있다.

### 주문 테이블

- 주문 테이블을 등록할 수 있다.
- 주문 테이블의 이름이 올바르지 않으면 등록할 수 없다.
    - 주문 테이블의 이름은 비워 둘 수 없다.
- 빈 테이블을 해지할 수 있다.
- 빈 테이블로 설정할 수 있다.
- 완료되지 않은 주문이 있는 주문 테이블은 빈 테이블로 설정할 수 없다.
- 방문한 손님 수를 변경할 수 있다.
- 방문한 손님 수가 올바르지 않으면 변경할 수 없다.
    - 방문한 손님 수는 0 이상이어야 한다.
- 빈 테이블은 방문한 손님 수를 변경할 수 없다.
- 주문 테이블의 목록을 조회할 수 있다.

### 주문

- 1개 이상의 등록된 메뉴로 배달 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 포장 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 매장 주문을 등록할 수 있다.
- 주문 유형이 올바르지 않으면 등록할 수 없다.
- 메뉴가 없으면 등록할 수 없다.
- 매장 주문은 주문 항목의 수량이 0 미만일 수 있다.
- 매장 주문을 제외한 주문의 경우 주문 항목의 수량은 0 이상이어야 한다.
- 배달 주소가 올바르지 않으면 배달 주문을 등록할 수 없다.
    - 배달 주소는 비워 둘 수 없다.
- 빈 테이블에는 매장 주문을 등록할 수 없다.
- 숨겨진 메뉴는 주문할 수 없다.
- 주문한 메뉴의 가격은 실제 메뉴 가격과 일치해야 한다.
- 주문을 접수한다.
- 접수 대기 중인 주문만 접수할 수 있다.
- 배달 주문을 접수되면 배달 대행사를 호출한다.
- 주문을 서빙한다.
- 접수된 주문만 서빙할 수 있다.
- 주문을 배달한다.
- 배달 주문만 배달할 수 있다.
- 서빙된 주문만 배달할 수 있다.
- 주문을 배달 완료한다.
- 배달 중인 주문만 배달 완료할 수 있다.
- 주문을 완료한다.
- 배달 주문의 경우 배달 완료된 주문만 완료할 수 있다.
- 포장 및 매장 주문의 경우 서빙된 주문만 완료할 수 있다.
- 주문 테이블의 모든 매장 주문이 완료되면 빈 테이블로 설정한다.
- 완료되지 않은 매장 주문이 있는 주문 테이블은 빈 테이블로 설정하지 않는다.
- 주문 목록을 조회할 수 있다.

## 용어 사전

## 용어 사전

### 상품
| 한글명         | 영문명            | 설명                                                                      |
|-------------|----------------|-------------------------------------------------------------------------|
| 상품          | product        | 상품의 가격, 이름, 상태 등 정보가 한 곳에 모여 상품을 의미함                                    |
| 상품 가격       | product price  | 상품의 가격                                                                  |
| 상품 이름       | product name   | 상품의 이름                                                                  |
| 상품 목록       | product list   | 상품이 한 개가 아닌 여러개가 모인 것                                                   |
| 상품 상태       | product status | 상품이 노출/숨김 상태를 의미                                                        |

### 메뉴 그룹
| 한글명         | 영문명             | 설명                                                                      |
|-------------|-----------------|-------------------------------------------------------------------------|
| 메뉴 그룹       | menu group      | 여러개의 메뉴를 나눠 어느 곳에 모아둔 것                                                 |
| 메뉴 그룹 이름    | menu group name | 메뉴 그룹의 이름                                                               |
| 메뉴 그룹 목록    | menu group list | 메뉴 그룹이 한 개가 아닌 여러개가 모인 것                                                |

### 메뉴
| 한글명         | 영문명                      | 설명                                                                      |
|-------------|--------------------------|-------------------------------------------------------------------------|
| 메뉴          | menu                     | 메뉴의 이름, 가격, 상태 등 정보가 한 곳에 모여 메뉴를 의미함                                    |
| 메뉴 이름       | menu name                | 메뉴의 이름                                                                  |
| 메뉴 가격       | menu price               | 메뉴의 가격                                                                  |
| 메뉴 목록  | menu list                | 메뉴 한 개가 아닌 여러개가 모인 것                                                    |
| 메뉴 상태       | menu status              | 메뉴가 노출/숨김 상태를 의미                                                        |
| 메뉴 상품       | menu product             | 메뉴에 등록된 상품 목록이 들어있는 것                                                   |
| 메뉴 상품 목록    | menu product list        | 메뉴 상품이 한 개가 아닌 여러개가 모인 것                                                |
| 메뉴 상품 수량    | menu product quantity    | 메뉴에 속한 상품의 수량을 의미                                                       |
| 메뉴 상품 총 가격  | menu product total price | 메뉴에 속한 상품이 수량을 포함해 총 가격을 산출                                             |

### 주문 테이블
| 한글명         | 영문명                     | 설명                                                                      |
|-------------|-------------------------|-------------------------------------------------------------------------|
| 주문 테이블      | order table             | 주문 테이블의 이름, 손님 수, 상태 등 정보가 한 곳에 모여 주문 테이블을 의미함                          |
| 주문 테이블 목록   | order table list        | 주문 테이블 한 개가 아닌 여러개가 모인 것                                                |
| 주문 테이블 이름   | order table name        | 주문 테이블의 이름                                                              |
| 주문 테이블 인원   | order table guest count | 주문 테이블에 앉아 있는 손님의 수                                                     |
| 주문 테이블 상태   | order table status      | 주문 테이블의 상태에 따라 손님을 응대 할 수 있음 (빈 테이블, 이용중인 테이블)                          |

### 주문
| 한글명        | 영문명                    | 설명                                                                     |
|------------|------------------------|------------------------------------------------------------------------|
| 주문    | order                  | 주문의 유형, 상태, 가격, 주소 등 정보가 한 곳에 모여있는 것을 의미함                              |
| 주문 메뉴 가격   | order menu price       | 손님이 주문한 메뉴의 가격                                                         |
| 주문 메뉴 총 가격 | order menu total price | 손님이 주문한 메뉴의 총 가격                                                       |
| 주문 유형      | order type             | 손님이 주문 유형을 선택할 수 있음.<br/>배달(DELIVERY), 포장(TAKEOUT), 매장내주문(EAT_IN)           |
| 주문 상태      | order status           | 손님이 주문한 상품을 접수부터 완료까지 상태를 표출함<br/>(접수 대기, 접수, 서빙, 배달, 배달 완료, 완료, 매장, 포장)<br/>WAITING, ACCEPTED, SERVED, DELIVERING, DELIVERED, COMPLETED |
| 배달 주소      | delivery address       | 배달 주문 요청으로 손님의 주소지를 의미                                                 |
| 배달 대행사     | delivery agency        | 메뉴를 손님에게 전달해주는 역할                                                      |
| 배달 대행 호출   | call delivery agency                  | 배달 대행사를 호출                                                             |

## 모델링
