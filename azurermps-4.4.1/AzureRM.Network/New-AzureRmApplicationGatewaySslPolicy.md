---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: dc6dc0c201ebb8298805064e06af5bb6c63ceda8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544692"
---
# <span data-ttu-id="08eec-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="08eec-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="08eec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08eec-102">SYNOPSIS</span></span>
<span data-ttu-id="08eec-103">Tworzy zasady SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="08eec-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08eec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08eec-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08eec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="08eec-105">DESCRIPTION</span></span>
<span data-ttu-id="08eec-106">Polecenie cmdlet **New-AzureRmApplicationGatewaySslPolicy** tworzy zasady SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="08eec-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="08eec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08eec-107">EXAMPLES</span></span>

### <span data-ttu-id="08eec-108">1:1</span><span class="sxs-lookup"><span data-stu-id="08eec-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="08eec-109">To polecenie tworzy zasadę niestandardową.</span><span class="sxs-lookup"><span data-stu-id="08eec-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="08eec-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08eec-110">PARAMETERS</span></span>

### <span data-ttu-id="08eec-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="08eec-111">-CipherSuite</span></span>
<span data-ttu-id="08eec-112">Mechanizmy szyfrowania SSL są włączone w określonej kolejności dla bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="08eec-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08eec-113">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="08eec-113">-DisabledSslProtocols</span></span>
<span data-ttu-id="08eec-114">Określa, które protokoły są wyłączone.</span><span class="sxs-lookup"><span data-stu-id="08eec-114">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="08eec-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="08eec-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="08eec-116">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="08eec-116">TLSv1_0</span></span> 
- <span data-ttu-id="08eec-117">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="08eec-117">TLSv1_1</span></span> 
- <span data-ttu-id="08eec-118">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="08eec-118">TLSv1_2</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08eec-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="08eec-119">-MinProtocolVersion</span></span>
<span data-ttu-id="08eec-120">Minimalna wersja protokołu SSL, która ma być obsługiwana w bramie aplikacji</span><span class="sxs-lookup"><span data-stu-id="08eec-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08eec-121">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="08eec-121">-PolicyName</span></span>
<span data-ttu-id="08eec-122">Nazwa wstępnie zdefiniowanych zasad SSL</span><span class="sxs-lookup"><span data-stu-id="08eec-122">Name of Ssl predefined policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08eec-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="08eec-123">-PolicyType</span></span>
<span data-ttu-id="08eec-124">Typ zasad SSL</span><span class="sxs-lookup"><span data-stu-id="08eec-124">Type of Ssl Policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08eec-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08eec-125">-Confirm</span></span>
<span data-ttu-id="08eec-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08eec-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08eec-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08eec-127">-WhatIf</span></span>
<span data-ttu-id="08eec-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08eec-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08eec-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08eec-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08eec-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08eec-130">-DefaultProfile</span></span>
<span data-ttu-id="08eec-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08eec-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08eec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08eec-132">CommonParameters</span></span>
<span data-ttu-id="08eec-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08eec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08eec-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08eec-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08eec-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08eec-135">INPUTS</span></span>

### <span data-ttu-id="08eec-136">System. String</span><span class="sxs-lookup"><span data-stu-id="08eec-136">System.String</span></span>

## <span data-ttu-id="08eec-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08eec-137">OUTPUTS</span></span>

### <span data-ttu-id="08eec-138">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="08eec-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="08eec-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08eec-139">NOTES</span></span>
* <span data-ttu-id="08eec-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="08eec-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="08eec-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08eec-141">RELATED LINKS</span></span>

[<span data-ttu-id="08eec-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="08eec-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="08eec-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="08eec-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


