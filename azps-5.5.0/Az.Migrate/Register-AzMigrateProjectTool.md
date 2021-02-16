---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185075"
---
# <span data-ttu-id="04823-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="04823-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="04823-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04823-102">SYNOPSIS</span></span>
<span data-ttu-id="04823-103">Rejestruje narzędzie w ramach migrowania projektu.</span><span class="sxs-lookup"><span data-stu-id="04823-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="04823-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="04823-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="04823-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="04823-105">DESCRIPTION</span></span>
<span data-ttu-id="04823-106">Rejestruje narzędzie w ramach migrowania projektu.</span><span class="sxs-lookup"><span data-stu-id="04823-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="04823-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="04823-107">EXAMPLES</span></span>

### <span data-ttu-id="04823-108">Przykład 1. Narzędzie Wąsy.</span><span class="sxs-lookup"><span data-stu-id="04823-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="04823-109">Rejestruje narzędzie w ramach migrowania projektu.</span><span class="sxs-lookup"><span data-stu-id="04823-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="04823-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04823-110">PARAMETERS</span></span>

### <span data-ttu-id="04823-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="04823-111">-AcceptLanguage</span></span>
<span data-ttu-id="04823-112">Nagłówek żądania standardowego.</span><span class="sxs-lookup"><span data-stu-id="04823-112">Standard request header.</span></span>
<span data-ttu-id="04823-113">Używany przez usługę do odpowiadania klientowi w odpowiednim języku.</span><span class="sxs-lookup"><span data-stu-id="04823-113">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="04823-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04823-114">-DefaultProfile</span></span>
<span data-ttu-id="04823-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="04823-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04823-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="04823-116">-MigrateProjectName</span></span>
<span data-ttu-id="04823-117">Nazwa projektu Azure Migrate.</span><span class="sxs-lookup"><span data-stu-id="04823-117">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="04823-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04823-118">-ResourceGroupName</span></span>
<span data-ttu-id="04823-119">Nazwa grupy zasobów azure, do których należy migrowanie projektu.</span><span class="sxs-lookup"><span data-stu-id="04823-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="04823-120">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="04823-120">-SubscriptionId</span></span>
<span data-ttu-id="04823-121">Identyfikator subskrypcji platformy Azure, w którym utworzono projekt migracji.</span><span class="sxs-lookup"><span data-stu-id="04823-121">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="04823-122">— narzędzie</span><span class="sxs-lookup"><span data-stu-id="04823-122">-Tool</span></span>
<span data-ttu-id="04823-123">Pobiera lub ustawia narzędzie do zarejestrowania.</span><span class="sxs-lookup"><span data-stu-id="04823-123">Gets or sets the tool to be registered.</span></span>

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

### <span data-ttu-id="04823-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04823-124">-Confirm</span></span>
<span data-ttu-id="04823-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="04823-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04823-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04823-126">-WhatIf</span></span>
<span data-ttu-id="04823-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04823-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04823-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="04823-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04823-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04823-129">CommonParameters</span></span>
<span data-ttu-id="04823-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04823-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04823-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04823-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04823-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04823-132">INPUTS</span></span>

## <span data-ttu-id="04823-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04823-133">OUTPUTS</span></span>

### <span data-ttu-id="04823-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="04823-134">System.Boolean</span></span>

## <span data-ttu-id="04823-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="04823-135">NOTES</span></span>

<span data-ttu-id="04823-136">ALIASY</span><span class="sxs-lookup"><span data-stu-id="04823-136">ALIASES</span></span>

## <span data-ttu-id="04823-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04823-137">RELATED LINKS</span></span>

