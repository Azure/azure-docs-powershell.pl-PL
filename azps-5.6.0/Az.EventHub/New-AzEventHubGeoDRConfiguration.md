---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: d545883f1c4ce51d4e3efce15787a2e0fa144378
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957105"
---
# <span data-ttu-id="c5568-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5568-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="c5568-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5568-102">SYNOPSIS</span></span>
<span data-ttu-id="c5568-103">Tworzy nowy alias(konfiguracja odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="c5568-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="c5568-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c5568-104">SYNTAX</span></span>

### <span data-ttu-id="c5568-105">GeoDRParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c5568-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5568-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c5568-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5568-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5568-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5568-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c5568-108">DESCRIPTION</span></span>
<span data-ttu-id="c5568-109">Polecenie **cmdlet New-AzEventHubGeoDRConfiguration** Tworzy nowy alias(konfiguracja odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="c5568-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="c5568-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c5568-110">EXAMPLES</span></span>

### <span data-ttu-id="c5568-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c5568-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="c5568-112">Tworzy alias "SampleDRConfigName" z podstawową przestrzenią nazw "SampleNamespace_Primary" z pomocniczą przestrzenią nazw "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="c5568-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="c5568-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5568-113">PARAMETERS</span></span>

### <span data-ttu-id="c5568-114">-AlternateName</span><span class="sxs-lookup"><span data-stu-id="c5568-114">-AlternateName</span></span>
<span data-ttu-id="c5568-115">Zmienna nazwa wymagana, gdy nazwa konfiguracji usługi DR jest taka sama jak podstawowa przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="c5568-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="c5568-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c5568-116">-AsJob</span></span>
<span data-ttu-id="c5568-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c5568-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5568-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5568-118">-DefaultProfile</span></span>
<span data-ttu-id="c5568-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5568-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5568-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5568-120">-InputObject</span></span>
<span data-ttu-id="c5568-121">Obiekt Przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="c5568-121">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5568-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c5568-122">-Name</span></span>
<span data-ttu-id="c5568-123">Nazwa konfiguracji dr</span><span class="sxs-lookup"><span data-stu-id="c5568-123">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5568-124">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="c5568-124">-Namespace</span></span>
<span data-ttu-id="c5568-125">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="c5568-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5568-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="c5568-126">-PartnerNamespace</span></span>
<span data-ttu-id="c5568-127">Identyfikator ARM partnerów konfiguracji dr</span><span class="sxs-lookup"><span data-stu-id="c5568-127">DR Configuration PartnerNamespace ARM ID</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5568-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5568-128">-ResourceGroupName</span></span>
<span data-ttu-id="c5568-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c5568-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5568-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5568-130">-ResourceId</span></span>
<span data-ttu-id="c5568-131">Identyfikator zasobu przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="c5568-131">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5568-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c5568-132">-Confirm</span></span>
<span data-ttu-id="c5568-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c5568-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5568-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5568-134">-WhatIf</span></span>
<span data-ttu-id="c5568-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5568-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5568-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c5568-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5568-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5568-137">CommonParameters</span></span>
<span data-ttu-id="c5568-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5568-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5568-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5568-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5568-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5568-140">INPUTS</span></span>

### <span data-ttu-id="c5568-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c5568-141">System.String</span></span>

### <span data-ttu-id="c5568-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c5568-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="c5568-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5568-143">OUTPUTS</span></span>

### <span data-ttu-id="c5568-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c5568-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="c5568-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c5568-145">NOTES</span></span>

## <span data-ttu-id="c5568-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5568-146">RELATED LINKS</span></span>
