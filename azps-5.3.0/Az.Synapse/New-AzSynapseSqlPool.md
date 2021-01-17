---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: bb653669ff15dad78ce3cec10f406aa099808e55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383579"
---
# <span data-ttu-id="592e8-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="592e8-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="592e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="592e8-102">SYNOPSIS</span></span>
<span data-ttu-id="592e8-103">Tworzy pulę SQL analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="592e8-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="592e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="592e8-104">SYNTAX</span></span>

### <span data-ttu-id="592e8-105">CreateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="592e8-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="592e8-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="592e8-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="592e8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="592e8-107">DESCRIPTION</span></span>
<span data-ttu-id="592e8-108">Polecenie cmdlet **New-AzSynapseSqlPool** tworzy pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="592e8-108">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="592e8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="592e8-109">EXAMPLES</span></span>

### <span data-ttu-id="592e8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="592e8-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="592e8-111">To polecenie tworzy pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="592e8-111">This command creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="592e8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="592e8-112">PARAMETERS</span></span>

### <span data-ttu-id="592e8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="592e8-113">-AsJob</span></span>
<span data-ttu-id="592e8-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="592e8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="592e8-115">— Sortowanie</span><span class="sxs-lookup"><span data-stu-id="592e8-115">-Collation</span></span>
<span data-ttu-id="592e8-116">Sortowanie definiuje reguły, które sortują i porównują dane, i nie można ich zmieniać po utworzeniu puli SQL.</span><span class="sxs-lookup"><span data-stu-id="592e8-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="592e8-117">Domyślnym sortowaniem jest SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="592e8-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="592e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592e8-118">-DefaultProfile</span></span>
<span data-ttu-id="592e8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="592e8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="592e8-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="592e8-120">-Name</span></span>
<span data-ttu-id="592e8-121">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="592e8-121">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="592e8-122">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="592e8-122">-PerformanceLevel</span></span>
<span data-ttu-id="592e8-123">Warstwa usług SQL i poziom wydajności, które mają zostać przypisane do puli SQL.</span><span class="sxs-lookup"><span data-stu-id="592e8-123">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="592e8-124">Na przykład DW2000c.</span><span class="sxs-lookup"><span data-stu-id="592e8-124">For example, DW2000c.</span></span>

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

### <span data-ttu-id="592e8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="592e8-125">-ResourceGroupName</span></span>
<span data-ttu-id="592e8-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="592e8-126">Resource group name.</span></span>

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

### <span data-ttu-id="592e8-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="592e8-127">-Tag</span></span>
<span data-ttu-id="592e8-128">Ciąg znaków, który jest ciągiem znaczników skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="592e8-128">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="592e8-129">-Version</span><span class="sxs-lookup"><span data-stu-id="592e8-129">-Version</span></span>
<span data-ttu-id="592e8-130">Wersja puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="592e8-130">Version of Synapse SQL pool.</span></span> <span data-ttu-id="592e8-131">Na przykład 2 lub 3.</span><span class="sxs-lookup"><span data-stu-id="592e8-131">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="592e8-132">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="592e8-132">-WorkspaceName</span></span>
<span data-ttu-id="592e8-133">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="592e8-133">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="592e8-134">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="592e8-134">-WorkspaceObject</span></span>
<span data-ttu-id="592e8-135">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="592e8-135">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="592e8-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="592e8-136">-Confirm</span></span>
<span data-ttu-id="592e8-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="592e8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="592e8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="592e8-138">-WhatIf</span></span>
<span data-ttu-id="592e8-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="592e8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="592e8-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="592e8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="592e8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592e8-141">CommonParameters</span></span>
<span data-ttu-id="592e8-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="592e8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592e8-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="592e8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592e8-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="592e8-144">INPUTS</span></span>

### <span data-ttu-id="592e8-145">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="592e8-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="592e8-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="592e8-146">OUTPUTS</span></span>

### <span data-ttu-id="592e8-147">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="592e8-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="592e8-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="592e8-148">NOTES</span></span>

## <span data-ttu-id="592e8-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="592e8-149">RELATED LINKS</span></span>
