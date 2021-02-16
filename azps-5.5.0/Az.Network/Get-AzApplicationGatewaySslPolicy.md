---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3e7e9559761bce69473511fbd6cdb94d635e13c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192002"
---
# <span data-ttu-id="78392-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="78392-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="78392-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78392-102">SYNOPSIS</span></span>
<span data-ttu-id="78392-103">Pobiera zasady SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="78392-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="78392-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="78392-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78392-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="78392-105">DESCRIPTION</span></span>
<span data-ttu-id="78392-106">Polecenie **cmdlet Get-AzApplicationGatewaySslPolicy** pobiera zasady SSL bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="78392-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="78392-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="78392-107">EXAMPLES</span></span>

### <span data-ttu-id="78392-108">1:</span><span class="sxs-lookup"><span data-stu-id="78392-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="78392-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="78392-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="78392-110">Drugie polecenie pobiera zasady ssl z bramy aplikacji przechowywane w zmiennej o nazwie $AppGW.</span><span class="sxs-lookup"><span data-stu-id="78392-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="78392-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78392-111">PARAMETERS</span></span>

### <span data-ttu-id="78392-112">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="78392-112">-ApplicationGateway</span></span>
<span data-ttu-id="78392-113">Określa bramę aplikacji zasad SSL, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78392-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="78392-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78392-114">-DefaultProfile</span></span>
<span data-ttu-id="78392-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="78392-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78392-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78392-116">CommonParameters</span></span>
<span data-ttu-id="78392-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78392-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78392-118">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78392-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78392-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78392-119">INPUTS</span></span>

### <span data-ttu-id="78392-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="78392-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="78392-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78392-121">OUTPUTS</span></span>

### <span data-ttu-id="78392-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="78392-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="78392-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="78392-123">NOTES</span></span>
* <span data-ttu-id="78392-124">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="78392-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="78392-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78392-125">RELATED LINKS</span></span>

[<span data-ttu-id="78392-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="78392-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="78392-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="78392-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


