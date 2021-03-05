---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 88a89a17adc7a05e75865121d2133f723e534fcc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960298"
---
# <span data-ttu-id="f35f4-101">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f35f4-101">Remove-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="f35f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f35f4-102">SYNOPSIS</span></span>
<span data-ttu-id="f35f4-103">Usuwa zasady SSL z profilu SSL bramy aplikacji Azure.</span><span class="sxs-lookup"><span data-stu-id="f35f4-103">Removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="f35f4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f35f4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f35f4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f35f4-105">DESCRIPTION</span></span>
<span data-ttu-id="f35f4-106">Polecenie Remove-AzApplicationGatewaySslProfilePolicy usuwa zasady SSL z profilu SSL bramy aplikacji Azure.</span><span class="sxs-lookup"><span data-stu-id="f35f4-106">The Remove-AzApplicationGatewaySslProfilePolicy cmdlet removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="f35f4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f35f4-107">EXAMPLES</span></span>

### <span data-ttu-id="f35f4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f35f4-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> $profile = Remove-AzApplicationGatewaySslProfilePolicy -SslProfile $profile
```

<span data-ttu-id="f35f4-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="f35f4-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="f35f4-110">Drugie polecenie pobiera profil SSL o nazwie Profile01 for $AppGw i zapisuje go w zmiennej $profile danych.</span><span class="sxs-lookup"><span data-stu-id="f35f4-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="f35f4-111">Ostatnie polecenie usuwa zasady ssl profilu ssl przechowywanego w u $profile.</span><span class="sxs-lookup"><span data-stu-id="f35f4-111">The last command removes the ssl policy of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="f35f4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f35f4-112">PARAMETERS</span></span>

### <span data-ttu-id="f35f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f35f4-113">-DefaultProfile</span></span>
<span data-ttu-id="f35f4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f35f4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f35f4-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="f35f4-115">-SslProfile</span></span>
<span data-ttu-id="f35f4-116">Profil SSL aplikacjiGateway</span><span class="sxs-lookup"><span data-stu-id="f35f4-116">The applicationGateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f35f4-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f35f4-117">-Confirm</span></span>
<span data-ttu-id="f35f4-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f35f4-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f35f4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f35f4-119">-WhatIf</span></span>
<span data-ttu-id="f35f4-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f35f4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f35f4-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f35f4-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f35f4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f35f4-122">CommonParameters</span></span>
<span data-ttu-id="f35f4-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f35f4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f35f4-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f35f4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f35f4-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f35f4-125">INPUTS</span></span>

### <span data-ttu-id="f35f4-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f35f4-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="f35f4-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f35f4-127">OUTPUTS</span></span>

### <span data-ttu-id="f35f4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="f35f4-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="f35f4-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f35f4-129">NOTES</span></span>

## <span data-ttu-id="f35f4-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f35f4-130">RELATED LINKS</span></span>

[<span data-ttu-id="f35f4-131">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f35f4-131">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="f35f4-132">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f35f4-132">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="f35f4-133">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f35f4-133">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="f35f4-134">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="f35f4-134">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)