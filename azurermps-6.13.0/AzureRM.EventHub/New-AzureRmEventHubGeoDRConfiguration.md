---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: e2ac72ba5d563b4be902d424ad30c19b40bff9d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526182"
---
# <span data-ttu-id="5fb3e-101">New-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="5fb3e-101">New-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="5fb3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5fb3e-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb3e-103">Tworzy nowy alias (Konfiguracja odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="5fb3e-103">Creates an new Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fb3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5fb3e-104">SYNTAX</span></span>

### <span data-ttu-id="5fb3e-105">GeoDRParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5fb3e-105">GeoDRParameterSet (Default)</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fb3e-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5fb3e-106">NamespaceInputObjectSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name] <String>
 [-PartnerNamespace] <String> [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fb3e-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fb3e-107">NamespaceResourceIdParameterSet</span></span>
```
New-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name] <String> [-PartnerNamespace] <String>
 [-AlternateName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fb3e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5fb3e-108">DESCRIPTION</span></span>
<span data-ttu-id="5fb3e-109">Polecenie cmdlet **New-AzureRmEventHubGeoDRConfiguration** tworzy nowy alias (Konfiguracja odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="5fb3e-109">The **New-AzureRmEventHubGeoDRConfiguration** cmdlet Creates a new Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="5fb3e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5fb3e-110">EXAMPLES</span></span>

### <span data-ttu-id="5fb3e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5fb3e-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName" -PartnerNamespace "SampleNamespace_Secondary"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
```

<span data-ttu-id="5fb3e-112">Tworzy alias "SampleDRCongifName" z podstawowym obszarem nazw "SampleNamespace_Primary" z pomocniczym obszarem nazw "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="5fb3e-112">Creates an alias "SampleDRCongifName" with primary namespace "SampleNamespace_Primary" with secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="5fb3e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5fb3e-113">PARAMETERS</span></span>

### <span data-ttu-id="5fb3e-114">-Symbol alternatywny</span><span class="sxs-lookup"><span data-stu-id="5fb3e-114">-AlternateName</span></span>
<span data-ttu-id="5fb3e-115">Symbol zastępczy wymagany, gdy nazwa konfiguracji DR jest taka sama jak główna przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="5fb3e-115">AlternateName required when DR configuration name is same as Primary Namespace</span></span>

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

### <span data-ttu-id="5fb3e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fb3e-116">-AsJob</span></span>
<span data-ttu-id="5fb3e-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5fb3e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5fb3e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fb3e-118">-DefaultProfile</span></span>
<span data-ttu-id="5fb3e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5fb3e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb3e-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5fb3e-120">-InputObject</span></span>
<span data-ttu-id="5fb3e-121">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="5fb3e-121">Namespace Object</span></span>

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

### <span data-ttu-id="5fb3e-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5fb3e-122">-Name</span></span>
<span data-ttu-id="5fb3e-123">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="5fb3e-123">DR Configuration Name</span></span>

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

### <span data-ttu-id="5fb3e-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5fb3e-124">-Namespace</span></span>
<span data-ttu-id="5fb3e-125">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="5fb3e-125">Namespace Name</span></span>

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

### <span data-ttu-id="5fb3e-126">-PartnerNamespace</span><span class="sxs-lookup"><span data-stu-id="5fb3e-126">-PartnerNamespace</span></span>
<span data-ttu-id="5fb3e-127">PartnerNamespace konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="5fb3e-127">DR Configuration PartnerNamespace</span></span>

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

### <span data-ttu-id="5fb3e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fb3e-128">-ResourceGroupName</span></span>
<span data-ttu-id="5fb3e-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5fb3e-129">Resource Group Name</span></span>

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

### <span data-ttu-id="5fb3e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fb3e-130">-ResourceId</span></span>
<span data-ttu-id="5fb3e-131">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="5fb3e-131">Namespace Resource Id</span></span>

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

### <span data-ttu-id="5fb3e-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5fb3e-132">-Confirm</span></span>
<span data-ttu-id="5fb3e-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fb3e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fb3e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fb3e-134">-WhatIf</span></span>
<span data-ttu-id="5fb3e-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fb3e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fb3e-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5fb3e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fb3e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb3e-137">CommonParameters</span></span>
<span data-ttu-id="5fb3e-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fb3e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb3e-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fb3e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb3e-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fb3e-140">INPUTS</span></span>

### <span data-ttu-id="5fb3e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5fb3e-141">System.String</span></span>

### <span data-ttu-id="5fb3e-142">Microsoft. Azure. Commands. EventHub. modele. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5fb3e-142">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="5fb3e-143">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5fb3e-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="5fb3e-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5fb3e-144">OUTPUTS</span></span>

### <span data-ttu-id="5fb3e-145">Microsoft. Azure. Commands. EventHub. modele. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="5fb3e-145">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="5fb3e-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5fb3e-146">NOTES</span></span>

## <span data-ttu-id="5fb3e-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5fb3e-147">RELATED LINKS</span></span>
