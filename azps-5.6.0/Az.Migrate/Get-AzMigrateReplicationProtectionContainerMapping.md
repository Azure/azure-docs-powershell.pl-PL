---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: 87fa8d8653d0409eb4b322e0ce21dbc9c8cfa668
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982842"
---
# <span data-ttu-id="d004b-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d004b-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="d004b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d004b-102">SYNOPSIS</span></span>
<span data-ttu-id="d004b-103">Pobiera szczegółowe informacje dotyczące mapowania kontenerów ochrony.</span><span class="sxs-lookup"><span data-stu-id="d004b-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="d004b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d004b-104">SYNTAX</span></span>

### <span data-ttu-id="d004b-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d004b-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d004b-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="d004b-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d004b-107">Lista</span><span class="sxs-lookup"><span data-stu-id="d004b-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d004b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d004b-108">DESCRIPTION</span></span>
<span data-ttu-id="d004b-109">Pobiera szczegółowe informacje dotyczące mapowania kontenerów ochrony.</span><span class="sxs-lookup"><span data-stu-id="d004b-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="d004b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d004b-110">EXAMPLES</span></span>

### <span data-ttu-id="d004b-111">Przykład 1. Uzyskiwanie określonego mapowania</span><span class="sxs-lookup"><span data-stu-id="d004b-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="d004b-112">Uzyskaj szczegółowe informacje dotyczące mapowania.</span><span class="sxs-lookup"><span data-stu-id="d004b-112">Get a mapping detail.</span></span>

## <span data-ttu-id="d004b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d004b-113">PARAMETERS</span></span>

### <span data-ttu-id="d004b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d004b-114">-DefaultProfile</span></span>
<span data-ttu-id="d004b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d004b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d004b-116">- FabricName</span><span class="sxs-lookup"><span data-stu-id="d004b-116">-FabricName</span></span>
<span data-ttu-id="d004b-117">Nazwa materiału.</span><span class="sxs-lookup"><span data-stu-id="d004b-117">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d004b-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="d004b-118">-MappingName</span></span>
<span data-ttu-id="d004b-119">Nazwa mapowania kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="d004b-119">Protection Container mapping name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d004b-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="d004b-120">-ProtectionContainerName</span></span>
<span data-ttu-id="d004b-121">Nazwa kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="d004b-121">Protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d004b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d004b-122">-ResourceGroupName</span></span>
<span data-ttu-id="d004b-123">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d004b-123">The name of the resource group where the recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d004b-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d004b-124">-ResourceName</span></span>
<span data-ttu-id="d004b-125">Nazwa magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d004b-125">The name of the recovery services vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d004b-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d004b-126">-SubscriptionId</span></span>
<span data-ttu-id="d004b-127">Identyfikator subskrypcji platformy Azure, w którym utworzono projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="d004b-127">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d004b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d004b-128">CommonParameters</span></span>
<span data-ttu-id="d004b-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d004b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d004b-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d004b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d004b-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d004b-131">INPUTS</span></span>

## <span data-ttu-id="d004b-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d004b-132">OUTPUTS</span></span>

### <span data-ttu-id="d004b-133">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d004b-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="d004b-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d004b-134">NOTES</span></span>

<span data-ttu-id="d004b-135">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d004b-135">ALIASES</span></span>

## <span data-ttu-id="d004b-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d004b-136">RELATED LINKS</span></span>

