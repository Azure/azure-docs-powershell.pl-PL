---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: e321691106d892c703a56bd94c3fe84ab7d9fe38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234534"
---
# <span data-ttu-id="37bc7-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="37bc7-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="37bc7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="37bc7-103">Pobiera szczegóły mapowania kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="37bc7-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="37bc7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37bc7-104">SYNTAX</span></span>

### <span data-ttu-id="37bc7-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="37bc7-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="37bc7-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="37bc7-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="37bc7-107">Lista</span><span class="sxs-lookup"><span data-stu-id="37bc7-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="37bc7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="37bc7-108">DESCRIPTION</span></span>
<span data-ttu-id="37bc7-109">Pobiera szczegóły mapowania kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="37bc7-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="37bc7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37bc7-110">EXAMPLES</span></span>

### <span data-ttu-id="37bc7-111">Przykład 1: uzyskiwanie określonego mapowania</span><span class="sxs-lookup"><span data-stu-id="37bc7-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="37bc7-112">Uzyskiwanie szczegółowych informacji o mapowaniu.</span><span class="sxs-lookup"><span data-stu-id="37bc7-112">Get a mapping detail.</span></span>

## <span data-ttu-id="37bc7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37bc7-113">PARAMETERS</span></span>

### <span data-ttu-id="37bc7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37bc7-114">-DefaultProfile</span></span>
<span data-ttu-id="37bc7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="37bc7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37bc7-116">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="37bc7-116">-FabricName</span></span>
<span data-ttu-id="37bc7-117">Nazwa sieci szkieletowej.</span><span class="sxs-lookup"><span data-stu-id="37bc7-117">Fabric name.</span></span>

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

### <span data-ttu-id="37bc7-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="37bc7-118">-MappingName</span></span>
<span data-ttu-id="37bc7-119">Nazwa mapowania kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="37bc7-119">Protection Container mapping name.</span></span>

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

### <span data-ttu-id="37bc7-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="37bc7-120">-ProtectionContainerName</span></span>
<span data-ttu-id="37bc7-121">Nazwa kontenera ochrony.</span><span class="sxs-lookup"><span data-stu-id="37bc7-121">Protection container name.</span></span>

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

### <span data-ttu-id="37bc7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37bc7-122">-ResourceGroupName</span></span>
<span data-ttu-id="37bc7-123">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="37bc7-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="37bc7-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="37bc7-124">-ResourceName</span></span>
<span data-ttu-id="37bc7-125">Nazwa magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="37bc7-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="37bc7-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="37bc7-126">-SubscriptionId</span></span>
<span data-ttu-id="37bc7-127">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="37bc7-127">The subscription Id.</span></span>

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

### <span data-ttu-id="37bc7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37bc7-128">CommonParameters</span></span>
<span data-ttu-id="37bc7-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37bc7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37bc7-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37bc7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37bc7-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37bc7-131">INPUTS</span></span>

## <span data-ttu-id="37bc7-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37bc7-132">OUTPUTS</span></span>

### <span data-ttu-id="37bc7-133">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180110. IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="37bc7-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="37bc7-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37bc7-134">NOTES</span></span>

<span data-ttu-id="37bc7-135">PISUJE</span><span class="sxs-lookup"><span data-stu-id="37bc7-135">ALIASES</span></span>

## <span data-ttu-id="37bc7-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37bc7-136">RELATED LINKS</span></span>

