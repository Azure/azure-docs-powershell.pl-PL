---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 96a170d302d66ed2fa27d2cd7bdb17fc23cefcd3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709609"
---
# <span data-ttu-id="e5d23-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="e5d23-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="e5d23-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5d23-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d23-103">Uzyskaj tożsamość przypisaną do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e5d23-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="e5d23-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5d23-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5d23-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e5d23-105">DESCRIPTION</span></span>
<span data-ttu-id="e5d23-106">Polecenie cmdlet **Get-AzApplicationGatewayIdentity** pobiera tożsamość przypisaną bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e5d23-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="e5d23-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5d23-107">EXAMPLES</span></span>

### <span data-ttu-id="e5d23-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e5d23-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="e5d23-109">W tym przykładzie pokazano, jak uzyskać tożsamość bramy aplikacji z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e5d23-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="e5d23-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5d23-110">PARAMETERS</span></span>

### <span data-ttu-id="e5d23-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5d23-111">-ApplicationGateway</span></span>
<span data-ttu-id="e5d23-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5d23-112">The applicationGateway</span></span>

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

### <span data-ttu-id="e5d23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d23-113">-DefaultProfile</span></span>
<span data-ttu-id="e5d23-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5d23-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5d23-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d23-115">CommonParameters</span></span>
<span data-ttu-id="e5d23-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5d23-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d23-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5d23-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d23-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5d23-118">INPUTS</span></span>

### <span data-ttu-id="e5d23-119">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5d23-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e5d23-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5d23-120">OUTPUTS</span></span>

### <span data-ttu-id="e5d23-121">Microsoft. Azure. Commands. Network. models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="e5d23-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="e5d23-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5d23-122">NOTES</span></span>

## <span data-ttu-id="e5d23-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5d23-123">RELATED LINKS</span></span>
