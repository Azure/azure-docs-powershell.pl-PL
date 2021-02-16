---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: bb653669ff15dad78ce3cec10f406aa099808e55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182754"
---
# <span data-ttu-id="1490d-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1490d-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="1490d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1490d-102">SYNOPSIS</span></span>
<span data-ttu-id="1490d-103">Tworzy pulę sql analizy Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1490d-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1490d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1490d-104">SYNTAX</span></span>

### <span data-ttu-id="1490d-105">CreateByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1490d-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1490d-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1490d-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1490d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1490d-107">DESCRIPTION</span></span>
<span data-ttu-id="1490d-108">Polecenie **cmdlet New-AzSynapseSqlPool** tworzy pulę sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1490d-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1490d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1490d-109">EXAMPLES</span></span>

### <span data-ttu-id="1490d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1490d-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="1490d-111">To polecenie tworzy pulę sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1490d-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1490d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1490d-112">PARAMETERS</span></span>

### <span data-ttu-id="1490d-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1490d-113">-AsJob</span></span>
<span data-ttu-id="1490d-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1490d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1490d-115">— sortowanie</span><span class="sxs-lookup"><span data-stu-id="1490d-115">-Collation</span></span>
<span data-ttu-id="1490d-116">Sortowanie definiuje reguły sortowania i porównywania danych, których nie można zmienić po utworzeniu puli języka SQL.</span><span class="sxs-lookup"><span data-stu-id="1490d-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="1490d-117">Sortowaniem domyślnym jest SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="1490d-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="1490d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1490d-118">-DefaultProfile</span></span>
<span data-ttu-id="1490d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1490d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1490d-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1490d-120">-Name</span></span>
<span data-ttu-id="1490d-121">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="1490d-121">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1490d-122">- PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="1490d-122">-PerformanceLevel</span></span>
<span data-ttu-id="1490d-123">Warstwa i poziom wydajności usługi SQL, które można przypisać do puli sql.</span><span class="sxs-lookup"><span data-stu-id="1490d-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="1490d-124">Na przykład DW2000c.</span><span class="sxs-lookup"><span data-stu-id="1490d-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="1490d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1490d-125">-ResourceGroupName</span></span>
<span data-ttu-id="1490d-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1490d-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1490d-127">— Tag</span><span class="sxs-lookup"><span data-stu-id="1490d-127">-Tag</span></span>
<span data-ttu-id="1490d-128">A string,string dictionary of tags associated with the resource.</span><span class="sxs-lookup"><span data-stu-id="1490d-128">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1490d-129">— Wersja</span><span class="sxs-lookup"><span data-stu-id="1490d-129">-Version</span></span>
<span data-ttu-id="1490d-130">Wersja puli języka SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="1490d-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="1490d-131">Na przykład 2 lub 3.</span><span class="sxs-lookup"><span data-stu-id="1490d-131">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1490d-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1490d-132">-WorkspaceName</span></span>
<span data-ttu-id="1490d-133">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="1490d-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1490d-134">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1490d-134">-WorkspaceObject</span></span>
<span data-ttu-id="1490d-135">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="1490d-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1490d-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1490d-136">-Confirm</span></span>
<span data-ttu-id="1490d-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1490d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1490d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1490d-138">-WhatIf</span></span>
<span data-ttu-id="1490d-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1490d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1490d-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1490d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1490d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1490d-141">CommonParameters</span></span>
<span data-ttu-id="1490d-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1490d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1490d-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1490d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1490d-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1490d-144">INPUTS</span></span>

### <span data-ttu-id="1490d-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1490d-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1490d-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1490d-146">OUTPUTS</span></span>

### <span data-ttu-id="1490d-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1490d-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="1490d-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1490d-148">NOTES</span></span>

## <span data-ttu-id="1490d-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1490d-149">RELATED LINKS</span></span>
