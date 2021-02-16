---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: e706e9eb21f601ed1a266faa0afb888297f17fdb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190155"
---
# <span data-ttu-id="afed4-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="afed4-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="afed4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afed4-102">SYNOPSIS</span></span>
<span data-ttu-id="afed4-103">Pobiera szczegółowe informacje o zarejestrowanym dostawcy usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="afed4-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="afed4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="afed4-104">SYNTAX</span></span>

### <span data-ttu-id="afed4-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="afed4-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="afed4-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="afed4-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="afed4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="afed4-107">DESCRIPTION</span></span>
<span data-ttu-id="afed4-108">Pobiera szczegółowe informacje o zarejestrowanym dostawcy usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="afed4-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="afed4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="afed4-109">EXAMPLES</span></span>

### <span data-ttu-id="afed4-110">Przykład 1. Uzyskiwanie wszystkich dostawców w magazynie</span><span class="sxs-lookup"><span data-stu-id="afed4-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="afed4-111">Lista wszystkich.</span><span class="sxs-lookup"><span data-stu-id="afed4-111">List all.</span></span>

## <span data-ttu-id="afed4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afed4-112">PARAMETERS</span></span>

### <span data-ttu-id="afed4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afed4-113">-DefaultProfile</span></span>
<span data-ttu-id="afed4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="afed4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afed4-115">- FabricName</span><span class="sxs-lookup"><span data-stu-id="afed4-115">-FabricName</span></span>
<span data-ttu-id="afed4-116">Nazwa materiału.</span><span class="sxs-lookup"><span data-stu-id="afed4-116">Fabric name.</span></span>

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

### <span data-ttu-id="afed4-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="afed4-117">-ProviderName</span></span>
<span data-ttu-id="afed4-118">Nazwa dostawcy usług odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="afed4-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="afed4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afed4-119">-ResourceGroupName</span></span>
<span data-ttu-id="afed4-120">Nazwa grupy zasobów, w której znajduje się magazyn usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="afed4-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="afed4-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="afed4-121">-ResourceName</span></span>
<span data-ttu-id="afed4-122">Nazwa magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="afed4-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="afed4-123">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="afed4-123">-SubscriptionId</span></span>
<span data-ttu-id="afed4-124">Identyfikator subskrypcji platformy Azure, w którym utworzono projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="afed4-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="afed4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afed4-125">CommonParameters</span></span>
<span data-ttu-id="afed4-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afed4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afed4-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afed4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afed4-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afed4-128">INPUTS</span></span>

## <span data-ttu-id="afed4-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="afed4-129">OUTPUTS</span></span>

### <span data-ttu-id="afed4-130">Microsoft.Azure.PowerShell.Cmdlet.Migrate.Models.Api20180110.IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="afed4-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="afed4-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="afed4-131">NOTES</span></span>

<span data-ttu-id="afed4-132">ALIASY</span><span class="sxs-lookup"><span data-stu-id="afed4-132">ALIASES</span></span>

## <span data-ttu-id="afed4-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afed4-133">RELATED LINKS</span></span>

