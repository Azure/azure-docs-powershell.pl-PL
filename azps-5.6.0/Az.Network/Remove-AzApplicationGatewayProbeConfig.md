---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 8ee58ee3f6c7a92fac0cb3c92f0a45966e4e875e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991012"
---
# <span data-ttu-id="13fff-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="13fff-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="13fff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13fff-102">SYNOPSIS</span></span>
<span data-ttu-id="13fff-103">Usuwa kondycję z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="13fff-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="13fff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="13fff-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13fff-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="13fff-105">DESCRIPTION</span></span>
<span data-ttu-id="13fff-106">Polecenie Remove-AzApplicationGatewayProbeConfig usuwa element cieplny z istniejącej bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="13fff-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="13fff-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="13fff-107">EXAMPLES</span></span>

### <span data-ttu-id="13fff-108">Przykład 1. Usuwanie pliku kondycji z istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="13fff-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="13fff-109">To polecenie usuwa z bramy aplikacji o nazwie Brama kondycję o nazwie Pochłoń04.</span><span class="sxs-lookup"><span data-stu-id="13fff-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="13fff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13fff-110">PARAMETERS</span></span>

### <span data-ttu-id="13fff-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13fff-111">-ApplicationGateway</span></span>
<span data-ttu-id="13fff-112">Określa bramę aplikacji, do której to polecenie cmdlet spowoduje usunięcie agonii.</span><span class="sxs-lookup"><span data-stu-id="13fff-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="13fff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13fff-113">-DefaultProfile</span></span>
<span data-ttu-id="13fff-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="13fff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13fff-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="13fff-115">-Name</span></span>
<span data-ttu-id="13fff-116">Określa nazwę pliku cmdlet, którego to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="13fff-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13fff-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13fff-117">CommonParameters</span></span>
<span data-ttu-id="13fff-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13fff-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13fff-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13fff-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13fff-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13fff-120">INPUTS</span></span>

### <span data-ttu-id="13fff-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13fff-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="13fff-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13fff-122">OUTPUTS</span></span>

### <span data-ttu-id="13fff-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13fff-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="13fff-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="13fff-124">NOTES</span></span>

## <span data-ttu-id="13fff-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13fff-125">RELATED LINKS</span></span>

[<span data-ttu-id="13fff-126">Usuwanie pliku z istniejącej bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="13fff-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="13fff-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="13fff-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="13fff-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="13fff-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="13fff-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="13fff-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="13fff-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="13fff-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

