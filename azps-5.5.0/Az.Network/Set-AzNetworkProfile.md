---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkProfile.md
ms.openlocfilehash: edbfdcdfc7e02c8bfdb266e1ec7a6b1308c07fa2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186843"
---
# <span data-ttu-id="8b3c1-101">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8b3c1-101">Set-AzNetworkProfile</span></span>

## <span data-ttu-id="8b3c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b3c1-102">SYNOPSIS</span></span>
<span data-ttu-id="8b3c1-103">Aktualizuje profil sieciowy.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-103">Updates a network profile.</span></span>

## <span data-ttu-id="8b3c1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8b3c1-104">SYNTAX</span></span>

```
Set-AzNetworkProfile -NetworkProfile <PSNetworkProfile> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b3c1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8b3c1-105">DESCRIPTION</span></span>
<span data-ttu-id="8b3c1-106">Polecenie **cmdlet Set-AzPublicIpPrefix** aktualizuje profil sieciowy.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-106">The **Set-AzPublicIpPrefix** cmdlet updates a network profile.</span></span>

## <span data-ttu-id="8b3c1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8b3c1-107">EXAMPLES</span></span>

### <span data-ttu-id="8b3c1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b3c1-108">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

$networkProfile.Tags = "TestTag"

$networkProfile.ContainerNetworkInterfaceConfigurations = New-AzNetworkProfileContainerNicConfig -Name cnicconfig1

$networkProfile | Set-AzNetworkProfile
```

<span data-ttu-id="8b3c1-109">Pierwsze polecenie otrzymuje istniejący profil sieciowy.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-109">The first command gets an existing network profile.</span></span> <span data-ttu-id="8b3c1-110">Drugie polecenie aktualizuje tag, a trzecie dodaje konfigurację interfejsu sieciowego w profilu sieciowym.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-110">The second command updates a tag and the third adds a network interface configuration on the network profile.</span></span> <span data-ttu-id="8b3c1-111">Czwarte polecenie aktualizuje profil sieciowy.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-111">The fourth command updates the network profile.</span></span>

## <span data-ttu-id="8b3c1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b3c1-112">PARAMETERS</span></span>

### <span data-ttu-id="8b3c1-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8b3c1-113">-AsJob</span></span>
<span data-ttu-id="8b3c1-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8b3c1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b3c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b3c1-115">-DefaultProfile</span></span>
<span data-ttu-id="8b3c1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b3c1-117">- NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8b3c1-117">-NetworkProfile</span></span>
<span data-ttu-id="8b3c1-118">Profil sieciowy</span><span class="sxs-lookup"><span data-stu-id="8b3c1-118">The network profile</span></span>

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

### <span data-ttu-id="8b3c1-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b3c1-119">-Confirm</span></span>
<span data-ttu-id="8b3c1-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b3c1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b3c1-121">-WhatIf</span></span>
<span data-ttu-id="8b3c1-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b3c1-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b3c1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b3c1-124">CommonParameters</span></span>
<span data-ttu-id="8b3c1-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b3c1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b3c1-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b3c1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b3c1-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b3c1-127">INPUTS</span></span>

### <span data-ttu-id="8b3c1-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8b3c1-128">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="8b3c1-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b3c1-129">OUTPUTS</span></span>

### <span data-ttu-id="8b3c1-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8b3c1-130">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="8b3c1-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8b3c1-131">NOTES</span></span>

## <span data-ttu-id="8b3c1-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b3c1-132">RELATED LINKS</span></span>

[<span data-ttu-id="8b3c1-133">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8b3c1-133">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="8b3c1-134">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8b3c1-134">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="8b3c1-135">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8b3c1-135">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)
