---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 541293160a1cf9e3d32de5d378c24d1ee4b2705b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500341"
---
# <span data-ttu-id="3d0c0-101">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="3d0c0-101">Remove-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="3d0c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d0c0-102">SYNOPSIS</span></span>
<span data-ttu-id="3d0c0-103">Usuwa zasady SSL z profilu SSL usługi Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3d0c0-103">Removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="3d0c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d0c0-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d0c0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3d0c0-105">DESCRIPTION</span></span>
<span data-ttu-id="3d0c0-106">Polecenie cmdlet Remove-AzApplicationGatewaySslProfilePolicy usuwa zasady SSL z profilu SSL usługi Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3d0c0-106">The Remove-AzApplicationGatewaySslProfilePolicy cmdlet removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="3d0c0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d0c0-107">EXAMPLES</span></span>

### <span data-ttu-id="3d0c0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3d0c0-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> $profile = Remove-AzApplicationGatewaySslProfilePolicy -SslProfile $profile
```

<span data-ttu-id="3d0c0-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3d0c0-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="3d0c0-110">Drugie polecenie pobiera profil SSL o nazwie Profile01 dla $AppGw i zapisuje go w zmiennej $profile.</span><span class="sxs-lookup"><span data-stu-id="3d0c0-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="3d0c0-111">Ostatnie polecenie usuwa zasady SSL profilu SSL przechowywanego w $profile.</span><span class="sxs-lookup"><span data-stu-id="3d0c0-111">The last command removes the ssl policy of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="3d0c0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d0c0-112">PARAMETERS</span></span>

### <span data-ttu-id="3d0c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d0c0-113">-DefaultProfile</span></span>
<span data-ttu-id="3d0c0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d0c0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d0c0-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="3d0c0-115">-SslProfile</span></span>
<span data-ttu-id="3d0c0-116">Profil SSL applicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d0c0-116">The applicationGateway SSL profile</span></span>

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

### <span data-ttu-id="3d0c0-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3d0c0-117">-Confirm</span></span>
<span data-ttu-id="3d0c0-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d0c0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d0c0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d0c0-119">-WhatIf</span></span>
<span data-ttu-id="3d0c0-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d0c0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d0c0-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3d0c0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d0c0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d0c0-122">CommonParameters</span></span>
<span data-ttu-id="3d0c0-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d0c0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d0c0-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d0c0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d0c0-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d0c0-125">INPUTS</span></span>

### <span data-ttu-id="3d0c0-126">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="3d0c0-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="3d0c0-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d0c0-127">OUTPUTS</span></span>

### <span data-ttu-id="3d0c0-128">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="3d0c0-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="3d0c0-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d0c0-129">NOTES</span></span>

## <span data-ttu-id="3d0c0-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d0c0-130">RELATED LINKS</span></span>

[<span data-ttu-id="3d0c0-131">Nowe — AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="3d0c0-131">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="3d0c0-132">Dodaj-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="3d0c0-132">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="3d0c0-133">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="3d0c0-133">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="3d0c0-134">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="3d0c0-134">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)