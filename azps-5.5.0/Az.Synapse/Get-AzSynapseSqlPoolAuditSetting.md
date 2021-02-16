---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 592c35a3407bd42846e8c24786716a73d5729c9a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195618"
---
# <span data-ttu-id="2d2d3-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="2d2d3-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="2d2d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d2d3-102">SYNOPSIS</span></span>
<span data-ttu-id="2d2d3-103">Pobiera ustawienia inspekcji puli języka SQL Synapse Analytics platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="2d2d3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2d2d3-104">SYNTAX</span></span>

### <span data-ttu-id="2d2d3-105">GetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="2d2d3-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d2d3-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d2d3-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d2d3-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d2d3-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d2d3-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d2d3-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d2d3-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="2d2d3-109">DESCRIPTION</span></span>
<span data-ttu-id="2d2d3-110">Polecenie **cmdlet Get-AzSynapseSqlPoolAuditSetting** pobiera ustawienia inspekcji puli SQL Synapse Analytics platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="2d2d3-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2d2d3-111">EXAMPLES</span></span>

### <span data-ttu-id="2d2d3-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2d2d3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="2d2d3-113">To polecenie pobiera ustawienia inspekcji puli języka SQL o nazwie ContosoSqlPool w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="2d2d3-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2d2d3-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="2d2d3-115">To polecenie pobiera ustawienia inspekcji puli sql o nazwie ContosoSqlPool w obszarze roboczym ContosoWorkspace za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="2d2d3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d2d3-116">PARAMETERS</span></span>

### <span data-ttu-id="2d2d3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d2d3-117">-DefaultProfile</span></span>
<span data-ttu-id="2d2d3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d2d3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d2d3-119">-InputObject</span></span>
<span data-ttu-id="2d2d3-120">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d2d3-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2d2d3-121">-Name</span></span>
<span data-ttu-id="2d2d3-122">Nazwa puli języka SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d2d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d2d3-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2d3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d2d3-125">-ResourceId</span></span>
<span data-ttu-id="2d2d3-126">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2d3-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2d2d3-127">-WorkspaceName</span></span>
<span data-ttu-id="2d2d3-128">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d2d3-129">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2d2d3-129">-WorkspaceObject</span></span>
<span data-ttu-id="2d2d3-130">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d2d3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d2d3-131">CommonParameters</span></span>
<span data-ttu-id="2d2d3-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d2d3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d2d3-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d2d3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d2d3-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d2d3-134">INPUTS</span></span>

### <span data-ttu-id="2d2d3-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2d2d3-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2d2d3-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="2d2d3-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="2d2d3-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2d2d3-137">OUTPUTS</span></span>

### <span data-ttu-id="2d2d3-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="2d2d3-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="2d2d3-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2d2d3-139">NOTES</span></span>

## <span data-ttu-id="2d2d3-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d2d3-140">RELATED LINKS</span></span>
