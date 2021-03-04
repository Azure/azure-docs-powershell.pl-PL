---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/initialize-azmigratereplicationinfrastructure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Initialize-AzMigrateReplicationInfrastructure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Initialize-AzMigrateReplicationInfrastructure.md
ms.openlocfilehash: 27206ac1c4e256efcd4093c8cdc9647b6059b3ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982785"
---
# <span data-ttu-id="b8a0c-101">Initialize-AzMigrateReplicationInfrastructure</span><span class="sxs-lookup"><span data-stu-id="b8a0c-101">Initialize-AzMigrateReplicationInfrastructure</span></span>

## <span data-ttu-id="b8a0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a0c-103">Inicjuje infrastrukturę dla projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-103">Initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="b8a0c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b8a0c-104">SYNTAX</span></span>

```
Initialize-AzMigrateReplicationInfrastructure -ProjectName <String> -ResourceGroupName <String>
 -Scenario <String> -TargetRegion <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b8a0c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b8a0c-105">DESCRIPTION</span></span>
<span data-ttu-id="b8a0c-106">Polecenie Initialize-AzMigrateReplicationInfrastructure inicjuje infrastrukturę dla migrowania projektu.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-106">The Initialize-AzMigrateReplicationInfrastructure cmdlet initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="b8a0c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b8a0c-107">EXAMPLES</span></span>

### <span data-ttu-id="b8a0c-108">Przykład 1. Inicjuje infrastrukturę dla projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-108">Example 1: Initialises the infrastructure for the migrate project.</span></span>
```powershell
PS C:\> Initialize-AzMigrateReplicationInfrastructure.ps1 -ResourceGroupName TestRG  -ProjectName TestProject -Vmwareagentless -TargetRegion centralus

True
```

<span data-ttu-id="b8a0c-109">Inicjuje infrastrukturę dla projektu migracji.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-109">Initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="b8a0c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8a0c-110">PARAMETERS</span></span>

### <span data-ttu-id="b8a0c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a0c-111">-DefaultProfile</span></span>
<span data-ttu-id="b8a0c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8a0c-113">— Nazwa_projektu</span><span class="sxs-lookup"><span data-stu-id="b8a0c-113">-ProjectName</span></span>
<span data-ttu-id="b8a0c-114">Określa nazwę projektu migracji platformy Azure, który ma być używany do migracji serwerów.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-114">Specifies the name of the Azure Migrate project to be used for server migration.</span></span>

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

### <span data-ttu-id="b8a0c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8a0c-115">-ResourceGroupName</span></span>
<span data-ttu-id="b8a0c-116">Określa grupę zasobów projektu migracji platformy Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-116">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="b8a0c-117">— Scenariusz</span><span class="sxs-lookup"><span data-stu-id="b8a0c-117">-Scenario</span></span>
<span data-ttu-id="b8a0c-118">Określa scenariusz migracji serwera, dla którego należy zainicjować infrastrukturę replikacji.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-118">Specifies the server migration scenario for which the replication infrastructure needs to be initialized.</span></span>

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

### <span data-ttu-id="b8a0c-119">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8a0c-119">-SubscriptionId</span></span>
<span data-ttu-id="b8a0c-120">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b8a0c-121">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="b8a0c-121">-TargetRegion</span></span>
<span data-ttu-id="b8a0c-122">Określa docelowy region platformy Azure na czas migracji serwerów.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-122">Specifies the target Azure region for server migrations.</span></span>

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

### <span data-ttu-id="b8a0c-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8a0c-123">-Confirm</span></span>
<span data-ttu-id="b8a0c-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8a0c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8a0c-125">-WhatIf</span></span>
<span data-ttu-id="b8a0c-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8a0c-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8a0c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a0c-128">CommonParameters</span></span>
<span data-ttu-id="b8a0c-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8a0c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a0c-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8a0c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a0c-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8a0c-131">INPUTS</span></span>

## <span data-ttu-id="b8a0c-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8a0c-132">OUTPUTS</span></span>

### <span data-ttu-id="b8a0c-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b8a0c-133">System.Boolean</span></span>

## <span data-ttu-id="b8a0c-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b8a0c-134">NOTES</span></span>

<span data-ttu-id="b8a0c-135">ALIASY</span><span class="sxs-lookup"><span data-stu-id="b8a0c-135">ALIASES</span></span>

## <span data-ttu-id="b8a0c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8a0c-136">RELATED LINKS</span></span>

