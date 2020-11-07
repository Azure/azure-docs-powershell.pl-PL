---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2ba4a6c0f625941daf34b6754a3df856b8554075
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895370"
---
# <span data-ttu-id="f6c28-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="f6c28-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="f6c28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6c28-102">SYNOPSIS</span></span>
<span data-ttu-id="f6c28-103">Uzyskaj tożsamość przypisaną do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f6c28-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="f6c28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6c28-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6c28-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f6c28-105">DESCRIPTION</span></span>
<span data-ttu-id="f6c28-106">Polecenie cmdlet **Get-AzApplicationGatewayIdentity** pobiera tożsamość przypisaną bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f6c28-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="f6c28-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6c28-107">EXAMPLES</span></span>

### <span data-ttu-id="f6c28-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f6c28-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="f6c28-109">W tym przykładzie pokazano, jak uzyskać tożsamość bramy aplikacji z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f6c28-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="f6c28-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6c28-110">PARAMETERS</span></span>

### <span data-ttu-id="f6c28-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6c28-111">-ApplicationGateway</span></span>
<span data-ttu-id="f6c28-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6c28-112">The applicationGateway</span></span>

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

### <span data-ttu-id="f6c28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6c28-113">-DefaultProfile</span></span>
<span data-ttu-id="f6c28-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6c28-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6c28-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6c28-115">CommonParameters</span></span>
<span data-ttu-id="f6c28-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6c28-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6c28-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6c28-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6c28-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6c28-118">INPUTS</span></span>

### <span data-ttu-id="f6c28-119">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6c28-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f6c28-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6c28-120">OUTPUTS</span></span>

### <span data-ttu-id="f6c28-121">Microsoft. Azure. Commands. Network. models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="f6c28-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="f6c28-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6c28-122">NOTES</span></span>

## <span data-ttu-id="f6c28-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6c28-123">RELATED LINKS</span></span>
