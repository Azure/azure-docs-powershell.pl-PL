---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 7d4cce44aa76628011b35d6723b1ae34a869a2e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987729"
---
# <span data-ttu-id="6998b-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="6998b-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="6998b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6998b-102">SYNOPSIS</span></span>
<span data-ttu-id="6998b-103">Usuwa tożsamość z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6998b-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="6998b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6998b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6998b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6998b-105">DESCRIPTION</span></span>
<span data-ttu-id="6998b-106">Polecenie cmdlet **Remove-AzApplicationGatewayIdentity** usuwa tożsamość z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6998b-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="6998b-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6998b-107">EXAMPLES</span></span>

### <span data-ttu-id="6998b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6998b-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="6998b-109">W tym przykładzie usuwamy tożsamość z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="6998b-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="6998b-110">Uwaga: Jeśli brama odwołuje się do klucza tajnego, ważne jest również usunięcie tych odwołań do certyfikatów SSL podczas tej operacji.</span><span class="sxs-lookup"><span data-stu-id="6998b-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="6998b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6998b-111">PARAMETERS</span></span>

### <span data-ttu-id="6998b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6998b-112">-ApplicationGateway</span></span>
<span data-ttu-id="6998b-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="6998b-113">The applicationGateway</span></span>

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

### <span data-ttu-id="6998b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6998b-114">-DefaultProfile</span></span>
<span data-ttu-id="6998b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6998b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6998b-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6998b-116">-Confirm</span></span>
<span data-ttu-id="6998b-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6998b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6998b-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6998b-118">-WhatIf</span></span>
<span data-ttu-id="6998b-119">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6998b-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6998b-120">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6998b-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6998b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6998b-121">CommonParameters</span></span>
<span data-ttu-id="6998b-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6998b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6998b-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6998b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6998b-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6998b-124">INPUTS</span></span>

### <span data-ttu-id="6998b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6998b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6998b-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6998b-126">OUTPUTS</span></span>

### <span data-ttu-id="6998b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6998b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6998b-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6998b-128">NOTES</span></span>

## <span data-ttu-id="6998b-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6998b-129">RELATED LINKS</span></span>
