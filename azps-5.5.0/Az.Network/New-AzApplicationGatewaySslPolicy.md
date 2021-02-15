---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: cf2f2ef91fa217b1710eeb100f4e3e6c2ce6fb9d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187082"
---
# <span data-ttu-id="3becb-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="3becb-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="3becb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3becb-102">SYNOPSIS</span></span>
<span data-ttu-id="3becb-103">Tworzy zasady SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3becb-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="3becb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3becb-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3becb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3becb-105">DESCRIPTION</span></span>
<span data-ttu-id="3becb-106">Polecenie **cmdlet New-AzApplicationGatewaySslPolicy** tworzy zasady SSL dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3becb-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="3becb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3becb-107">EXAMPLES</span></span>

### <span data-ttu-id="3becb-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3becb-108">Example 1</span></span>
```powershell
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="3becb-109">To polecenie tworzy zasady niestandardowe.</span><span class="sxs-lookup"><span data-stu-id="3becb-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="3becb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3becb-110">PARAMETERS</span></span>

### <span data-ttu-id="3becb-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="3becb-111">-CipherSuite</span></span>
<span data-ttu-id="3becb-112">Pakiety szyfrowania ssl, które mają być włączone w określonej kolejności dla bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="3becb-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3becb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3becb-113">-DefaultProfile</span></span>
<span data-ttu-id="3becb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3becb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3becb-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="3becb-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="3becb-116">Określa, które protokoły są wyłączone.</span><span class="sxs-lookup"><span data-stu-id="3becb-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="3becb-117">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3becb-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3becb-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="3becb-118">TLSv1_0</span></span> 
- <span data-ttu-id="3becb-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="3becb-119">TLSv1_1</span></span> 
- <span data-ttu-id="3becb-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="3becb-120">TLSv1_2</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3becb-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="3becb-121">-MinProtocolVersion</span></span>
<span data-ttu-id="3becb-122">Minimalna wersja protokołu Ssl, która ma być obsługiwana przez bramę aplikacji</span><span class="sxs-lookup"><span data-stu-id="3becb-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="3becb-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="3becb-123">-PolicyName</span></span>
<span data-ttu-id="3becb-124">Nazwa wstępnie zdefiniowanych zasad Ssl</span><span class="sxs-lookup"><span data-stu-id="3becb-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="3becb-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="3becb-125">-PolicyType</span></span>
<span data-ttu-id="3becb-126">Typ zasad SSL</span><span class="sxs-lookup"><span data-stu-id="3becb-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="3becb-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3becb-127">-Confirm</span></span>
<span data-ttu-id="3becb-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3becb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3becb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3becb-129">-WhatIf</span></span>
<span data-ttu-id="3becb-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3becb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3becb-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3becb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3becb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3becb-132">CommonParameters</span></span>
<span data-ttu-id="3becb-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3becb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3becb-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3becb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3becb-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3becb-135">INPUTS</span></span>

### <span data-ttu-id="3becb-136">Brak</span><span class="sxs-lookup"><span data-stu-id="3becb-136">None</span></span>

## <span data-ttu-id="3becb-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3becb-137">OUTPUTS</span></span>

### <span data-ttu-id="3becb-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="3becb-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="3becb-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3becb-139">NOTES</span></span>
* <span data-ttu-id="3becb-140">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="3becb-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="3becb-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3becb-141">RELATED LINKS</span></span>

[<span data-ttu-id="3becb-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="3becb-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="3becb-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="3becb-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


