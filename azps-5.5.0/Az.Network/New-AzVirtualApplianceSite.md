---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: 9ac7885cc81744914599308c20bf3350642fc967
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193570"
---
# <span data-ttu-id="ffa2a-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="ffa2a-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="ffa2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffa2a-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa2a-103">Tworzenie witryny połączonej z urządzeniem wirtualnym sieci.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="ffa2a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ffa2a-104">SYNTAX</span></span>

### <span data-ttu-id="ffa2a-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ffa2a-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffa2a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffa2a-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffa2a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ffa2a-107">DESCRIPTION</span></span>
<span data-ttu-id="ffa2a-108">Polecenie New-AzVirtualApplianceSite tworzy witrynę Wirtualne urządzenie połączone z zasobem wirtualnego urządzenia network.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="ffa2a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ffa2a-109">EXAMPLES</span></span>

### <span data-ttu-id="ffa2a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ffa2a-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="ffa2a-111">Utwórz nową witrynę Wirtualne urządzenie w grupie zasobów: testrg.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="ffa2a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffa2a-112">PARAMETERS</span></span>

### <span data-ttu-id="ffa2a-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ffa2a-113">-AddressPrefix</span></span>
<span data-ttu-id="ffa2a-114">Prefiks adresu witryny.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-114">The address prefix for the site.</span></span>

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

### <span data-ttu-id="ffa2a-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ffa2a-115">-AsJob</span></span>
<span data-ttu-id="ffa2a-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ffa2a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ffa2a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa2a-117">-DefaultProfile</span></span>
<span data-ttu-id="ffa2a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffa2a-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ffa2a-119">-Force</span></span>
<span data-ttu-id="ffa2a-120">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="ffa2a-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ffa2a-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ffa2a-121">-Name</span></span>
<span data-ttu-id="ffa2a-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa2a-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="ffa2a-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="ffa2a-124">Urządzenie wirtualne Network, do których jest dołączona ta witryna.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-124">The Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="ffa2a-125">—O365Policy</span><span class="sxs-lookup"><span data-stu-id="ffa2a-125">-O365Policy</span></span>
<span data-ttu-id="ffa2a-126">Zasady podziału usługi Office 365.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-126">The Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa2a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa2a-127">-ResourceGroupName</span></span>
<span data-ttu-id="ffa2a-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa2a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffa2a-129">-ResourceId</span></span>
<span data-ttu-id="ffa2a-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-130">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa2a-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="ffa2a-131">-Tag</span></span>
<span data-ttu-id="ffa2a-132">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ffa2a-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ffa2a-133">-Confirm</span></span>
<span data-ttu-id="ffa2a-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa2a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa2a-135">-WhatIf</span></span>
<span data-ttu-id="ffa2a-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffa2a-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa2a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa2a-138">CommonParameters</span></span>
<span data-ttu-id="ffa2a-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffa2a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa2a-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffa2a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa2a-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffa2a-141">INPUTS</span></span>

### <span data-ttu-id="ffa2a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ffa2a-142">System.String</span></span>

### <span data-ttu-id="ffa2a-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="ffa2a-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="ffa2a-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ffa2a-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ffa2a-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffa2a-145">OUTPUTS</span></span>

### <span data-ttu-id="ffa2a-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="ffa2a-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="ffa2a-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ffa2a-147">NOTES</span></span>

## <span data-ttu-id="ffa2a-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffa2a-148">RELATED LINKS</span></span>
