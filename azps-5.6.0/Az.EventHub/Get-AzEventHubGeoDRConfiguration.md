---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: b2003821178875777240cb43bcdc1e9e53784fc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957249"
---
# <span data-ttu-id="7384a-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="7384a-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="7384a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7384a-102">SYNOPSIS</span></span>
<span data-ttu-id="7384a-103">Pobiera alias(konfiguracja odzyskiwania po awarii) dla podstawowej lub pomocniczej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="7384a-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="7384a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7384a-104">SYNTAX</span></span>

### <span data-ttu-id="7384a-105">GeoDRParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7384a-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7384a-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7384a-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7384a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7384a-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7384a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7384a-108">DESCRIPTION</span></span>
<span data-ttu-id="7384a-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span><span class="sxs-lookup"><span data-stu-id="7384a-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="7384a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7384a-110">EXAMPLES</span></span>

### <span data-ttu-id="7384a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7384a-111">Example 1</span></span>
```
PS C:\> Get-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="7384a-112">Pobiera konfigurację aliasu "SampleDRConfigName" dla podstawowej przestrzeni nazw "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="7384a-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="7384a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7384a-113">PARAMETERS</span></span>

### <span data-ttu-id="7384a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7384a-114">-DefaultProfile</span></span>
<span data-ttu-id="7384a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7384a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7384a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7384a-116">-InputObject</span></span>
<span data-ttu-id="7384a-117">Obiekt Przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="7384a-117">Namespace Object</span></span>

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

### <span data-ttu-id="7384a-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7384a-118">-Name</span></span>
<span data-ttu-id="7384a-119">Nazwa konfiguracji dr</span><span class="sxs-lookup"><span data-stu-id="7384a-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="7384a-120">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="7384a-120">-Namespace</span></span>
<span data-ttu-id="7384a-121">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="7384a-121">Namespace Name</span></span>

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

### <span data-ttu-id="7384a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7384a-122">-ResourceGroupName</span></span>
<span data-ttu-id="7384a-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7384a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="7384a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7384a-124">-ResourceId</span></span>
<span data-ttu-id="7384a-125">Identyfikator zasobu przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="7384a-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7384a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7384a-126">CommonParameters</span></span>
<span data-ttu-id="7384a-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7384a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7384a-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7384a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7384a-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7384a-129">INPUTS</span></span>

### <span data-ttu-id="7384a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7384a-130">System.String</span></span>

### <span data-ttu-id="7384a-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="7384a-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="7384a-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7384a-132">OUTPUTS</span></span>

### <span data-ttu-id="7384a-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="7384a-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="7384a-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7384a-134">NOTES</span></span>

## <span data-ttu-id="7384a-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7384a-135">RELATED LINKS</span></span>
