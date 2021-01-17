---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: e0918573b7fc1190d32aaaaa4bfe73ed9fe05fe6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490125"
---
# <span data-ttu-id="6785c-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="6785c-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="6785c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6785c-102">SYNOPSIS</span></span>
<span data-ttu-id="6785c-103">Usuwanie projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="6785c-103">Delete the migrate project.</span></span>
<span data-ttu-id="6785c-104">Usuwanie nieistniejącego projektu jest operacją No-Operation.</span><span class="sxs-lookup"><span data-stu-id="6785c-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="6785c-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6785c-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6785c-106">Opis</span><span class="sxs-lookup"><span data-stu-id="6785c-106">DESCRIPTION</span></span>
<span data-ttu-id="6785c-107">Usuwanie projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="6785c-107">Delete the migrate project.</span></span>
<span data-ttu-id="6785c-108">Usuwanie nieistniejącego projektu jest operacją No-Operation.</span><span class="sxs-lookup"><span data-stu-id="6785c-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="6785c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6785c-109">EXAMPLES</span></span>

### <span data-ttu-id="6785c-110">Przykład 1. Delete (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="6785c-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="6785c-111">Usuwanie projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="6785c-111">Delete the migrate project.</span></span>
<span data-ttu-id="6785c-112">Usuwanie nieistniejącego projektu jest operacją No-Operation.</span><span class="sxs-lookup"><span data-stu-id="6785c-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="6785c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6785c-113">PARAMETERS</span></span>

### <span data-ttu-id="6785c-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="6785c-114">-AcceptLanguage</span></span>
<span data-ttu-id="6785c-115">Standardowy nagłówek żądania.</span><span class="sxs-lookup"><span data-stu-id="6785c-115">Standard request header.</span></span>
<span data-ttu-id="6785c-116">Używana przez usługę do odpowiadania klientowi w odpowiednim języku.</span><span class="sxs-lookup"><span data-stu-id="6785c-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="6785c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6785c-117">-DefaultProfile</span></span>
<span data-ttu-id="6785c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6785c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6785c-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6785c-119">-Name</span></span>
<span data-ttu-id="6785c-120">Nazwa projektu migracji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6785c-120">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="6785c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6785c-121">-PassThru</span></span>
<span data-ttu-id="6785c-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="6785c-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6785c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6785c-123">-ResourceGroupName</span></span>
<span data-ttu-id="6785c-124">Nazwa grupy zasobów platformy Azure, do której należy migracja projektu.</span><span class="sxs-lookup"><span data-stu-id="6785c-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="6785c-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6785c-125">-SubscriptionId</span></span>
<span data-ttu-id="6785c-126">Identyfikator subskrypcji platformy Azure, w którym został utworzony projekt migrowania.</span><span class="sxs-lookup"><span data-stu-id="6785c-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="6785c-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6785c-127">-Confirm</span></span>
<span data-ttu-id="6785c-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6785c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6785c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6785c-129">-WhatIf</span></span>
<span data-ttu-id="6785c-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6785c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6785c-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6785c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6785c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6785c-132">CommonParameters</span></span>
<span data-ttu-id="6785c-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6785c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6785c-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6785c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6785c-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6785c-135">INPUTS</span></span>

## <span data-ttu-id="6785c-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6785c-136">OUTPUTS</span></span>

### <span data-ttu-id="6785c-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6785c-137">System.Boolean</span></span>

## <span data-ttu-id="6785c-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6785c-138">NOTES</span></span>

<span data-ttu-id="6785c-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="6785c-139">ALIASES</span></span>

## <span data-ttu-id="6785c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6785c-140">RELATED LINKS</span></span>

