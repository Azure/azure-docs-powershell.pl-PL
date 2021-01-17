---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: a89d762f0317075a0da94290ad964aeef133fdd5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490149"
---
# <span data-ttu-id="dac8a-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="dac8a-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="dac8a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dac8a-102">SYNOPSIS</span></span>
<span data-ttu-id="dac8a-103">Pobiera szczegóły kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="dac8a-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="dac8a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dac8a-104">SYNTAX</span></span>

### <span data-ttu-id="dac8a-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="dac8a-105">List (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dac8a-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="dac8a-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="dac8a-107">List1</span><span class="sxs-lookup"><span data-stu-id="dac8a-107">List1</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dac8a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dac8a-108">DESCRIPTION</span></span>
<span data-ttu-id="dac8a-109">Pobiera szczegóły kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="dac8a-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="dac8a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dac8a-110">EXAMPLES</span></span>

### <span data-ttu-id="dac8a-111">Przykład 1: Lista wszystkich kontenerów ochrony w magazynie i w sieci szkieletowej</span><span class="sxs-lookup"><span data-stu-id="dac8a-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="dac8a-112">Lista wszystkich.</span><span class="sxs-lookup"><span data-stu-id="dac8a-112">Lists all.</span></span>

### <span data-ttu-id="dac8a-113">Przykład 2: uzyskiwanie określonego kontenera</span><span class="sxs-lookup"><span data-stu-id="dac8a-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="dac8a-114">Pobiera określoną wartość.</span><span class="sxs-lookup"><span data-stu-id="dac8a-114">Gets a specific one.</span></span>

## <span data-ttu-id="dac8a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dac8a-115">PARAMETERS</span></span>

### <span data-ttu-id="dac8a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dac8a-116">-DefaultProfile</span></span>
<span data-ttu-id="dac8a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dac8a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dac8a-118">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="dac8a-118">-FabricName</span></span>
<span data-ttu-id="dac8a-119">Nazwa sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="dac8a-119">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac8a-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="dac8a-120">-ProtectionContainerName</span></span>
<span data-ttu-id="dac8a-121">Nazwa kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="dac8a-121">Protection container name.</span></span>

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

### <span data-ttu-id="dac8a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dac8a-122">-ResourceGroupName</span></span>
<span data-ttu-id="dac8a-123">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="dac8a-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="dac8a-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="dac8a-124">-ResourceName</span></span>
<span data-ttu-id="dac8a-125">Nazwa magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="dac8a-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="dac8a-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="dac8a-126">-SubscriptionId</span></span>
<span data-ttu-id="dac8a-127">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="dac8a-127">The subscription Id.</span></span>

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

### <span data-ttu-id="dac8a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dac8a-128">CommonParameters</span></span>
<span data-ttu-id="dac8a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dac8a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dac8a-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dac8a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dac8a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dac8a-131">INPUTS</span></span>

## <span data-ttu-id="dac8a-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dac8a-132">OUTPUTS</span></span>

### <span data-ttu-id="dac8a-133">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="dac8a-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="dac8a-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dac8a-134">NOTES</span></span>

<span data-ttu-id="dac8a-135">PISUJE</span><span class="sxs-lookup"><span data-stu-id="dac8a-135">ALIASES</span></span>

## <span data-ttu-id="dac8a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dac8a-136">RELATED LINKS</span></span>

