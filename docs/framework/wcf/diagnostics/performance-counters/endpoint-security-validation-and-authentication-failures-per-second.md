---
title: 终结点：Security Validation and Authentication Failures Per Second（每秒安全验证和身份验证失败次数）
ms.date: 03/30/2017
ms.assetid: 89a70b90-d7e4-4b03-9b84-4dc88ce3d605
ms.openlocfilehash: 43886f79585fb9a63eeb51360cc869365c100a1d
ms.sourcegitcommit: 5fd80619c760fa8c25d33a6f5661247cb65da465
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2018
ms.locfileid: "50744231"
---
# <a name="endpoint-security-validation-and-authentication-failures-per-second"></a>终结点：Security Validation and Authentication Failures Per Second（每秒安全验证和身份验证失败次数）
计数器名称：Security Validation and Authentication Failures Per Second（每秒安全验证和身份验证失败次数）  
  
## <a name="description"></a>描述  
 每当消息由于“Security Calls Not Authorized”（未授权的安全调用次数）计数器中未包括的安全问题而遭到拒绝时，此计数器即会递增。 此类问题包括：  
  
-   无法从消息中读取客户端令牌。  
  
-   客户端令牌身份验证失败（如密码错误）。  
  
-   签名验证失败（如消息已被篡改）。  
  
-   消息与上一条消息重复，这种情况可能在重放攻击过程中发生。  
  
-   已发生解密失败。  
  
-   消息中缺少一些必需元素（如缺少时间戳或加密的数据块）。  
  
-   TLSNEGO/SPNEGO 握手过程中已发生错误。  
  
 此计数器为性能计数器类型[PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649)，使用以下公式计算其值：  
  
 (N1-N0)/((D1-D0)/F)
