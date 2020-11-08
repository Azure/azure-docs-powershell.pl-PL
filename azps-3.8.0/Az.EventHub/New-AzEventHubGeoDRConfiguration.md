---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: fe0d8f29650498e895e19e18bcb080107b2dbf35
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050393"
---
# <span data-ttu-id="94ed7-101">New-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="94ed7-101">New-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="94ed7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="94ed7-103">Tworzy nowy alias (Konfiguracja odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="94ed7-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="94ed7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94ed7-104">SYNTAX</span></span>

### <span data-ttu-id="94ed7-105">GeoDRParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="94ed7-105">GeoDRParameterSet (Default)</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94ed7-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="94ed7-106">NamespaceInputObjectSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94ed7-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94ed7-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94ed7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="94ed7-108">DESCRIPTION</span></span>
<span data-ttu-id="94ed7-109">Polecenie cmdlet **New-AzEventHubGeoDRConfiguration** tworzy nowy alias (Konfiguracja odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="94ed7-109">The **New-AzEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="94ed7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94ed7-110">EXAMPLES</span></span>

### <span data-ttu-id="94ed7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="94ed7-111">Example 1</span></span>
```
PS C:\> New-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="94ed7-112">Tworzy alias "SampleDRConfigName" z podstawowym obszarem nazw "SampleNamespace_Primary" z pomocniczym obszarem nazw "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="94ed7-112">Creates an alias "SampleDRConfigName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="94ed7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94ed7-113">PARAMETERS</span></span>

### <span data-ttu-id="94ed7-114">-Symbol alternatywny</span><span class="sxs-lookup"><span data-stu-id="94ed7-114">-AlternateName</span></span>
<span data-ttu-id="94ed7-115">Symbol zastępczy wymagany, gdy nazwa konfiguracji DR jest taka sama jak główna przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="94ed7-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="94ed7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94ed7-116">-AsJob</span></span>
<span data-ttu-id="94ed7-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="94ed7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94ed7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ed7-118">-DefaultProfile</span></span>
<span data-ttu-id="94ed7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94ed7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94ed7-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="94ed7-120">-InputObject</span></span>
<span data-ttu-id="94ed7-121">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="94ed7-121">Namespace Object</span></span>

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

### <span data-ttu-id="94ed7-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="94ed7-122">-Name</span></span>
<span data-ttu-id="94ed7-123">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="94ed7-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="94ed7-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="94ed7-124">-Namespace</span></span>
<span data-ttu-id="94ed7-125">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="94ed7-125">Namespace Name</span></span>

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

### <span data-ttu-id="94ed7-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="94ed7-126">-PartnerNamespace</span></span>
<span data-ttu-id="94ed7-127">PartnerNamespace konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="94ed7-127">DR Configuration PartnerNamespace</span></span>

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

### <span data-ttu-id="94ed7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94ed7-128">-ResourceGroupName</span></span>
<span data-ttu-id="94ed7-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="94ed7-129">Resource Group Name</span></span>

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

### <span data-ttu-id="94ed7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94ed7-130">-ResourceId</span></span>
<span data-ttu-id="94ed7-131">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="94ed7-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="94ed7-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94ed7-132">-Confirm</span></span>
<span data-ttu-id="94ed7-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94ed7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94ed7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94ed7-134">-WhatIf</span></span>
<span data-ttu-id="94ed7-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94ed7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94ed7-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="94ed7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94ed7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ed7-137">CommonParameters</span></span>
<span data-ttu-id="94ed7-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94ed7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ed7-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94ed7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ed7-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94ed7-140">INPUTS</span></span>

### <span data-ttu-id="94ed7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="94ed7-141">System.String</span></span>

### <span data-ttu-id="94ed7-142">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="94ed7-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="94ed7-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94ed7-143">OUTPUTS</span></span>

### <span data-ttu-id="94ed7-144">Microsoft. Azure. Commands. EventHub. modele. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="94ed7-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="94ed7-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94ed7-145">NOTES</span></span>

## <span data-ttu-id="94ed7-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94ed7-146">RELATED LINKS</span></span>
