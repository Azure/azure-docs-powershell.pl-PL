---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 010e54b21d4abb3068f62e561c002fed6ca734d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988807"
---
# <span data-ttu-id="0a6be-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0a6be-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="0a6be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a6be-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6be-103">Tworzy nową konfigurację migracji i rozpoczyna migrację jednostek z przestrzeni nazw Standard do Premium</span><span class="sxs-lookup"><span data-stu-id="0a6be-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="0a6be-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0a6be-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a6be-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0a6be-105">DESCRIPTION</span></span>
<span data-ttu-id="0a6be-106">Polecenie **cmdlet Start-AzServiceBusMigration** tworzy nową konfigurację migracji i rozpoczyna migrację jednostek z przestrzeni nazw Standard do Premium</span><span class="sxs-lookup"><span data-stu-id="0a6be-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="0a6be-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0a6be-107">EXAMPLES</span></span>

### <span data-ttu-id="0a6be-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0a6be-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="0a6be-109">Tworzy nową konfigurację migracji dla nazw "TestingNamespaceStandardMigration" do przestrzeni nazw "TestingNamespacePremiumMigration"</span><span class="sxs-lookup"><span data-stu-id="0a6be-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="0a6be-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a6be-110">PARAMETERS</span></span>

### <span data-ttu-id="0a6be-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0a6be-111">-AsJob</span></span>
<span data-ttu-id="0a6be-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0a6be-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a6be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6be-113">-DefaultProfile</span></span>
<span data-ttu-id="0a6be-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a6be-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a6be-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0a6be-115">-Name</span></span>
<span data-ttu-id="0a6be-116">Nazwa standardowej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="0a6be-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="0a6be-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="0a6be-117">-PostMigrationName</span></span>
<span data-ttu-id="0a6be-118">Nazwa standardowa przestrzeni nazw po migracji w migracji</span><span class="sxs-lookup"><span data-stu-id="0a6be-118">Post Migration Name for Standard Namespace in Migration</span></span>

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

### <span data-ttu-id="0a6be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a6be-119">-ResourceGroupName</span></span>
<span data-ttu-id="0a6be-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0a6be-120">Resource Group Name</span></span>

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

### <span data-ttu-id="0a6be-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="0a6be-121">-TargetNameSpace</span></span>
<span data-ttu-id="0a6be-122">Identyfikator ARM przestrzeni ARM Premium</span><span class="sxs-lookup"><span data-stu-id="0a6be-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="0a6be-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0a6be-123">-Confirm</span></span>
<span data-ttu-id="0a6be-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0a6be-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a6be-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a6be-125">-WhatIf</span></span>
<span data-ttu-id="0a6be-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a6be-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a6be-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0a6be-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a6be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6be-128">CommonParameters</span></span>
<span data-ttu-id="0a6be-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a6be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6be-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a6be-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6be-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a6be-131">INPUTS</span></span>

### <span data-ttu-id="0a6be-132">Brak</span><span class="sxs-lookup"><span data-stu-id="0a6be-132">None</span></span>

## <span data-ttu-id="0a6be-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a6be-133">OUTPUTS</span></span>

### <span data-ttu-id="0a6be-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="0a6be-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="0a6be-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0a6be-135">NOTES</span></span>

## <span data-ttu-id="0a6be-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a6be-136">RELATED LINKS</span></span>
