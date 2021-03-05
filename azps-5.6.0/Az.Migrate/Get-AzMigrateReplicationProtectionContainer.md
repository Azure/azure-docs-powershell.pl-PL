---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: 7a1cec73706d1ed799966bc3d97da06867139c33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982858"
---
# <span data-ttu-id="eb085-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="eb085-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="eb085-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb085-102">SYNOPSIS</span></span>
<span data-ttu-id="eb085-103">Pobiera szczegółowe informacje dotyczące kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="eb085-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="eb085-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="eb085-104">SYNTAX</span></span>

### <span data-ttu-id="eb085-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="eb085-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eb085-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="eb085-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb085-107">Lista</span><span class="sxs-lookup"><span data-stu-id="eb085-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="eb085-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="eb085-108">DESCRIPTION</span></span>
<span data-ttu-id="eb085-109">Pobiera szczegółowe informacje dotyczące kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="eb085-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="eb085-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="eb085-110">EXAMPLES</span></span>

### <span data-ttu-id="eb085-111">Przykład 1. Lista wszystkich kontenerów ochrony w magazynie i w materiałach</span><span class="sxs-lookup"><span data-stu-id="eb085-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="eb085-112">Lista wszystkich.</span><span class="sxs-lookup"><span data-stu-id="eb085-112">Lists all.</span></span>

### <span data-ttu-id="eb085-113">Przykład 2. Uzyskiwanie określonego kontenera</span><span class="sxs-lookup"><span data-stu-id="eb085-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="eb085-114">Pobiera określony.</span><span class="sxs-lookup"><span data-stu-id="eb085-114">Gets a specific one.</span></span>

## <span data-ttu-id="eb085-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb085-115">PARAMETERS</span></span>

### <span data-ttu-id="eb085-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb085-116">-DefaultProfile</span></span>
<span data-ttu-id="eb085-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb085-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb085-118">- FabricName</span><span class="sxs-lookup"><span data-stu-id="eb085-118">-FabricName</span></span>
<span data-ttu-id="eb085-119">Nazwa materiału.</span><span class="sxs-lookup"><span data-stu-id="eb085-119">Fabric name.</span></span>

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

### <span data-ttu-id="eb085-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="eb085-120">-ProtectionContainerName</span></span>
<span data-ttu-id="eb085-121">Nazwa kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="eb085-121">Protection container name.</span></span>

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

### <span data-ttu-id="eb085-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb085-122">-ResourceGroupName</span></span>
<span data-ttu-id="eb085-123">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="eb085-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="eb085-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="eb085-124">-ResourceName</span></span>
<span data-ttu-id="eb085-125">Nazwa magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="eb085-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="eb085-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eb085-126">-SubscriptionId</span></span>
<span data-ttu-id="eb085-127">Identyfikator subskrypcji platformy Azure, w którym utworzono projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="eb085-127">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="eb085-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb085-128">CommonParameters</span></span>
<span data-ttu-id="eb085-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb085-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb085-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb085-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb085-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb085-131">INPUTS</span></span>

## <span data-ttu-id="eb085-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb085-132">OUTPUTS</span></span>

### <span data-ttu-id="eb085-133">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api20180110.IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="eb085-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="eb085-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="eb085-134">NOTES</span></span>

<span data-ttu-id="eb085-135">ALIASY</span><span class="sxs-lookup"><span data-stu-id="eb085-135">ALIASES</span></span>

## <span data-ttu-id="eb085-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb085-136">RELATED LINKS</span></span>

