---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkProfile.md
ms.openlocfilehash: 370229f44b260367759ca2f51319258627d3d8c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524349"
---
# <span data-ttu-id="ec2c5-101">Set-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ec2c5-101">Set-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="ec2c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec2c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ec2c5-103">Ustawia stan celu dla istniejącego profilu sieciowego</span><span class="sxs-lookup"><span data-stu-id="ec2c5-103">Sets the goal state for an existing network profile</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec2c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec2c5-104">SYNTAX</span></span>

```
Set-AzureRmNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec2c5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ec2c5-105">DESCRIPTION</span></span>
<span data-ttu-id="ec2c5-106">Polecenie cmdlet **Set-AzureRmPublicIpPrefix** ustawia stan celu dla profilu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="ec2c5-106">The **Set-AzureRmPublicIpPrefix** cmdlet sets the goal state for a network profile.</span></span>

## <span data-ttu-id="ec2c5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec2c5-107">EXAMPLES</span></span>

### <span data-ttu-id="ec2c5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ec2c5-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzureRmNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzureRmNetworkProfile
```

<span data-ttu-id="ec2c5-109">Pierwsze polecenie uzyskuje istniejący profil sieciowy.</span><span class="sxs-lookup"><span data-stu-id="ec2c5-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="ec2c5-110">Drugie polecenie aktualizuje tag, a trzeci dodaje konfigurację interfejsu sieciowego w profilu sieciowym.</span><span class="sxs-lookup"><span data-stu-id="ec2c5-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="ec2c5-111">Czwarte polecenie aktualizuje profil sieci.</span><span class="sxs-lookup"><span data-stu-id="ec2c5-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="ec2c5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec2c5-112">PARAMETERS</span></span>

### <span data-ttu-id="ec2c5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec2c5-113">-AsJob</span></span>
<span data-ttu-id="ec2c5-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ec2c5-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec2c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec2c5-115">-DefaultProfile</span></span>
<span data-ttu-id="ec2c5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec2c5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec2c5-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ec2c5-117">-NetworkProfile</span></span>
<span data-ttu-id="ec2c5-118">Profil sieciowy</span><span class="sxs-lookup"><span data-stu-id="ec2c5-118">The network profile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec2c5-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ec2c5-119">-Confirm</span></span>
<span data-ttu-id="ec2c5-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec2c5-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec2c5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec2c5-121">-WhatIf</span></span>
<span data-ttu-id="ec2c5-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec2c5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec2c5-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ec2c5-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec2c5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec2c5-124">CommonParameters</span></span>
<span data-ttu-id="ec2c5-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec2c5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec2c5-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec2c5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec2c5-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec2c5-127">INPUTS</span></span>

### <span data-ttu-id="ec2c5-128">Microsoft. Azure. Commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ec2c5-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="ec2c5-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec2c5-129">OUTPUTS</span></span>

### <span data-ttu-id="ec2c5-130">Microsoft. Azure. Commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ec2c5-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="ec2c5-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec2c5-131">NOTES</span></span>

## <span data-ttu-id="ec2c5-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec2c5-132">RELATED LINKS</span></span>
