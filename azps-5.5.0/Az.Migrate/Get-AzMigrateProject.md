---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241227"
---
# <span data-ttu-id="50499-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="50499-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="50499-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50499-102">SYNOPSIS</span></span>
<span data-ttu-id="50499-103">Metoda uzyskania migrowania projektu.</span><span class="sxs-lookup"><span data-stu-id="50499-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="50499-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="50499-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="50499-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="50499-105">DESCRIPTION</span></span>
<span data-ttu-id="50499-106">Metoda uzyskania migrowania projektu.</span><span class="sxs-lookup"><span data-stu-id="50499-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="50499-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="50499-107">EXAMPLES</span></span>

### <span data-ttu-id="50499-108">Przykład 1. Pobierz</span><span class="sxs-lookup"><span data-stu-id="50499-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="50499-109">Metoda uzyskania migrowania projektu.</span><span class="sxs-lookup"><span data-stu-id="50499-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="50499-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50499-110">PARAMETERS</span></span>

### <span data-ttu-id="50499-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50499-111">-DefaultProfile</span></span>
<span data-ttu-id="50499-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="50499-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50499-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="50499-113">-Name</span></span>
<span data-ttu-id="50499-114">Nazwa projektu Azure Migrate.</span><span class="sxs-lookup"><span data-stu-id="50499-114">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50499-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50499-115">-ResourceGroupName</span></span>
<span data-ttu-id="50499-116">Nazwa grupy zasobów azure, do których należy migrowanie projektu.</span><span class="sxs-lookup"><span data-stu-id="50499-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="50499-117">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50499-117">-SubscriptionId</span></span>
<span data-ttu-id="50499-118">Identyfikator subskrypcji platformy Azure, w którym utworzono projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="50499-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="50499-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50499-119">CommonParameters</span></span>
<span data-ttu-id="50499-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50499-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50499-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50499-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50499-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50499-122">INPUTS</span></span>

## <span data-ttu-id="50499-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50499-123">OUTPUTS</span></span>

### <span data-ttu-id="50499-124">Microsoft.Azure.PowerShell.Cmdlet.Migrate.Models.Api20180901Preview.IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="50499-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="50499-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="50499-125">NOTES</span></span>

<span data-ttu-id="50499-126">ALIASY</span><span class="sxs-lookup"><span data-stu-id="50499-126">ALIASES</span></span>

## <span data-ttu-id="50499-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50499-127">RELATED LINKS</span></span>

