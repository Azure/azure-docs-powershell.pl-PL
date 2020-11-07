---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: c63940ab03f6d288de3c1b5b0d767182168ed1fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869535"
---
# <span data-ttu-id="7b05f-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7b05f-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="7b05f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b05f-102">SYNOPSIS</span></span>
<span data-ttu-id="7b05f-103">Aktualizuje profil sieciowy.</span><span class="sxs-lookup"><span data-stu-id="7b05f-103">Updates a network profile.</span></span>

## <span data-ttu-id="7b05f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b05f-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b05f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7b05f-105">DESCRIPTION</span></span>
<span data-ttu-id="7b05f-106">Polecenie cmdlet **Set-AzPublicIpPrefix** aktualizuje profil sieciowy.</span><span class="sxs-lookup"><span data-stu-id="7b05f-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="7b05f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b05f-107">EXAMPLES</span></span>

### <span data-ttu-id="7b05f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7b05f-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="7b05f-109">Pierwsze polecenie uzyskuje istniejący profil sieciowy.</span><span class="sxs-lookup"><span data-stu-id="7b05f-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="7b05f-110">Drugie polecenie aktualizuje tag, a trzeci dodaje konfigurację interfejsu sieciowego w profilu sieciowym.</span><span class="sxs-lookup"><span data-stu-id="7b05f-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="7b05f-111">Czwarte polecenie aktualizuje profil sieci.</span><span class="sxs-lookup"><span data-stu-id="7b05f-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="7b05f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b05f-112">PARAMETERS</span></span>

### <span data-ttu-id="7b05f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b05f-113">-AsJob</span></span>
<span data-ttu-id="7b05f-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7b05f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b05f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b05f-115">-DefaultProfile</span></span>
<span data-ttu-id="7b05f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b05f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b05f-117">-NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7b05f-117">-NetworkProfile</span></span>
<span data-ttu-id="7b05f-118">Profil sieciowy</span><span class="sxs-lookup"><span data-stu-id="7b05f-118">The network profile</span></span>

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

### <span data-ttu-id="7b05f-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7b05f-119">-Confirm</span></span>
<span data-ttu-id="7b05f-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b05f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b05f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b05f-121">-WhatIf</span></span>
<span data-ttu-id="7b05f-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b05f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b05f-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7b05f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b05f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b05f-124">CommonParameters</span></span>
<span data-ttu-id="7b05f-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b05f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b05f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b05f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b05f-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b05f-127">INPUTS</span></span>

### <span data-ttu-id="7b05f-128">Microsoft. Azure. Commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7b05f-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="7b05f-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b05f-129">OUTPUTS</span></span>

### <span data-ttu-id="7b05f-130">Microsoft. Azure. Commands. Network. models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7b05f-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="7b05f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b05f-131">NOTES</span></span>

## <span data-ttu-id="7b05f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b05f-132">RELATED LINKS</span></span>

[<span data-ttu-id="7b05f-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7b05f-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="7b05f-134">Nowe — AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7b05f-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="7b05f-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7b05f-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
