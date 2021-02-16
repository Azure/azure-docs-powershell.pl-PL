---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: e0918573b7fc1190d32aaaaa4bfe73ed9fe05fe6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185066"
---
# <span data-ttu-id="ddf27-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="ddf27-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="ddf27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddf27-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf27-103">Usuń projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="ddf27-103">Delete the migrate project.</span></span>
<span data-ttu-id="ddf27-104">Usuwanie nieistniejący projekt nie jest operacją.</span><span class="sxs-lookup"><span data-stu-id="ddf27-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="ddf27-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ddf27-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ddf27-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="ddf27-106">DESCRIPTION</span></span>
<span data-ttu-id="ddf27-107">Usuń projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="ddf27-107">Delete the migrate project.</span></span>
<span data-ttu-id="ddf27-108">Usuwanie nieistniejący projekt nie jest operacją.</span><span class="sxs-lookup"><span data-stu-id="ddf27-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="ddf27-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ddf27-109">EXAMPLES</span></span>

### <span data-ttu-id="ddf27-110">Przykład 1. Usuwanie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ddf27-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="ddf27-111">Usuń projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="ddf27-111">Delete the migrate project.</span></span>
<span data-ttu-id="ddf27-112">Usuwanie nieistniejący projekt nie jest operacją.</span><span class="sxs-lookup"><span data-stu-id="ddf27-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="ddf27-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddf27-113">PARAMETERS</span></span>

### <span data-ttu-id="ddf27-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="ddf27-114">-AcceptLanguage</span></span>
<span data-ttu-id="ddf27-115">Nagłówek żądania standardowego.</span><span class="sxs-lookup"><span data-stu-id="ddf27-115">Standard request header.</span></span>
<span data-ttu-id="ddf27-116">Używany przez usługę do odpowiadania klientowi w odpowiednim języku.</span><span class="sxs-lookup"><span data-stu-id="ddf27-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="ddf27-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf27-117">-DefaultProfile</span></span>
<span data-ttu-id="ddf27-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ddf27-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddf27-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ddf27-119">-Name</span></span>
<span data-ttu-id="ddf27-120">Nazwa projektu Azure Migrate.</span><span class="sxs-lookup"><span data-stu-id="ddf27-120">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="ddf27-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddf27-121">-PassThru</span></span>
<span data-ttu-id="ddf27-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="ddf27-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ddf27-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddf27-123">-ResourceGroupName</span></span>
<span data-ttu-id="ddf27-124">Nazwa grupy zasobów azure, do których należy migrowanie projektu.</span><span class="sxs-lookup"><span data-stu-id="ddf27-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="ddf27-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ddf27-125">-SubscriptionId</span></span>
<span data-ttu-id="ddf27-126">Identyfikator subskrypcji platformy Azure, w którym utworzono projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="ddf27-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="ddf27-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ddf27-127">-Confirm</span></span>
<span data-ttu-id="ddf27-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ddf27-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddf27-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddf27-129">-WhatIf</span></span>
<span data-ttu-id="ddf27-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddf27-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddf27-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ddf27-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddf27-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf27-132">CommonParameters</span></span>
<span data-ttu-id="ddf27-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddf27-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf27-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ddf27-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf27-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddf27-135">INPUTS</span></span>

## <span data-ttu-id="ddf27-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddf27-136">OUTPUTS</span></span>

### <span data-ttu-id="ddf27-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ddf27-137">System.Boolean</span></span>

## <span data-ttu-id="ddf27-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ddf27-138">NOTES</span></span>

<span data-ttu-id="ddf27-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ddf27-139">ALIASES</span></span>

## <span data-ttu-id="ddf27-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ddf27-140">RELATED LINKS</span></span>

