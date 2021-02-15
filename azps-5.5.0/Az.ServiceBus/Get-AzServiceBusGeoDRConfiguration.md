---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 5a2f3a3310675324fde3ff262cf88325224193c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242250"
---
# <span data-ttu-id="678dd-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="678dd-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="678dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="678dd-102">SYNOPSIS</span></span>
<span data-ttu-id="678dd-103">Pobiera alias(konfiguracja odzyskiwania po awarii) dla podstawowej lub pomocniczej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="678dd-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="678dd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="678dd-104">SYNTAX</span></span>

### <span data-ttu-id="678dd-105">GeoDRPropertiesSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="678dd-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="678dd-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="678dd-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="678dd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="678dd-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="678dd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="678dd-108">DESCRIPTION</span></span>
<span data-ttu-id="678dd-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span><span class="sxs-lookup"><span data-stu-id="678dd-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="678dd-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="678dd-110">EXAMPLES</span></span>

### <span data-ttu-id="678dd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="678dd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="678dd-112">Pobiera konfigurację aliasu "SampleDRConfigName" dla podstawowej przestrzeni nazw "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="678dd-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="678dd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="678dd-113">PARAMETERS</span></span>

### <span data-ttu-id="678dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="678dd-114">-DefaultProfile</span></span>
<span data-ttu-id="678dd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="678dd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="678dd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="678dd-116">-InputObject</span></span>
<span data-ttu-id="678dd-117">Obiekt Przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="678dd-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="678dd-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="678dd-118">-Name</span></span>
<span data-ttu-id="678dd-119">Nazwa konfiguracji dr</span><span class="sxs-lookup"><span data-stu-id="678dd-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="678dd-120">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="678dd-120">-Namespace</span></span>
<span data-ttu-id="678dd-121">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="678dd-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678dd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="678dd-122">-ResourceGroupName</span></span>
<span data-ttu-id="678dd-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="678dd-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678dd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="678dd-124">-ResourceId</span></span>
<span data-ttu-id="678dd-125">Identyfikator zasobu przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="678dd-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="678dd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678dd-126">CommonParameters</span></span>
<span data-ttu-id="678dd-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="678dd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678dd-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="678dd-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678dd-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="678dd-129">INPUTS</span></span>

### <span data-ttu-id="678dd-130">System.String</span><span class="sxs-lookup"><span data-stu-id="678dd-130">System.String</span></span>

### <span data-ttu-id="678dd-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="678dd-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="678dd-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="678dd-132">OUTPUTS</span></span>

### <span data-ttu-id="678dd-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="678dd-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="678dd-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="678dd-134">NOTES</span></span>

## <span data-ttu-id="678dd-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="678dd-135">RELATED LINKS</span></span>
