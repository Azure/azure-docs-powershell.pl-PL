---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/start-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Start-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Start-AzureRmServiceBusMigration.md
ms.openlocfilehash: 979db64fb11b4fffc901d96811b24be5c79f6b63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546472"
---
# <span data-ttu-id="ac8d6-101">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ac8d6-101">Start-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="ac8d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac8d6-102">SYNOPSIS</span></span>
<span data-ttu-id="ac8d6-103">Tworzy nową konfigurację migracji i rozpoczyna migrację jednostek z obszarów nazw standardowych do Premium</span><span class="sxs-lookup"><span data-stu-id="ac8d6-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac8d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac8d6-104">SYNTAX</span></span>

```
Start-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac8d6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ac8d6-105">DESCRIPTION</span></span>
<span data-ttu-id="ac8d6-106">Polecenie cmdlet **Start-AzureRmServiceBusMigration** tworzy nową konfigurację migracji i rozpoczyna migrację jednostek z obszarów nazw standardowych do Premium</span><span class="sxs-lookup"><span data-stu-id="ac8d6-106">The **Start-AzureRmServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="ac8d6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac8d6-107">EXAMPLES</span></span>

### <span data-ttu-id="ac8d6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ac8d6-108">Example 1</span></span>
```powershell
PS C:\> Start-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation -PostMigrationName TestingNamespaceStandardMirgationPostMigration

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="ac8d6-109">Tworzy nową konfigurację migracji dla "TestingNamespaceStandardMirgation" do obszarów nazw "TestingNamespacePremiumMirgation".</span><span class="sxs-lookup"><span data-stu-id="ac8d6-109">Creates a new migration configuration for 'TestingNamespaceStandardMirgation' to 'TestingNamespacePremiumMirgation' namespaces</span></span>

## <span data-ttu-id="ac8d6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac8d6-110">PARAMETERS</span></span>

### <span data-ttu-id="ac8d6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac8d6-111">-AsJob</span></span>
<span data-ttu-id="ac8d6-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ac8d6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac8d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac8d6-113">-DefaultProfile</span></span>
<span data-ttu-id="ac8d6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac8d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac8d6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ac8d6-115">-Name</span></span>
<span data-ttu-id="ac8d6-116">Nazwa standardowej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="ac8d6-116">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8d6-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="ac8d6-117">-PostMigrationName</span></span>
<span data-ttu-id="ac8d6-118">Nazwa wpisu po migracji dla przestrzeni nazw Standrad w migracji</span><span class="sxs-lookup"><span data-stu-id="ac8d6-118">Post Migration Name for Standrad Namespace in Migration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8d6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac8d6-119">-ResourceGroupName</span></span>
<span data-ttu-id="ac8d6-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ac8d6-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8d6-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="ac8d6-121">-TargetNameSpace</span></span>
<span data-ttu-id="ac8d6-122">Identyfikator ARM dla obszaru nazw Premium</span><span class="sxs-lookup"><span data-stu-id="ac8d6-122">Premium Namespace ARM Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8d6-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ac8d6-123">-Confirm</span></span>
<span data-ttu-id="ac8d6-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac8d6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac8d6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac8d6-125">-WhatIf</span></span>
<span data-ttu-id="ac8d6-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac8d6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac8d6-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ac8d6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac8d6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac8d6-128">CommonParameters</span></span>
<span data-ttu-id="ac8d6-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac8d6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac8d6-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac8d6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac8d6-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac8d6-131">INPUTS</span></span>

### <span data-ttu-id="ac8d6-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ac8d6-132">None</span></span>

## <span data-ttu-id="ac8d6-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac8d6-133">OUTPUTS</span></span>

### <span data-ttu-id="ac8d6-134">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ac8d6-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="ac8d6-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac8d6-135">NOTES</span></span>

## <span data-ttu-id="ac8d6-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac8d6-136">RELATED LINKS</span></span>
