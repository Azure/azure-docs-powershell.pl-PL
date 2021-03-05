---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 8f8e40f5b2209b75c52376c08b69dff8946add77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976529"
---
# <span data-ttu-id="bd282-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="bd282-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="bd282-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd282-102">SYNOPSIS</span></span>
<span data-ttu-id="bd282-103">Zapisuje zmodyfikowaną zaporę.</span><span class="sxs-lookup"><span data-stu-id="bd282-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="bd282-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bd282-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd282-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bd282-105">DESCRIPTION</span></span>
<span data-ttu-id="bd282-106">Polecenie **cmdlet Set-AzIpGroup** aktualizuje grupę IpGroup platformy Azure</span><span class="sxs-lookup"><span data-stu-id="bd282-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="bd282-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bd282-107">EXAMPLES</span></span>

### <span data-ttu-id="bd282-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bd282-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="bd282-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd282-109">PARAMETERS</span></span>

### <span data-ttu-id="bd282-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="bd282-110">-AsJob</span></span>
<span data-ttu-id="bd282-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bd282-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd282-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd282-112">-DefaultProfile</span></span>
<span data-ttu-id="bd282-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd282-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd282-114">- IpGroup</span><span class="sxs-lookup"><span data-stu-id="bd282-114">-IpGroup</span></span>
<span data-ttu-id="bd282-115">Grupa Ip</span><span class="sxs-lookup"><span data-stu-id="bd282-115">The IpGroup</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd282-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd282-116">-Confirm</span></span>
<span data-ttu-id="bd282-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bd282-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd282-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd282-118">-WhatIf</span></span>
<span data-ttu-id="bd282-119">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd282-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd282-120">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bd282-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd282-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd282-121">CommonParameters</span></span>
<span data-ttu-id="bd282-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd282-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd282-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd282-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd282-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd282-124">INPUTS</span></span>

### <span data-ttu-id="bd282-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="bd282-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="bd282-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd282-126">OUTPUTS</span></span>

### <span data-ttu-id="bd282-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="bd282-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="bd282-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bd282-128">NOTES</span></span>

## <span data-ttu-id="bd282-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd282-129">RELATED LINKS</span></span>
