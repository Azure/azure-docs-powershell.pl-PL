---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: dea94d89bfd5384d8ec614259a5bb342cd9d186b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015649"
---
# <span data-ttu-id="b94e5-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="b94e5-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="b94e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b94e5-102">SYNOPSIS</span></span>
<span data-ttu-id="b94e5-103">Pobiera ustawienia inspekcji puli sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b94e5-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b94e5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b94e5-104">SYNTAX</span></span>

### <span data-ttu-id="b94e5-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b94e5-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b94e5-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b94e5-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b94e5-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b94e5-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b94e5-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b94e5-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b94e5-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="b94e5-109">DESCRIPTION</span></span>
<span data-ttu-id="b94e5-110">Polecenie **cmdlet Get-AzSynapseSqlPoolAuditSetting** pobiera ustawienia inspekcji puli SQL Synapse Analytics platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b94e5-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b94e5-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b94e5-111">EXAMPLES</span></span>

### <span data-ttu-id="b94e5-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b94e5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="b94e5-113">To polecenie pobiera ustawienia inspekcji puli języka SQL o nazwie ContosoSqlPool w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b94e5-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="b94e5-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b94e5-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="b94e5-115">To polecenie pobiera ustawienia inspekcji puli sql o nazwie ContosoSqlPool w obszarze roboczym ContosoWorkspace za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="b94e5-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="b94e5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b94e5-116">PARAMETERS</span></span>

### <span data-ttu-id="b94e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b94e5-117">-DefaultProfile</span></span>
<span data-ttu-id="b94e5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b94e5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b94e5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b94e5-119">-InputObject</span></span>
<span data-ttu-id="b94e5-120">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="b94e5-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b94e5-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b94e5-121">-Name</span></span>
<span data-ttu-id="b94e5-122">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="b94e5-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="b94e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b94e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="b94e5-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b94e5-124">Resource group name.</span></span>

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

### <span data-ttu-id="b94e5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b94e5-125">-ResourceId</span></span>
<span data-ttu-id="b94e5-126">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="b94e5-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="b94e5-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b94e5-127">-WorkspaceName</span></span>
<span data-ttu-id="b94e5-128">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="b94e5-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b94e5-129">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b94e5-129">-WorkspaceObject</span></span>
<span data-ttu-id="b94e5-130">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="b94e5-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b94e5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b94e5-131">CommonParameters</span></span>
<span data-ttu-id="b94e5-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b94e5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b94e5-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b94e5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b94e5-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b94e5-134">INPUTS</span></span>

### <span data-ttu-id="b94e5-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b94e5-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b94e5-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b94e5-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="b94e5-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b94e5-137">OUTPUTS</span></span>

### <span data-ttu-id="b94e5-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="b94e5-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="b94e5-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b94e5-139">NOTES</span></span>

## <span data-ttu-id="b94e5-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b94e5-140">RELATED LINKS</span></span>
