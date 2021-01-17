---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380695"
---
# <span data-ttu-id="b1fa2-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="b1fa2-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="b1fa2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="b1fa2-103">Rejestruje narzędzie do migrowania projektu.</span><span class="sxs-lookup"><span data-stu-id="b1fa2-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="b1fa2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1fa2-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b1fa2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b1fa2-105">DESCRIPTION</span></span>
<span data-ttu-id="b1fa2-106">Rejestruje narzędzie do migrowania projektu.</span><span class="sxs-lookup"><span data-stu-id="b1fa2-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="b1fa2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1fa2-107">EXAMPLES</span></span>

### <span data-ttu-id="b1fa2-108">Przykład 1: Narzędzie REgister.</span><span class="sxs-lookup"><span data-stu-id="b1fa2-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="b1fa2-109">Rejestruje narzędzie do migrowania projektu.</span><span class="sxs-lookup"><span data-stu-id="b1fa2-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="b1fa2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1fa2-110">PARAMETERS</span></span>

### <span data-ttu-id="b1fa2-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="b1fa2-111">-AcceptLanguage</span></span>
<span data-ttu-id="b1fa2-112">Standardowy nagłówek żądania.</span><span class="sxs-lookup"><span data-stu-id="b1fa2-112">Standard request header.</span></span>
<span data-ttu-id="b1fa2-113">Używana przez usługę do odpowiadania klientowi w odpowiednim języku.</span><span class="sxs-lookup"><span data-stu-id="b1fa2-113">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="b1fa2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1fa2-114">-DefaultProfile</span></span>
<span data-ttu-id="b1fa2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b1fa2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1fa2-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="b1fa2-116">-MigrateProjectName</span></span>
<span data-ttu-id="b1fa2-117">Nazwa projektu migracji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b1fa2-117">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="b1fa2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1fa2-118">-ResourceGroupName</span></span>
<span data-ttu-id="b1fa2-119">Nazwa grupy zasobów platformy Azure, do której należy migracja projektu.</span><span class="sxs-lookup"><span data-stu-id="b1fa2-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="b1fa2-120">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b1fa2-120">-SubscriptionId</span></span>
<span data-ttu-id="b1fa2-121">Identyfikator subskrypcji platformy Azure, w którym został utworzony projekt migrowania.</span><span class="sxs-lookup"><span data-stu-id="b1fa2-121">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="b1fa2-122">-Narzędzie</span><span class="sxs-lookup"><span data-stu-id="b1fa2-122">-Tool</span></span>
<span data-ttu-id="b1fa2-123">Pobiera lub ustawia narzędzie, które ma zostać zarejestrowane.</span><span class="sxs-lookup"><span data-stu-id="b1fa2-123">Gets or sets the tool to be registered.</span></span>

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

### <span data-ttu-id="b1fa2-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b1fa2-124">-Confirm</span></span>
<span data-ttu-id="b1fa2-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1fa2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1fa2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1fa2-126">-WhatIf</span></span>
<span data-ttu-id="b1fa2-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1fa2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1fa2-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b1fa2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1fa2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1fa2-129">CommonParameters</span></span>
<span data-ttu-id="b1fa2-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1fa2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1fa2-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1fa2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1fa2-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1fa2-132">INPUTS</span></span>

## <span data-ttu-id="b1fa2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1fa2-133">OUTPUTS</span></span>

### <span data-ttu-id="b1fa2-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b1fa2-134">System.Boolean</span></span>

## <span data-ttu-id="b1fa2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1fa2-135">NOTES</span></span>

<span data-ttu-id="b1fa2-136">PISUJE</span><span class="sxs-lookup"><span data-stu-id="b1fa2-136">ALIASES</span></span>

## <span data-ttu-id="b1fa2-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1fa2-137">RELATED LINKS</span></span>

