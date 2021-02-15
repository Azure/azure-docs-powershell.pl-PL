---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189499"
---
# <span data-ttu-id="2ce66-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2ce66-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="2ce66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ce66-102">SYNOPSIS</span></span>
<span data-ttu-id="2ce66-103">Zapisuje zmodyfikowaną zaporę.</span><span class="sxs-lookup"><span data-stu-id="2ce66-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="2ce66-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2ce66-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ce66-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2ce66-105">DESCRIPTION</span></span>
<span data-ttu-id="2ce66-106">Polecenie **cmdlet Set-AzIpGroup** aktualizuje grupę IpGroup platformy Azure</span><span class="sxs-lookup"><span data-stu-id="2ce66-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="2ce66-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2ce66-107">EXAMPLES</span></span>

### <span data-ttu-id="2ce66-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2ce66-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="2ce66-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ce66-109">PARAMETERS</span></span>

### <span data-ttu-id="2ce66-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2ce66-110">-AsJob</span></span>
<span data-ttu-id="2ce66-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2ce66-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ce66-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ce66-112">-DefaultProfile</span></span>
<span data-ttu-id="2ce66-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ce66-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ce66-114">- IpGroup</span><span class="sxs-lookup"><span data-stu-id="2ce66-114">-IpGroup</span></span>
<span data-ttu-id="2ce66-115">Grupa Ip</span><span class="sxs-lookup"><span data-stu-id="2ce66-115">The IpGroup</span></span>

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

### <span data-ttu-id="2ce66-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2ce66-116">-Confirm</span></span>
<span data-ttu-id="2ce66-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2ce66-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ce66-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ce66-118">-WhatIf</span></span>
<span data-ttu-id="2ce66-119">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ce66-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ce66-120">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2ce66-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ce66-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ce66-121">CommonParameters</span></span>
<span data-ttu-id="2ce66-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ce66-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ce66-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ce66-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ce66-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ce66-124">INPUTS</span></span>

### <span data-ttu-id="2ce66-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="2ce66-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="2ce66-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2ce66-126">OUTPUTS</span></span>

### <span data-ttu-id="2ce66-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="2ce66-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="2ce66-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2ce66-128">NOTES</span></span>

## <span data-ttu-id="2ce66-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ce66-129">RELATED LINKS</span></span>
