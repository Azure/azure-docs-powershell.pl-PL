---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 7d0d292cb7eba6b776371493e9ceb7e19ef17115
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951601"
---
# <span data-ttu-id="5e025-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="5e025-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="5e025-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e025-102">SYNOPSIS</span></span>
<span data-ttu-id="5e025-103">Zmienianie lub modyfikowanie witryny urządzenia wirtualnego połączonego z zasobem wirtualnego urządzenia sieciowego.</span><span class="sxs-lookup"><span data-stu-id="5e025-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="5e025-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5e025-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e025-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5e025-105">DESCRIPTION</span></span>
<span data-ttu-id="5e025-106">Polecenie Update-AzVirtualApplianceSite modyfikuje zasób witryny Wirtualne urządzenie.</span><span class="sxs-lookup"><span data-stu-id="5e025-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="5e025-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5e025-107">EXAMPLES</span></span>

### <span data-ttu-id="5e025-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5e025-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="5e025-109">Zmodyfikuj prefiks adresu zasobu witryny Wirtualne urządzenie.</span><span class="sxs-lookup"><span data-stu-id="5e025-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="5e025-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e025-110">PARAMETERS</span></span>

### <span data-ttu-id="5e025-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="5e025-111">-AddresssPrefix</span></span>
<span data-ttu-id="5e025-112">Prefiks adresu witryny.</span><span class="sxs-lookup"><span data-stu-id="5e025-112">The address prefix for the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e025-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5e025-113">-AsJob</span></span>
<span data-ttu-id="5e025-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5e025-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e025-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e025-115">-DefaultProfile</span></span>
<span data-ttu-id="5e025-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e025-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e025-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="5e025-117">-Force</span></span>
<span data-ttu-id="5e025-118">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="5e025-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5e025-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5e025-119">-Name</span></span>
<span data-ttu-id="5e025-120">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="5e025-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e025-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="5e025-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="5e025-122">Urządzenie sieciowe wirtualne, do których jest dołączona ta witryna.</span><span class="sxs-lookup"><span data-stu-id="5e025-122">Network virtual appliance that this site is attached to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e025-123">—O365Policy</span><span class="sxs-lookup"><span data-stu-id="5e025-123">-O365Policy</span></span>
<span data-ttu-id="5e025-124">Zasady dotyczące przerw w usłudze Office 365.</span><span class="sxs-lookup"><span data-stu-id="5e025-124">Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e025-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e025-125">-ResourceGroupName</span></span>
<span data-ttu-id="5e025-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5e025-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e025-127">— Tag</span><span class="sxs-lookup"><span data-stu-id="5e025-127">-Tag</span></span>
<span data-ttu-id="5e025-128">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="5e025-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e025-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e025-129">-Confirm</span></span>
<span data-ttu-id="5e025-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5e025-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e025-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e025-131">-WhatIf</span></span>
<span data-ttu-id="5e025-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e025-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e025-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5e025-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e025-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e025-134">CommonParameters</span></span>
<span data-ttu-id="5e025-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e025-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e025-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e025-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e025-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e025-137">INPUTS</span></span>

### <span data-ttu-id="5e025-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5e025-138">System.String</span></span>

### <span data-ttu-id="5e025-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="5e025-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="5e025-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5e025-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5e025-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e025-141">OUTPUTS</span></span>

### <span data-ttu-id="5e025-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="5e025-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="5e025-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5e025-143">NOTES</span></span>

## <span data-ttu-id="5e025-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e025-144">RELATED LINKS</span></span>
