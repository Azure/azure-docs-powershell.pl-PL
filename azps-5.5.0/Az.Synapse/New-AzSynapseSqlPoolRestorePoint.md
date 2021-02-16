---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 574c41fe8b0f3266a6fff80c020b60c9832cb431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182738"
---
# <span data-ttu-id="daeef-101">New-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="daeef-101">New-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="daeef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daeef-102">SYNOPSIS</span></span>
<span data-ttu-id="daeef-103">Tworzy nowy punkt przywracania w puli sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="daeef-103">Creates a new restore point in an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="daeef-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="daeef-104">SYNTAX</span></span>

### <span data-ttu-id="daeef-105">CreateByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="daeef-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="daeef-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="daeef-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="daeef-107">CreateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="daeef-107">CreateByInputObjectParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daeef-108">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="daeef-108">CreateByResourceIdParameterSet</span></span>
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daeef-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="daeef-109">DESCRIPTION</span></span>
<span data-ttu-id="daeef-110">Polecenie cmdlet **New-AzSynapseSqlPoolRestorePoint** tworzy nowy punkt przywracania, z którym można przywrócić pulę sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="daeef-110">The **New-AzSynapseSqlPoolRestorePoint** cmdlet creates a new restore point that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="daeef-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="daeef-111">EXAMPLES</span></span>

### <span data-ttu-id="daeef-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="daeef-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

<span data-ttu-id="daeef-113">To polecenie tworzy punkt przywracania puli sql o nazwie ContosoSqlPool w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="daeef-113">This command creates a restore point for SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="daeef-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="daeef-114">PARAMETERS</span></span>

### <span data-ttu-id="daeef-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="daeef-115">-AsJob</span></span>
<span data-ttu-id="daeef-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="daeef-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="daeef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daeef-117">-DefaultProfile</span></span>
<span data-ttu-id="daeef-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="daeef-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daeef-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="daeef-119">-InputObject</span></span>
<span data-ttu-id="daeef-120">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="daeef-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="daeef-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="daeef-121">-Name</span></span>
<span data-ttu-id="daeef-122">Nazwa puli języka SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="daeef-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="daeef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daeef-123">-ResourceGroupName</span></span>
<span data-ttu-id="daeef-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="daeef-124">Resource group name.</span></span>

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

### <span data-ttu-id="daeef-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="daeef-125">-ResourceId</span></span>
<span data-ttu-id="daeef-126">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="daeef-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="daeef-127">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="daeef-127">-RestorePointLabel</span></span>
<span data-ttu-id="daeef-128">Etykieta, z którym skojarzymy punkt przywracania, może nie być unikatowa.</span><span class="sxs-lookup"><span data-stu-id="daeef-128">The label we associate a restore point with, may not be unique.</span></span>

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

### <span data-ttu-id="daeef-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="daeef-129">-WorkspaceName</span></span>
<span data-ttu-id="daeef-130">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="daeef-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="daeef-131">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="daeef-131">-WorkspaceObject</span></span>
<span data-ttu-id="daeef-132">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="daeef-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="daeef-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="daeef-133">-Confirm</span></span>
<span data-ttu-id="daeef-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="daeef-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daeef-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daeef-135">-WhatIf</span></span>
<span data-ttu-id="daeef-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daeef-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daeef-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="daeef-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daeef-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daeef-138">CommonParameters</span></span>
<span data-ttu-id="daeef-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daeef-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daeef-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="daeef-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daeef-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="daeef-141">INPUTS</span></span>

### <span data-ttu-id="daeef-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="daeef-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="daeef-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="daeef-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="daeef-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="daeef-144">OUTPUTS</span></span>

### <span data-ttu-id="daeef-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="daeef-145">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

## <span data-ttu-id="daeef-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="daeef-146">NOTES</span></span>

## <span data-ttu-id="daeef-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="daeef-147">RELATED LINKS</span></span>
