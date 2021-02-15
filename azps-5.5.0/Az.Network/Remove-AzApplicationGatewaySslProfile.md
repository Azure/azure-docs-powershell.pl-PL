---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: ded757d1e81ef5db94157f4676ed91dc11680fd4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202602"
---
# <span data-ttu-id="f6767-101">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f6767-101">Remove-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="f6767-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6767-102">SYNOPSIS</span></span>
<span data-ttu-id="f6767-103">Usuwa profil ssl z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f6767-103">Removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="f6767-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f6767-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfile -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6767-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f6767-105">DESCRIPTION</span></span>
<span data-ttu-id="f6767-106">Polecenie **cmdlet Remove-AzApplicationGatewaySslProfile** usuwa profil ssl z bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f6767-106">The **Remove-AzApplicationGatewaySslProfile** cmdlet removes the ssl profile from an application gateway.</span></span>

## <span data-ttu-id="f6767-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f6767-107">EXAMPLES</span></span>

### <span data-ttu-id="f6767-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f6767-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "SslProfile01"
```

<span data-ttu-id="f6767-109">Pierwsze polecenie otrzymuje bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="f6767-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="f6767-110">Drugie polecenie usuwa profil ssl o nazwie SslProfile01 z bramy aplikacji przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f6767-110">The second command removes the ssl profile named SslProfile01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f6767-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6767-111">PARAMETERS</span></span>

### <span data-ttu-id="f6767-112">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6767-112">-ApplicationGateway</span></span>
<span data-ttu-id="f6767-113">The applicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6767-113">The applicationGateway</span></span>

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

### <span data-ttu-id="f6767-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6767-114">-DefaultProfile</span></span>
<span data-ttu-id="f6767-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6767-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6767-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f6767-116">-Name</span></span>
<span data-ttu-id="f6767-117">Nazwa profilu SSL</span><span class="sxs-lookup"><span data-stu-id="f6767-117">The name of the ssl profile</span></span>

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

### <span data-ttu-id="f6767-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6767-118">CommonParameters</span></span>
<span data-ttu-id="f6767-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6767-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6767-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6767-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6767-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6767-121">INPUTS</span></span>

### <span data-ttu-id="f6767-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6767-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f6767-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6767-123">OUTPUTS</span></span>

### <span data-ttu-id="f6767-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f6767-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f6767-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f6767-125">NOTES</span></span>

## <span data-ttu-id="f6767-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6767-126">RELATED LINKS</span></span>

[<span data-ttu-id="f6767-127">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f6767-127">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="f6767-128">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f6767-128">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="f6767-129">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f6767-129">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="f6767-130">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f6767-130">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)