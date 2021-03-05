---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: d9edb00bf7944400fa681f857dd7005d9eaf69b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003754"
---
# <span data-ttu-id="69e72-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="69e72-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="69e72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69e72-102">SYNOPSIS</span></span>
<span data-ttu-id="69e72-103">Usuń projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="69e72-103">Delete the migrate project.</span></span>
<span data-ttu-id="69e72-104">Usuwanie nieistniejącego projektu nie jest operacją.</span><span class="sxs-lookup"><span data-stu-id="69e72-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="69e72-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="69e72-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="69e72-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="69e72-106">DESCRIPTION</span></span>
<span data-ttu-id="69e72-107">Usuń projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="69e72-107">Delete the migrate project.</span></span>
<span data-ttu-id="69e72-108">Usuwanie nieistniejącego projektu nie jest operacją.</span><span class="sxs-lookup"><span data-stu-id="69e72-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="69e72-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="69e72-109">EXAMPLES</span></span>

### <span data-ttu-id="69e72-110">Przykład 1. Usuwanie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="69e72-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="69e72-111">Usuń projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="69e72-111">Delete the migrate project.</span></span>
<span data-ttu-id="69e72-112">Usuwanie nieistniejącego projektu nie jest operacją.</span><span class="sxs-lookup"><span data-stu-id="69e72-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="69e72-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69e72-113">PARAMETERS</span></span>

### <span data-ttu-id="69e72-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="69e72-114">-AcceptLanguage</span></span>
<span data-ttu-id="69e72-115">Nagłówek żądania standardowego.</span><span class="sxs-lookup"><span data-stu-id="69e72-115">Standard request header.</span></span>
<span data-ttu-id="69e72-116">Używany przez usługę do odpowiadania klientowi w odpowiednim języku.</span><span class="sxs-lookup"><span data-stu-id="69e72-116">Used by service to respond to client in appropriate language.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69e72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69e72-117">-DefaultProfile</span></span>
<span data-ttu-id="69e72-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="69e72-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69e72-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="69e72-119">-Name</span></span>
<span data-ttu-id="69e72-120">Nazwa projektu Azure Migrate.</span><span class="sxs-lookup"><span data-stu-id="69e72-120">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="69e72-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69e72-121">-PassThru</span></span>
<span data-ttu-id="69e72-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="69e72-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69e72-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69e72-123">-ResourceGroupName</span></span>
<span data-ttu-id="69e72-124">Nazwa grupy zasobów azure, do których należy migrowanie projektu.</span><span class="sxs-lookup"><span data-stu-id="69e72-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="69e72-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69e72-125">-SubscriptionId</span></span>
<span data-ttu-id="69e72-126">Identyfikator subskrypcji platformy Azure, w którym utworzono projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="69e72-126">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69e72-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69e72-127">-Confirm</span></span>
<span data-ttu-id="69e72-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="69e72-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69e72-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69e72-129">-WhatIf</span></span>
<span data-ttu-id="69e72-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69e72-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69e72-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="69e72-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69e72-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e72-132">CommonParameters</span></span>
<span data-ttu-id="69e72-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69e72-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e72-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69e72-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e72-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69e72-135">INPUTS</span></span>

## <span data-ttu-id="69e72-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69e72-136">OUTPUTS</span></span>

### <span data-ttu-id="69e72-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69e72-137">System.Boolean</span></span>

## <span data-ttu-id="69e72-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="69e72-138">NOTES</span></span>

<span data-ttu-id="69e72-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="69e72-139">ALIASES</span></span>

## <span data-ttu-id="69e72-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69e72-140">RELATED LINKS</span></span>

