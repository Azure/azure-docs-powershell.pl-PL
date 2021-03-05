---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: c8959d281c5eda7e2dd3f40941f5c727a000c588
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982394"
---
# <span data-ttu-id="e75b3-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e75b3-101">New-AzIpGroup</span></span>

## <span data-ttu-id="e75b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e75b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e75b3-103">Tworzy grupę IpGroup platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e75b3-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="e75b3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e75b3-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e75b3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e75b3-105">DESCRIPTION</span></span>
<span data-ttu-id="e75b3-106">Polecenie **cmdlet New-AzIpGroup** tworzy grupę IpGroup platformy Azure</span><span class="sxs-lookup"><span data-stu-id="e75b3-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="e75b3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e75b3-107">EXAMPLES</span></span>

### <span data-ttu-id="e75b3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e75b3-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="e75b3-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e75b3-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="e75b3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e75b3-110">PARAMETERS</span></span>

### <span data-ttu-id="e75b3-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e75b3-111">-AsJob</span></span>
<span data-ttu-id="e75b3-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e75b3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e75b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e75b3-113">-DefaultProfile</span></span>
<span data-ttu-id="e75b3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e75b3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e75b3-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="e75b3-115">-Force</span></span>
<span data-ttu-id="e75b3-116">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="e75b3-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e75b3-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="e75b3-117">-IpAddress</span></span>
<span data-ttu-id="e75b3-118">IpAddresses zdefiniowane w grupie IpGroup</span><span class="sxs-lookup"><span data-stu-id="e75b3-118">IpAddresses defined in the IpGroup</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e75b3-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e75b3-119">-Location</span></span>
<span data-ttu-id="e75b3-120">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="e75b3-120">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75b3-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e75b3-121">-Name</span></span>
<span data-ttu-id="e75b3-122">Nazwa grupy adresów ip.</span><span class="sxs-lookup"><span data-stu-id="e75b3-122">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75b3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e75b3-123">-ResourceGroupName</span></span>
<span data-ttu-id="e75b3-124">Nazwa grupy zasobów grupy ipgroup.</span><span class="sxs-lookup"><span data-stu-id="e75b3-124">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75b3-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="e75b3-125">-Tag</span></span>
<span data-ttu-id="e75b3-126">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="e75b3-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75b3-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e75b3-127">-Confirm</span></span>
<span data-ttu-id="e75b3-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e75b3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e75b3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e75b3-129">-WhatIf</span></span>
<span data-ttu-id="e75b3-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e75b3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e75b3-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e75b3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e75b3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e75b3-132">CommonParameters</span></span>
<span data-ttu-id="e75b3-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e75b3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e75b3-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e75b3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e75b3-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e75b3-135">INPUTS</span></span>

### <span data-ttu-id="e75b3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e75b3-136">System.String</span></span>

### <span data-ttu-id="e75b3-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e75b3-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="e75b3-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e75b3-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e75b3-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e75b3-139">OUTPUTS</span></span>

### <span data-ttu-id="e75b3-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="e75b3-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="e75b3-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e75b3-141">NOTES</span></span>

## <span data-ttu-id="e75b3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e75b3-142">RELATED LINKS</span></span>
