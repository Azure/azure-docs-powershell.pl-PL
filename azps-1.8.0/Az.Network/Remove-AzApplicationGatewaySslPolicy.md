---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 517327ab3af1665d70f3d2f8eff4594d708a2f85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709165"
---
# <span data-ttu-id="e0069-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e0069-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="e0069-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0069-102">SYNOPSIS</span></span>
<span data-ttu-id="e0069-103">Usuwa zasady SSL z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0069-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="e0069-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0069-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0069-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e0069-105">DESCRIPTION</span></span>
<span data-ttu-id="e0069-106">Polecenie cmdlet Remove-AzApplicationGatewaySslPolicy usuwa zasady SSL z bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0069-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="e0069-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0069-107">EXAMPLES</span></span>

### <span data-ttu-id="e0069-108">Przykład 1: usuwanie zasad SSL z bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="e0069-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="e0069-109">To polecenie usuwa zasady SSL z bramy Application Gateway o nazwie ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="e0069-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="e0069-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0069-110">PARAMETERS</span></span>

### <span data-ttu-id="e0069-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e0069-111">-ApplicationGateway</span></span>
<span data-ttu-id="e0069-112">Określa bramę aplikacji, z której to polecenie cmdlet usuwa zasady SSL.</span><span class="sxs-lookup"><span data-stu-id="e0069-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0069-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0069-113">-DefaultProfile</span></span>
<span data-ttu-id="e0069-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0069-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0069-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e0069-115">-Force</span></span>
<span data-ttu-id="e0069-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e0069-116">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0069-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0069-117">-Confirm</span></span>
<span data-ttu-id="e0069-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0069-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0069-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0069-119">-WhatIf</span></span>
<span data-ttu-id="e0069-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0069-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0069-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e0069-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0069-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0069-122">CommonParameters</span></span>
<span data-ttu-id="e0069-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0069-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0069-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0069-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0069-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0069-125">INPUTS</span></span>

### <span data-ttu-id="e0069-126">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e0069-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e0069-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0069-127">OUTPUTS</span></span>

### <span data-ttu-id="e0069-128">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e0069-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e0069-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0069-129">NOTES</span></span>
<span data-ttu-id="e0069-130">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="e0069-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e0069-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0069-131">RELATED LINKS</span></span>

[<span data-ttu-id="e0069-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e0069-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="e0069-133">Nowe — AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e0069-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="e0069-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e0069-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

