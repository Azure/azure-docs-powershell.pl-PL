---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 686a2486d6a5e28e0149eb8fbf2387744d545fd0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197867"
---
# <span data-ttu-id="c0ff7-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c0ff7-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="c0ff7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ff7-103">Pobiera migracjęConfiguration dla przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="c0ff7-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="c0ff7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0ff7-104">SYNTAX</span></span>

### <span data-ttu-id="c0ff7-105">MigrationConfigurationPropertiesSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c0ff7-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0ff7-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c0ff7-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0ff7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0ff7-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0ff7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0ff7-108">DESCRIPTION</span></span>
<span data-ttu-id="c0ff7-109">**Get-AzServiceBusMigration** pobiera konfigurację migracji dla przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="c0ff7-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="c0ff7-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0ff7-110">EXAMPLES</span></span>

### <span data-ttu-id="c0ff7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0ff7-111">Example 1</span></span>
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

<span data-ttu-id="c0ff7-112">Pobiera właściwości konfiguracji migracji "TestingNamespaceStandardMigration"</span><span class="sxs-lookup"><span data-stu-id="c0ff7-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="c0ff7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0ff7-113">PARAMETERS</span></span>

### <span data-ttu-id="c0ff7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ff7-114">-DefaultProfile</span></span>
<span data-ttu-id="c0ff7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0ff7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0ff7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0ff7-116">-InputObject</span></span>
<span data-ttu-id="c0ff7-117">Obiekt Przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="c0ff7-117">Namespace Object</span></span>

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

### <span data-ttu-id="c0ff7-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c0ff7-118">-Name</span></span>
<span data-ttu-id="c0ff7-119">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="c0ff7-119">Namespace Name</span></span>

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

### <span data-ttu-id="c0ff7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0ff7-120">-ResourceGroupName</span></span>
<span data-ttu-id="c0ff7-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c0ff7-121">Resource Group Name</span></span>

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

### <span data-ttu-id="c0ff7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0ff7-122">-ResourceId</span></span>
<span data-ttu-id="c0ff7-123">Identyfikator zasobu przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="c0ff7-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="c0ff7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ff7-124">CommonParameters</span></span>
<span data-ttu-id="c0ff7-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0ff7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ff7-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0ff7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ff7-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0ff7-127">INPUTS</span></span>

### <span data-ttu-id="c0ff7-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c0ff7-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="c0ff7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c0ff7-129">System.String</span></span>

## <span data-ttu-id="c0ff7-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0ff7-130">OUTPUTS</span></span>

### <span data-ttu-id="c0ff7-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c0ff7-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="c0ff7-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0ff7-132">NOTES</span></span>

## <span data-ttu-id="c0ff7-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0ff7-133">RELATED LINKS</span></span>
