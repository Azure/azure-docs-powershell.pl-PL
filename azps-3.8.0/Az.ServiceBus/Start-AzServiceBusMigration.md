---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 0837532c6e708b4ff7d8cbee4f5ad231b4032347
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053271"
---
# <span data-ttu-id="a66d1-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a66d1-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="a66d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a66d1-102">SYNOPSIS</span></span>
<span data-ttu-id="a66d1-103">Tworzy nową konfigurację migracji i rozpoczyna migrację jednostek z obszarów nazw standardowych do Premium</span><span class="sxs-lookup"><span data-stu-id="a66d1-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="a66d1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a66d1-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a66d1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a66d1-105">DESCRIPTION</span></span>
<span data-ttu-id="a66d1-106">Polecenie cmdlet **Start-AzServiceBusMigration** tworzy nową konfigurację migracji i rozpoczyna migrację jednostek z obszarów nazw standardowych do Premium</span><span class="sxs-lookup"><span data-stu-id="a66d1-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="a66d1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a66d1-107">EXAMPLES</span></span>

### <span data-ttu-id="a66d1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a66d1-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="a66d1-109">Tworzy nową konfigurację migracji dla "TestingNamespaceStandardMigration" do obszarów nazw "TestingNamespacePremiumMigration".</span><span class="sxs-lookup"><span data-stu-id="a66d1-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="a66d1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a66d1-110">PARAMETERS</span></span>

### <span data-ttu-id="a66d1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a66d1-111">-AsJob</span></span>
<span data-ttu-id="a66d1-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a66d1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a66d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a66d1-113">-DefaultProfile</span></span>
<span data-ttu-id="a66d1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a66d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a66d1-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a66d1-115">-Name</span></span>
<span data-ttu-id="a66d1-116">Nazwa standardowej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="a66d1-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="a66d1-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="a66d1-117">-PostMigrationName</span></span>
<span data-ttu-id="a66d1-118">Nazwa wpisu po migracji dla standardowej przestrzeni nazw w ramach migracji</span><span class="sxs-lookup"><span data-stu-id="a66d1-118">Post Migration Name for Standard Namespace in Migration</span></span>

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

### <span data-ttu-id="a66d1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a66d1-119">-ResourceGroupName</span></span>
<span data-ttu-id="a66d1-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a66d1-120">Resource Group Name</span></span>

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

### <span data-ttu-id="a66d1-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="a66d1-121">-TargetNameSpace</span></span>
<span data-ttu-id="a66d1-122">Identyfikator ARM dla obszaru nazw Premium</span><span class="sxs-lookup"><span data-stu-id="a66d1-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="a66d1-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a66d1-123">-Confirm</span></span>
<span data-ttu-id="a66d1-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a66d1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a66d1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a66d1-125">-WhatIf</span></span>
<span data-ttu-id="a66d1-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a66d1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a66d1-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a66d1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a66d1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a66d1-128">CommonParameters</span></span>
<span data-ttu-id="a66d1-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a66d1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a66d1-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a66d1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a66d1-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a66d1-131">INPUTS</span></span>

### <span data-ttu-id="a66d1-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a66d1-132">None</span></span>

## <span data-ttu-id="a66d1-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a66d1-133">OUTPUTS</span></span>

### <span data-ttu-id="a66d1-134">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="a66d1-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="a66d1-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a66d1-135">NOTES</span></span>

## <span data-ttu-id="a66d1-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a66d1-136">RELATED LINKS</span></span>
