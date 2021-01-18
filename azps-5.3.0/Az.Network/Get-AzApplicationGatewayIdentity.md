---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2ba4a6c0f625941daf34b6754a3df856b8554075
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499574"
---
# <span data-ttu-id="7b787-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="7b787-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="7b787-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b787-102">SYNOPSIS</span></span>
<span data-ttu-id="7b787-103">Uzyskaj tożsamość przypisaną do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7b787-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="7b787-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b787-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b787-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7b787-105">DESCRIPTION</span></span>
<span data-ttu-id="7b787-106">Polecenie cmdlet **Get-AzApplicationGatewayIdentity** pobiera tożsamość przypisaną bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7b787-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="7b787-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b787-107">EXAMPLES</span></span>

### <span data-ttu-id="7b787-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7b787-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="7b787-109">W tym przykładzie pokazano, jak uzyskać tożsamość bramy aplikacji z bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7b787-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="7b787-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b787-110">PARAMETERS</span></span>

### <span data-ttu-id="7b787-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7b787-111">-ApplicationGateway</span></span>
<span data-ttu-id="7b787-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7b787-112">The applicationGateway</span></span>

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

### <span data-ttu-id="7b787-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b787-113">-DefaultProfile</span></span>
<span data-ttu-id="7b787-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b787-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b787-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b787-115">CommonParameters</span></span>
<span data-ttu-id="7b787-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b787-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b787-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b787-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b787-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b787-118">INPUTS</span></span>

### <span data-ttu-id="7b787-119">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7b787-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7b787-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b787-120">OUTPUTS</span></span>

### <span data-ttu-id="7b787-121">Microsoft. Azure. Commands. Network. models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="7b787-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="7b787-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b787-122">NOTES</span></span>

## <span data-ttu-id="7b787-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b787-123">RELATED LINKS</span></span>
