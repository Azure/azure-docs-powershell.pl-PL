---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490146"
---
# <span data-ttu-id="1a38b-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="1a38b-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="1a38b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1a38b-102">SYNOPSIS</span></span>
<span data-ttu-id="1a38b-103">Metoda pobierania projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="1a38b-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="1a38b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1a38b-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1a38b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1a38b-105">DESCRIPTION</span></span>
<span data-ttu-id="1a38b-106">Metoda pobierania projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="1a38b-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="1a38b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1a38b-107">EXAMPLES</span></span>

### <span data-ttu-id="1a38b-108">Przykład 1: Uzyskaj</span><span class="sxs-lookup"><span data-stu-id="1a38b-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="1a38b-109">Metoda pobierania projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="1a38b-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="1a38b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a38b-110">PARAMETERS</span></span>

### <span data-ttu-id="1a38b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a38b-111">-DefaultProfile</span></span>
<span data-ttu-id="1a38b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a38b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a38b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1a38b-113">-Name</span></span>
<span data-ttu-id="1a38b-114">Nazwa projektu migracji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1a38b-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="1a38b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a38b-115">-ResourceGroupName</span></span>
<span data-ttu-id="1a38b-116">Nazwa grupy zasobów platformy Azure, do której należy migracja projektu.</span><span class="sxs-lookup"><span data-stu-id="1a38b-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="1a38b-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1a38b-117">-SubscriptionId</span></span>
<span data-ttu-id="1a38b-118">Identyfikator subskrypcji platformy Azure, w którym został utworzony projekt migrowania.</span><span class="sxs-lookup"><span data-stu-id="1a38b-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="1a38b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a38b-119">CommonParameters</span></span>
<span data-ttu-id="1a38b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a38b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a38b-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a38b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a38b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a38b-122">INPUTS</span></span>

## <span data-ttu-id="1a38b-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1a38b-123">OUTPUTS</span></span>

### <span data-ttu-id="1a38b-124">Microsoft. Azure. PowerShell. polecenia. Migruj. MODELES. Api20180901Preview. IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="1a38b-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="1a38b-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1a38b-125">NOTES</span></span>

<span data-ttu-id="1a38b-126">PISUJE</span><span class="sxs-lookup"><span data-stu-id="1a38b-126">ALIASES</span></span>

## <span data-ttu-id="1a38b-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a38b-127">RELATED LINKS</span></span>

