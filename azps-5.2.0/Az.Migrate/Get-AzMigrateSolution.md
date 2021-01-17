---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: 62b43668e8d886a11a26204edcd3c8b13635eff4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371035"
---
# <span data-ttu-id="d8000-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="d8000-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="d8000-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8000-102">SYNOPSIS</span></span>
<span data-ttu-id="d8000-103">Umożliwia odprowadzenie rozwiązania w projekcie migracji.</span><span class="sxs-lookup"><span data-stu-id="d8000-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="d8000-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8000-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d8000-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d8000-105">DESCRIPTION</span></span>
<span data-ttu-id="d8000-106">Umożliwia odprowadzenie rozwiązania w projekcie migracji.</span><span class="sxs-lookup"><span data-stu-id="d8000-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="d8000-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8000-107">EXAMPLES</span></span>

### <span data-ttu-id="d8000-108">Przykład 1: Uzyskaj</span><span class="sxs-lookup"><span data-stu-id="d8000-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="d8000-109">Rozpocznij Migrowanie rozwiązania projektu według nazwy.</span><span class="sxs-lookup"><span data-stu-id="d8000-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="d8000-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8000-110">PARAMETERS</span></span>

### <span data-ttu-id="d8000-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8000-111">-DefaultProfile</span></span>
<span data-ttu-id="d8000-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8000-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8000-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="d8000-113">-MigrateProjectName</span></span>
<span data-ttu-id="d8000-114">Nazwa projektu migracji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d8000-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="d8000-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d8000-115">-Name</span></span>
<span data-ttu-id="d8000-116">Unikatowa nazwa rozwiązania migracji w projekcie migracji.</span><span class="sxs-lookup"><span data-stu-id="d8000-116">Unique name of a migration solution within a migrate project.</span></span>

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

### <span data-ttu-id="d8000-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8000-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8000-118">Nazwa grupy zasobów platformy Azure, do której należy migracja projektu.</span><span class="sxs-lookup"><span data-stu-id="d8000-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="d8000-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d8000-119">-SubscriptionId</span></span>
<span data-ttu-id="d8000-120">Identyfikator subskrypcji platformy Azure, w którym został utworzony projekt migrowania.</span><span class="sxs-lookup"><span data-stu-id="d8000-120">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="d8000-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8000-121">CommonParameters</span></span>
<span data-ttu-id="d8000-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8000-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8000-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8000-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8000-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8000-124">INPUTS</span></span>

## <span data-ttu-id="d8000-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8000-125">OUTPUTS</span></span>

### <span data-ttu-id="d8000-126">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180901Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="d8000-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="d8000-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8000-127">NOTES</span></span>

<span data-ttu-id="d8000-128">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d8000-128">ALIASES</span></span>

## <span data-ttu-id="d8000-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8000-129">RELATED LINKS</span></span>

