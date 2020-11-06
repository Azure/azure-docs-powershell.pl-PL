---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 7d3635b33e96052c42ca77384d2f138af5cc0d5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550220"
---
# <span data-ttu-id="2eaa1-101">Get-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="2eaa1-101">Get-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="2eaa1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2eaa1-102">SYNOPSIS</span></span>
<span data-ttu-id="2eaa1-103">Pobiera alias (konfigurację odzyskiwania po awarii) dla podstawowego lub pomocniczego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="2eaa1-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2eaa1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2eaa1-104">SYNTAX</span></span>

### <span data-ttu-id="2eaa1-105">GeoDRPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2eaa1-105">GeoDRPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eaa1-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2eaa1-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eaa1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2eaa1-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eaa1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2eaa1-108">DESCRIPTION</span></span>
<span data-ttu-id="2eaa1-109">**AzureRmServiceBusGeoDRConfiguration** pobiera alias (konfigurację odzyskiwania po awarii) dla podstawowego lub pomocniczego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="2eaa1-109">The **Get-AzureRmServiceBusGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="2eaa1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2eaa1-110">EXAMPLES</span></span>

### <span data-ttu-id="2eaa1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2eaa1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.ServiceBus/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.ServiceBus/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="2eaa1-112">Pobiera konfigurację aliasu "SampleDRCongifName" dla podstawowego obszaru nazw "SampleNamespace_Primary"</span><span class="sxs-lookup"><span data-stu-id="2eaa1-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="2eaa1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2eaa1-113">PARAMETERS</span></span>

### <span data-ttu-id="2eaa1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eaa1-114">-DefaultProfile</span></span>
<span data-ttu-id="2eaa1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2eaa1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eaa1-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2eaa1-116">-InputObject</span></span>
<span data-ttu-id="2eaa1-117">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="2eaa1-117">Namespace Object</span></span>

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

### <span data-ttu-id="2eaa1-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2eaa1-118">-Name</span></span>
<span data-ttu-id="2eaa1-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="2eaa1-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="2eaa1-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2eaa1-120">-Namespace</span></span>
<span data-ttu-id="2eaa1-121">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="2eaa1-121">Namespace Name</span></span>

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

### <span data-ttu-id="2eaa1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eaa1-122">-ResourceGroupName</span></span>
<span data-ttu-id="2eaa1-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2eaa1-123">Resource Group Name</span></span>

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

### <span data-ttu-id="2eaa1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2eaa1-124">-ResourceId</span></span>
<span data-ttu-id="2eaa1-125">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="2eaa1-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="2eaa1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eaa1-126">CommonParameters</span></span>
<span data-ttu-id="2eaa1-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eaa1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eaa1-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eaa1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eaa1-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2eaa1-129">INPUTS</span></span>

### <span data-ttu-id="2eaa1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2eaa1-130">System.String</span></span>

### <span data-ttu-id="2eaa1-131">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2eaa1-131">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="2eaa1-132">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2eaa1-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2eaa1-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2eaa1-133">OUTPUTS</span></span>

### <span data-ttu-id="2eaa1-134">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="2eaa1-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="2eaa1-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2eaa1-135">NOTES</span></span>

## <span data-ttu-id="2eaa1-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2eaa1-136">RELATED LINKS</span></span>
