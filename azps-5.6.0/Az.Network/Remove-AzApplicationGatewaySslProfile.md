---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: ab8afdb01a2993330c75b23b02392ee583cad297
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996465"
---
# <span data-ttu-id="1e6cd-101">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1e6cd-101">Remove-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="1e6cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e6cd-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6cd-103">Usuwa profil ssl z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1e6cd-103">Removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="1e6cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1e6cd-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfile -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e6cd-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1e6cd-105">DESCRIPTION</span></span>
<span data-ttu-id="1e6cd-106">Polecenie **cmdlet Remove-AzApplicationGatewaySslProfile** usuwa profil ssl z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1e6cd-106">The **Remove-AzApplicationGatewaySslProfile** cmdlet removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="1e6cd-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1e6cd-107">EXAMPLES</span></span>

### <span data-ttu-id="1e6cd-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1e6cd-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "SslProfile01"
```

<span data-ttu-id="1e6cd-109">Pierwsze polecenie otrzymuje bramę aplikacji o nazwie ApplicationGateway01 należącą do grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="1e6cd-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="1e6cd-110">Drugie polecenie usuwa profil ssl o nazwie SslProfile01 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1e6cd-110">The second command removes the ssl profile named SslProfile01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="1e6cd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e6cd-111">PARAMETERS</span></span>

### <span data-ttu-id="1e6cd-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e6cd-112">-ApplicationGateway</span></span>
<span data-ttu-id="1e6cd-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e6cd-113">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e6cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6cd-114">-DefaultProfile</span></span>
<span data-ttu-id="1e6cd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e6cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6cd-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1e6cd-116">-Name</span></span>
<span data-ttu-id="1e6cd-117">Nazwa profilu SSL</span><span class="sxs-lookup"><span data-stu-id="1e6cd-117">The name of the ssl profile</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6cd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6cd-118">CommonParameters</span></span>
<span data-ttu-id="1e6cd-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e6cd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6cd-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e6cd-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6cd-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e6cd-121">INPUTS</span></span>

### <span data-ttu-id="1e6cd-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e6cd-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1e6cd-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e6cd-123">OUTPUTS</span></span>

### <span data-ttu-id="1e6cd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e6cd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1e6cd-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1e6cd-125">NOTES</span></span>

## <span data-ttu-id="1e6cd-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e6cd-126">RELATED LINKS</span></span>

[<span data-ttu-id="1e6cd-127">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1e6cd-127">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="1e6cd-128">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1e6cd-128">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="1e6cd-129">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1e6cd-129">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="1e6cd-130">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="1e6cd-130">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)