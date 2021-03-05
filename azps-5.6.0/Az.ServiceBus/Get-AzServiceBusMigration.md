---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 29595722be5f7659d63828462ade0826ac85e610
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005633"
---
# <span data-ttu-id="cf078-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="cf078-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="cf078-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf078-102">SYNOPSIS</span></span>
<span data-ttu-id="cf078-103">Pobiera migracjęConfiguration dla przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="cf078-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="cf078-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cf078-104">SYNTAX</span></span>

### <span data-ttu-id="cf078-105">MigrationConfigurationPropertiesSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="cf078-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf078-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cf078-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf078-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf078-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf078-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cf078-108">DESCRIPTION</span></span>
<span data-ttu-id="cf078-109">**Get-AzServiceBusMigration** pobiera konfigurację migracji dla przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="cf078-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="cf078-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cf078-110">EXAMPLES</span></span>

### <span data-ttu-id="cf078-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cf078-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="cf078-112">Pobiera właściwości konfiguracji migracji "TestingNamespaceStandardMigration"</span><span class="sxs-lookup"><span data-stu-id="cf078-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="cf078-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf078-113">PARAMETERS</span></span>

### <span data-ttu-id="cf078-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf078-114">-DefaultProfile</span></span>
<span data-ttu-id="cf078-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf078-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf078-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf078-116">-InputObject</span></span>
<span data-ttu-id="cf078-117">Obiekt Przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="cf078-117">Namespace Object</span></span>

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

### <span data-ttu-id="cf078-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cf078-118">-Name</span></span>
<span data-ttu-id="cf078-119">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="cf078-119">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf078-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf078-120">-ResourceGroupName</span></span>
<span data-ttu-id="cf078-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cf078-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf078-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf078-122">-ResourceId</span></span>
<span data-ttu-id="cf078-123">Identyfikator zasobu przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="cf078-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="cf078-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf078-124">CommonParameters</span></span>
<span data-ttu-id="cf078-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf078-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf078-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf078-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf078-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf078-127">INPUTS</span></span>

### <span data-ttu-id="cf078-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="cf078-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="cf078-129">System.String</span><span class="sxs-lookup"><span data-stu-id="cf078-129">System.String</span></span>

## <span data-ttu-id="cf078-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf078-130">OUTPUTS</span></span>

### <span data-ttu-id="cf078-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="cf078-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="cf078-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cf078-132">NOTES</span></span>

## <span data-ttu-id="cf078-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf078-133">RELATED LINKS</span></span>
