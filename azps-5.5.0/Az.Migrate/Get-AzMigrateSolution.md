---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: 62b43668e8d886a11a26204edcd3c8b13635eff4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241226"
---
# <span data-ttu-id="31448-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="31448-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="31448-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31448-102">SYNOPSIS</span></span>
<span data-ttu-id="31448-103">Pobiera rozwiązanie w projekcie migracji.</span><span class="sxs-lookup"><span data-stu-id="31448-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="31448-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="31448-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="31448-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="31448-105">DESCRIPTION</span></span>
<span data-ttu-id="31448-106">Pobiera rozwiązanie w projekcie migracji.</span><span class="sxs-lookup"><span data-stu-id="31448-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="31448-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="31448-107">EXAMPLES</span></span>

### <span data-ttu-id="31448-108">Przykład 1. Pobierz</span><span class="sxs-lookup"><span data-stu-id="31448-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="31448-109">Uzyskaj rozwiązanie do migrowania projektu według nazwy.</span><span class="sxs-lookup"><span data-stu-id="31448-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="31448-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31448-110">PARAMETERS</span></span>

### <span data-ttu-id="31448-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31448-111">-DefaultProfile</span></span>
<span data-ttu-id="31448-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="31448-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31448-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="31448-113">-MigrateProjectName</span></span>
<span data-ttu-id="31448-114">Nazwa projektu Azure Migrate.</span><span class="sxs-lookup"><span data-stu-id="31448-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="31448-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="31448-115">-Name</span></span>
<span data-ttu-id="31448-116">Unikatowa nazwa rozwiązania do migracji w projekcie migracji.</span><span class="sxs-lookup"><span data-stu-id="31448-116">Unique name of a migration solution within a migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31448-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31448-117">-ResourceGroupName</span></span>
<span data-ttu-id="31448-118">Nazwa grupy zasobów azure, do których należy migrowanie projektu.</span><span class="sxs-lookup"><span data-stu-id="31448-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="31448-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31448-119">-SubscriptionId</span></span>
<span data-ttu-id="31448-120">Identyfikator subskrypcji platformy Azure, w którym utworzono projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="31448-120">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="31448-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31448-121">CommonParameters</span></span>
<span data-ttu-id="31448-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31448-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31448-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31448-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31448-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31448-124">INPUTS</span></span>

## <span data-ttu-id="31448-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31448-125">OUTPUTS</span></span>

### <span data-ttu-id="31448-126">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api20180901Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="31448-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="31448-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="31448-127">NOTES</span></span>

<span data-ttu-id="31448-128">ALIASY</span><span class="sxs-lookup"><span data-stu-id="31448-128">ALIASES</span></span>

## <span data-ttu-id="31448-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31448-129">RELATED LINKS</span></span>

