---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 5a2f3a3310675324fde3ff262cf88325224193c6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222932"
---
# <span data-ttu-id="cd5db-101">Get-AzServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd5db-101">Get-AzServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="cd5db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd5db-102">SYNOPSIS</span></span>
<span data-ttu-id="cd5db-103">Pobiera alias (konfigurację odzyskiwania po awarii) dla podstawowego lub pomocniczego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="cd5db-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="cd5db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd5db-104">SYNTAX</span></span>

### <span data-ttu-id="cd5db-105">GeoDRPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cd5db-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd5db-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cd5db-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd5db-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd5db-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd5db-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cd5db-108">DESCRIPTION</span></span>
<span data-ttu-id="cd5db-109">**AzServiceBusGeoDRConfiguration** pobiera alias (konfigurację odzyskiwania po awarii) dla podstawowego lub pomocniczego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="cd5db-109">The **Get-AzServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="cd5db-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd5db-110">EXAMPLES</span></span>

### <span data-ttu-id="cd5db-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd5db-111">Example 1</span></span>
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

<span data-ttu-id="cd5db-112">Pobiera konfigurację aliasu "SampleDRConfigName" dla podstawowego obszaru nazw "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="cd5db-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="cd5db-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd5db-113">PARAMETERS</span></span>

### <span data-ttu-id="cd5db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd5db-114">-DefaultProfile</span></span>
<span data-ttu-id="cd5db-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd5db-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd5db-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cd5db-116">-InputObject</span></span>
<span data-ttu-id="cd5db-117">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="cd5db-117">Namespace Object</span></span>

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

### <span data-ttu-id="cd5db-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd5db-118">-Name</span></span>
<span data-ttu-id="cd5db-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="cd5db-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="cd5db-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cd5db-120">-Namespace</span></span>
<span data-ttu-id="cd5db-121">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="cd5db-121">Namespace Name</span></span>

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

### <span data-ttu-id="cd5db-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd5db-122">-ResourceGroupName</span></span>
<span data-ttu-id="cd5db-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cd5db-123">Resource Group Name</span></span>

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

### <span data-ttu-id="cd5db-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd5db-124">-ResourceId</span></span>
<span data-ttu-id="cd5db-125">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="cd5db-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="cd5db-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd5db-126">CommonParameters</span></span>
<span data-ttu-id="cd5db-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd5db-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd5db-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd5db-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd5db-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd5db-129">INPUTS</span></span>

### <span data-ttu-id="cd5db-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cd5db-130">System.String</span></span>

### <span data-ttu-id="cd5db-131">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="cd5db-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="cd5db-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd5db-132">OUTPUTS</span></span>

### <span data-ttu-id="cd5db-133">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="cd5db-133">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="cd5db-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd5db-134">NOTES</span></span>

## <span data-ttu-id="cd5db-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd5db-135">RELATED LINKS</span></span>
