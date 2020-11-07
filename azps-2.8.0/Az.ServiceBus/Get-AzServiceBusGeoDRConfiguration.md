---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 2d3d62c7921812e45f514f5811500ccb277cced7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871651"
---
# <span data-ttu-id="0af2b-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="0af2b-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="0af2b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0af2b-102">SYNOPSIS</span></span>
<span data-ttu-id="0af2b-103">Pobiera alias (konfigurację odzyskiwania po awarii) dla podstawowego lub pomocniczego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="0af2b-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="0af2b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0af2b-104">SYNTAX</span></span>

### <span data-ttu-id="0af2b-105">GeoDRPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0af2b-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0af2b-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0af2b-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0af2b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0af2b-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0af2b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0af2b-108">DESCRIPTION</span></span>
<span data-ttu-id="0af2b-109">**AzServiceBusGeoDRConfiguration** pobiera alias (konfigurację odzyskiwania po awarii) dla podstawowego lub pomocniczego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="0af2b-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="0af2b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0af2b-110">EXAMPLES</span></span>

### <span data-ttu-id="0af2b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0af2b-111">Example 1</span></span>
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

<span data-ttu-id="0af2b-112">Pobiera konfigurację aliasu "SampleDRConfigName" dla podstawowego obszaru nazw "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="0af2b-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="0af2b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0af2b-113">PARAMETERS</span></span>

### <span data-ttu-id="0af2b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af2b-114">-DefaultProfile</span></span>
<span data-ttu-id="0af2b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0af2b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0af2b-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0af2b-116">-InputObject</span></span>
<span data-ttu-id="0af2b-117">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="0af2b-117">Namespace Object</span></span>

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

### <span data-ttu-id="0af2b-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0af2b-118">-Name</span></span>
<span data-ttu-id="0af2b-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="0af2b-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="0af2b-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0af2b-120">-Namespace</span></span>
<span data-ttu-id="0af2b-121">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="0af2b-121">Namespace Name</span></span>

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

### <span data-ttu-id="0af2b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0af2b-122">-ResourceGroupName</span></span>
<span data-ttu-id="0af2b-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0af2b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="0af2b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0af2b-124">-ResourceId</span></span>
<span data-ttu-id="0af2b-125">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="0af2b-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="0af2b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af2b-126">CommonParameters</span></span>
<span data-ttu-id="0af2b-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0af2b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af2b-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0af2b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af2b-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0af2b-129">INPUTS</span></span>

### <span data-ttu-id="0af2b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0af2b-130">System.String</span></span>

### <span data-ttu-id="0af2b-131">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="0af2b-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="0af2b-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0af2b-132">OUTPUTS</span></span>

### <span data-ttu-id="0af2b-133">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="0af2b-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="0af2b-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0af2b-134">NOTES</span></span>

## <span data-ttu-id="0af2b-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0af2b-135">RELATED LINKS</span></span>
