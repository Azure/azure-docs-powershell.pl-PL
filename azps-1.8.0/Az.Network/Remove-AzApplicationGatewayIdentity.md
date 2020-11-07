---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 22ace3fb8c2b6b8f620a90cc2f53533ba4a42ff5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709175"
---
# <span data-ttu-id="c63a8-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="c63a8-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="c63a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c63a8-102">SYNOPSIS</span></span>
<span data-ttu-id="c63a8-103">Usuwa tożsamość z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c63a8-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="c63a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c63a8-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c63a8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c63a8-105">DESCRIPTION</span></span>
<span data-ttu-id="c63a8-106">Polecenie cmdlet **Remove-AzApplicationGatewayIdentity** usuwa tożsamość z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c63a8-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="c63a8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c63a8-107">EXAMPLES</span></span>

### <span data-ttu-id="c63a8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c63a8-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="c63a8-109">W tym przykładzie usuniesz tożsamość z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c63a8-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="c63a8-110">Uwaga: Jeśli Brama odwołuje się do klucza tajnego magazynu kluczy, ważne jest również usunięcie tych odwołań do certyfikatów SSL w tej operacji.</span><span class="sxs-lookup"><span data-stu-id="c63a8-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="c63a8-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c63a8-111">PARAMETERS</span></span>

### <span data-ttu-id="c63a8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c63a8-112">-ApplicationGateway</span></span>
<span data-ttu-id="c63a8-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c63a8-113">The applicationGateway</span></span>

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

### <span data-ttu-id="c63a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c63a8-114">-DefaultProfile</span></span>
<span data-ttu-id="c63a8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c63a8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c63a8-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c63a8-116">-Confirm</span></span>
<span data-ttu-id="c63a8-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c63a8-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c63a8-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c63a8-118">-WhatIf</span></span>
<span data-ttu-id="c63a8-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c63a8-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c63a8-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c63a8-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c63a8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c63a8-121">CommonParameters</span></span>
<span data-ttu-id="c63a8-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c63a8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c63a8-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c63a8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c63a8-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c63a8-124">INPUTS</span></span>

### <span data-ttu-id="c63a8-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c63a8-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c63a8-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c63a8-126">OUTPUTS</span></span>

### <span data-ttu-id="c63a8-127">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c63a8-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c63a8-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c63a8-128">NOTES</span></span>

## <span data-ttu-id="c63a8-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c63a8-129">RELATED LINKS</span></span>