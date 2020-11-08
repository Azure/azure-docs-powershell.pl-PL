---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: b4238f5b1492afad7d09ee9c338a346d5f54a5e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063984"
---
# <span data-ttu-id="ef4a3-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef4a3-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="ef4a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4a3-103">Pobiera konfigurację skalowania bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ef4a3-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="ef4a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef4a3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef4a3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ef4a3-105">DESCRIPTION</span></span>
<span data-ttu-id="ef4a3-106">Polecenie cmdlet **Get-AzApplicationGatewayAutoscaleConfiguration umożliwia wyświetlenie** konfiguracji autoskalowania bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ef4a3-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="ef4a3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef4a3-107">EXAMPLES</span></span>

### <span data-ttu-id="ef4a3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ef4a3-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="ef4a3-109">Pierwsze polecenie uzyskuje bramę Application Gateway i zapisuje ją w zmiennej $gw.</span><span class="sxs-lookup"><span data-stu-id="ef4a3-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="ef4a3-110">Drugie polecenie wyodrębnia konfigurację autoskalowania z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ef4a3-110">The second command extracts out the autoscale configuration from the application gateway.</span></span>

## <span data-ttu-id="ef4a3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef4a3-111">PARAMETERS</span></span>

### <span data-ttu-id="ef4a3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef4a3-112">-ApplicationGateway</span></span>
<span data-ttu-id="ef4a3-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef4a3-113">The applicationGateway</span></span>

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

### <span data-ttu-id="ef4a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef4a3-114">-DefaultProfile</span></span>
<span data-ttu-id="ef4a3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef4a3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef4a3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4a3-116">CommonParameters</span></span>
<span data-ttu-id="ef4a3-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef4a3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4a3-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef4a3-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4a3-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef4a3-119">INPUTS</span></span>

### <span data-ttu-id="ef4a3-120">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef4a3-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ef4a3-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef4a3-121">OUTPUTS</span></span>

### <span data-ttu-id="ef4a3-122">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef4a3-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="ef4a3-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef4a3-123">NOTES</span></span>

## <span data-ttu-id="ef4a3-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef4a3-124">RELATED LINKS</span></span>

[<span data-ttu-id="ef4a3-125">Nowe — AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef4a3-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="ef4a3-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef4a3-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="ef4a3-127">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef4a3-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
