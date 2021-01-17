---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 574c41fe8b0f3266a6fff80c020b60c9832cb431
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383565"
---
# <span data-ttu-id="8a8b4-101">New-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="8a8b4-101">New-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="8a8b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="8a8b4-103">Tworzy nowy punkt przywracania w puli SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-103">Creates a new restore point in an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="8a8b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a8b4-104">SYNTAX</span></span>

### <span data-ttu-id="8a8b4-105">CreateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8a8b4-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a8b4-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a8b4-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a8b4-107">CreateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a8b4-107">CreateByInputObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a8b4-108">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a8b4-108">CreateByResourceIdParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a8b4-109">Opis</span><span class="sxs-lookup"><span data-stu-id="8a8b4-109">DESCRIPTION</span></span>
<span data-ttu-id="8a8b4-110">Polecenie cmdlet **New-AzSynapseSqlPoolRestorePoint** tworzy nowy punkt przywracania, z którego można przywrócić pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-110">The **New-AzSynapseSqlPoolRestorePoint** cmdlet creates a new restore point that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="8a8b4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a8b4-111">EXAMPLES</span></span>

### <span data-ttu-id="8a8b4-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8a8b4-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

<span data-ttu-id="8a8b4-113">To polecenie tworzy punkt przywracania dla puli SQL o nazwie ContosoSqlPool w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-113">This command creates a restore point for SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="8a8b4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a8b4-114">PARAMETERS</span></span>

### <span data-ttu-id="8a8b4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a8b4-115">-AsJob</span></span>
<span data-ttu-id="8a8b4-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8a8b4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a8b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a8b4-117">-DefaultProfile</span></span>
<span data-ttu-id="8a8b4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a8b4-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8a8b4-119">-InputObject</span></span>
<span data-ttu-id="8a8b4-120">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8a8b4-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8a8b4-121">-Name</span></span>
<span data-ttu-id="8a8b4-122">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="8a8b4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a8b4-123">-ResourceGroupName</span></span>
<span data-ttu-id="8a8b4-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-124">Resource group name.</span></span>

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

### <span data-ttu-id="8a8b4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a8b4-125">-ResourceId</span></span>
<span data-ttu-id="8a8b4-126">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="8a8b4-127">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="8a8b4-127">-RestorePointLabel</span></span>
<span data-ttu-id="8a8b4-128">Etykieta, z którą jest skojarzony punkt przywracania, nie może być unikatowa.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-128">The label we associate a restore point with, may not be unique.</span></span>

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

### <span data-ttu-id="8a8b4-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="8a8b4-129">-WorkspaceName</span></span>
<span data-ttu-id="8a8b4-130">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8a8b4-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="8a8b4-131">-WorkspaceObject</span></span>
<span data-ttu-id="8a8b4-132">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8a8b4-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8a8b4-133">-Confirm</span></span>
<span data-ttu-id="8a8b4-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a8b4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a8b4-135">-WhatIf</span></span>
<span data-ttu-id="8a8b4-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a8b4-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a8b4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a8b4-138">CommonParameters</span></span>
<span data-ttu-id="8a8b4-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a8b4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a8b4-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a8b4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a8b4-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a8b4-141">INPUTS</span></span>

### <span data-ttu-id="8a8b4-142">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8a8b4-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8a8b4-143">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8a8b4-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="8a8b4-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a8b4-144">OUTPUTS</span></span>

### <span data-ttu-id="8a8b4-145">Microsoft. Azure. Commands. Synapse. models. PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="8a8b4-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

## <span data-ttu-id="8a8b4-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a8b4-146">NOTES</span></span>

## <span data-ttu-id="8a8b4-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a8b4-147">RELATED LINKS</span></span>
