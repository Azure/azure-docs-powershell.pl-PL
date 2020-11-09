---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: 9ac7885cc81744914599308c20bf3350642fc967
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319219"
---
# <span data-ttu-id="dcdc9-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="dcdc9-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="dcdc9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dcdc9-102">SYNOPSIS</span></span>
<span data-ttu-id="dcdc9-103">Utwórz witrynę połączoną z sieciowym urządzeniem wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="dcdc9-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="dcdc9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dcdc9-104">SYNTAX</span></span>

### <span data-ttu-id="dcdc9-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dcdc9-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcdc9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcdc9-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcdc9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dcdc9-107">DESCRIPTION</span></span>
<span data-ttu-id="dcdc9-108">Polecenie New-AzVirtualApplianceSite służy do tworzenia witryny urządzenia wirtualnego połączonej z zasobem sieciowego urządzenia wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="dcdc9-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="dcdc9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dcdc9-109">EXAMPLES</span></span>

### <span data-ttu-id="dcdc9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dcdc9-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="dcdc9-111">Utwórz nową witrynę urządzenia wirtualnego w grupie zasób: testrg.</span><span class="sxs-lookup"><span data-stu-id="dcdc9-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="dcdc9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dcdc9-112">PARAMETERS</span></span>

### <span data-ttu-id="dcdc9-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="dcdc9-113">-AddressPrefix</span></span>
<span data-ttu-id="dcdc9-114">Prefiks adresu witryny.</span><span class="sxs-lookup"><span data-stu-id="dcdc9-114">The address prefix for the site.</span></span>

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

### <span data-ttu-id="dcdc9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcdc9-115">-AsJob</span></span>
<span data-ttu-id="dcdc9-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="dcdc9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcdc9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcdc9-117">-DefaultProfile</span></span>
<span data-ttu-id="dcdc9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dcdc9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcdc9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="dcdc9-119">-Force</span></span>
<span data-ttu-id="dcdc9-120">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="dcdc9-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="dcdc9-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dcdc9-121">-Name</span></span>
<span data-ttu-id="dcdc9-122">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="dcdc9-122">The resource name.</span></span>

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

### <span data-ttu-id="dcdc9-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="dcdc9-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="dcdc9-124">Sieciowy urządzenie wirtualne, do którego dołączona jest ta witryna.</span><span class="sxs-lookup"><span data-stu-id="dcdc9-124">The Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="dcdc9-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="dcdc9-125">-O365Policy</span></span>
<span data-ttu-id="dcdc9-126">Zasady podgrupa pakietu Office 365.</span><span class="sxs-lookup"><span data-stu-id="dcdc9-126">The Office 365 breakout policy.</span></span>

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

### <span data-ttu-id="dcdc9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcdc9-127">-ResourceGroupName</span></span>
<span data-ttu-id="dcdc9-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dcdc9-128">The resource group name.</span></span>

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

### <span data-ttu-id="dcdc9-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcdc9-129">-ResourceId</span></span>
<span data-ttu-id="dcdc9-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="dcdc9-130">The resource id.</span></span>

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

### <span data-ttu-id="dcdc9-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="dcdc9-131">-Tag</span></span>
<span data-ttu-id="dcdc9-132">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="dcdc9-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="dcdc9-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dcdc9-133">-Confirm</span></span>
<span data-ttu-id="dcdc9-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcdc9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcdc9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcdc9-135">-WhatIf</span></span>
<span data-ttu-id="dcdc9-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcdc9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcdc9-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dcdc9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcdc9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcdc9-138">CommonParameters</span></span>
<span data-ttu-id="dcdc9-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcdc9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcdc9-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcdc9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcdc9-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcdc9-141">INPUTS</span></span>

### <span data-ttu-id="dcdc9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="dcdc9-142">System.String</span></span>

### <span data-ttu-id="dcdc9-143">Microsoft. Azure. Commands. Network. models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="dcdc9-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="dcdc9-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dcdc9-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dcdc9-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dcdc9-145">OUTPUTS</span></span>

### <span data-ttu-id="dcdc9-146">Microsoft. Azure. Commands. Network. models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="dcdc9-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="dcdc9-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dcdc9-147">NOTES</span></span>

## <span data-ttu-id="dcdc9-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcdc9-148">RELATED LINKS</span></span>
