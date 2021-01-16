---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 574c41fe8b0f3266a6fff80c020b60c9832cb431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356517"
---
# <span data-ttu-id="03fd4-101">New-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="03fd4-101">New-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="03fd4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03fd4-102">SYNOPSIS</span></span>
<span data-ttu-id="03fd4-103">Tworzy nowy punkt przywracania w puli SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="03fd4-103">Creates a new restore point in an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="03fd4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03fd4-104">SYNTAX</span></span>

### <span data-ttu-id="03fd4-105">CreateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="03fd4-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03fd4-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03fd4-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03fd4-107">CreateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03fd4-107">CreateByInputObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03fd4-108">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03fd4-108">CreateByResourceIdParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03fd4-109">Opis</span><span class="sxs-lookup"><span data-stu-id="03fd4-109">DESCRIPTION</span></span>
<span data-ttu-id="03fd4-110">Polecenie cmdlet **New-AzSynapseSqlPoolRestorePoint** tworzy nowy punkt przywracania, z którego można przywrócić pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="03fd4-110">The **New-AzSynapseSqlPoolRestorePoint** cmdlet creates a new restore point that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="03fd4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03fd4-111">EXAMPLES</span></span>

### <span data-ttu-id="03fd4-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="03fd4-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

<span data-ttu-id="03fd4-113">To polecenie tworzy punkt przywracania dla puli SQL o nazwie ContosoSqlPool w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="03fd4-113">This command creates a restore point for SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="03fd4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03fd4-114">PARAMETERS</span></span>

### <span data-ttu-id="03fd4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03fd4-115">-AsJob</span></span>
<span data-ttu-id="03fd4-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="03fd4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03fd4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03fd4-117">-DefaultProfile</span></span>
<span data-ttu-id="03fd4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03fd4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03fd4-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="03fd4-119">-InputObject</span></span>
<span data-ttu-id="03fd4-120">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="03fd4-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03fd4-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03fd4-121">-Name</span></span>
<span data-ttu-id="03fd4-122">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="03fd4-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fd4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03fd4-123">-ResourceGroupName</span></span>
<span data-ttu-id="03fd4-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="03fd4-124">Resource group name.</span></span>

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

### <span data-ttu-id="03fd4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03fd4-125">-ResourceId</span></span>
<span data-ttu-id="03fd4-126">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="03fd4-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fd4-127">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="03fd4-127">-RestorePointLabel</span></span>
<span data-ttu-id="03fd4-128">Etykieta, z którą jest skojarzony punkt przywracania, nie może być unikatowa.</span><span class="sxs-lookup"><span data-stu-id="03fd4-128">The label we associate a restore point with, may not be unique.</span></span>

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

### <span data-ttu-id="03fd4-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="03fd4-129">-WorkspaceName</span></span>
<span data-ttu-id="03fd4-130">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="03fd4-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="03fd4-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="03fd4-131">-WorkspaceObject</span></span>
<span data-ttu-id="03fd4-132">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="03fd4-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="03fd4-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03fd4-133">-Confirm</span></span>
<span data-ttu-id="03fd4-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03fd4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03fd4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03fd4-135">-WhatIf</span></span>
<span data-ttu-id="03fd4-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03fd4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03fd4-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="03fd4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03fd4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03fd4-138">CommonParameters</span></span>
<span data-ttu-id="03fd4-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03fd4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03fd4-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03fd4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03fd4-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03fd4-141">INPUTS</span></span>

### <span data-ttu-id="03fd4-142">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="03fd4-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="03fd4-143">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="03fd4-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="03fd4-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03fd4-144">OUTPUTS</span></span>

### <span data-ttu-id="03fd4-145">Microsoft. Azure. Commands. Synapse. models. PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="03fd4-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

## <span data-ttu-id="03fd4-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03fd4-146">NOTES</span></span>

## <span data-ttu-id="03fd4-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03fd4-147">RELATED LINKS</span></span>
