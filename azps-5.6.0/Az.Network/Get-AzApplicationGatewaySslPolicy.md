---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 4e15a4296a405a7f0f1e9ac918a5a806603203da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994043"
---
# <span data-ttu-id="c3aab-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c3aab-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c3aab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3aab-102">SYNOPSIS</span></span>
<span data-ttu-id="c3aab-103">Pobiera zasady SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c3aab-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="c3aab-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c3aab-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3aab-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c3aab-105">DESCRIPTION</span></span>
<span data-ttu-id="c3aab-106">Polecenie **cmdlet Get-AzApplicationGatewaySslPolicy** pobiera zasady SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c3aab-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="c3aab-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c3aab-107">EXAMPLES</span></span>

### <span data-ttu-id="c3aab-108">1:</span><span class="sxs-lookup"><span data-stu-id="c3aab-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="c3aab-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 i przechowuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c3aab-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="c3aab-110">Drugie polecenie pobiera zasady ssl z bramy aplikacji przechowywane w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c3aab-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="c3aab-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3aab-111">PARAMETERS</span></span>

### <span data-ttu-id="c3aab-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3aab-112">-ApplicationGateway</span></span>
<span data-ttu-id="c3aab-113">Określa bramę aplikacji zasad SSL, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3aab-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c3aab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3aab-114">-DefaultProfile</span></span>
<span data-ttu-id="c3aab-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3aab-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3aab-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3aab-116">CommonParameters</span></span>
<span data-ttu-id="c3aab-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3aab-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3aab-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3aab-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3aab-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3aab-119">INPUTS</span></span>

### <span data-ttu-id="c3aab-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3aab-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c3aab-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3aab-121">OUTPUTS</span></span>

### <span data-ttu-id="c3aab-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c3aab-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c3aab-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c3aab-123">NOTES</span></span>
* <span data-ttu-id="c3aab-124">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="c3aab-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c3aab-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3aab-125">RELATED LINKS</span></span>

[<span data-ttu-id="c3aab-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c3aab-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="c3aab-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c3aab-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


