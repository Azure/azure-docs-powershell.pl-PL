---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 105097f30ea87637cd0ad4bd16e0b8da922c2f4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001169"
---
# <span data-ttu-id="36682-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="36682-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="36682-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36682-102">SYNOPSIS</span></span>
<span data-ttu-id="36682-103">Uzyskaj tożsamość przypisaną do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36682-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="36682-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="36682-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36682-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="36682-105">DESCRIPTION</span></span>
<span data-ttu-id="36682-106">Polecenie **cmdlet Get-AzApplicationGatewayIdentity** pobiera tożsamość przypisaną do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36682-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="36682-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="36682-107">EXAMPLES</span></span>

### <span data-ttu-id="36682-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="36682-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="36682-109">W tych przykładach pokazano, jak pobrać tożsamość bramy aplikacji z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="36682-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="36682-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36682-110">PARAMETERS</span></span>

### <span data-ttu-id="36682-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36682-111">-ApplicationGateway</span></span>
<span data-ttu-id="36682-112">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="36682-112">The applicationGateway</span></span>

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

### <span data-ttu-id="36682-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36682-113">-DefaultProfile</span></span>
<span data-ttu-id="36682-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="36682-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36682-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36682-115">CommonParameters</span></span>
<span data-ttu-id="36682-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36682-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36682-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36682-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36682-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36682-118">INPUTS</span></span>

### <span data-ttu-id="36682-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36682-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="36682-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36682-120">OUTPUTS</span></span>

### <span data-ttu-id="36682-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="36682-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="36682-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="36682-122">NOTES</span></span>

## <span data-ttu-id="36682-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36682-123">RELATED LINKS</span></span>
