---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: f9f921368f55b5901657ca4e366927a284302745
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241707"
---
# <span data-ttu-id="7e11c-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="7e11c-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="7e11c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e11c-102">SYNOPSIS</span></span>
<span data-ttu-id="7e11c-103">Pobiera odrębne punkty przywracania, z których można przywrócić pulę sql Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7e11c-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="7e11c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7e11c-104">SYNTAX</span></span>

### <span data-ttu-id="7e11c-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7e11c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e11c-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e11c-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e11c-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e11c-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e11c-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e11c-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e11c-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="7e11c-109">DESCRIPTION</span></span>
<span data-ttu-id="7e11c-110">Polecenie **cmdlet Get-AzSynapseSqlPoolRestorePoint** pobiera odrębne punkty przywracania, z których można przywrócić pulę sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7e11c-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="7e11c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7e11c-111">EXAMPLES</span></span>

### <span data-ttu-id="7e11c-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7e11c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="7e11c-113">To polecenie zwraca wszystkie dostępne punkty przywracania dla puli języka SQL Azure Synapse Analytics o nazwie ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="7e11c-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="7e11c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e11c-114">PARAMETERS</span></span>

### <span data-ttu-id="7e11c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e11c-115">-DefaultProfile</span></span>
<span data-ttu-id="7e11c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e11c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e11c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e11c-117">-InputObject</span></span>
<span data-ttu-id="7e11c-118">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="7e11c-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7e11c-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7e11c-119">-Name</span></span>
<span data-ttu-id="7e11c-120">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="7e11c-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="7e11c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e11c-121">-ResourceGroupName</span></span>
<span data-ttu-id="7e11c-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7e11c-122">Resource group name.</span></span>

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

### <span data-ttu-id="7e11c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e11c-123">-ResourceId</span></span>
<span data-ttu-id="7e11c-124">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="7e11c-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="7e11c-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7e11c-125">-WorkspaceName</span></span>
<span data-ttu-id="7e11c-126">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="7e11c-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7e11c-127">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7e11c-127">-WorkspaceObject</span></span>
<span data-ttu-id="7e11c-128">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="7e11c-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7e11c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e11c-129">CommonParameters</span></span>
<span data-ttu-id="7e11c-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e11c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e11c-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e11c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e11c-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e11c-132">INPUTS</span></span>

### <span data-ttu-id="7e11c-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7e11c-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7e11c-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7e11c-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7e11c-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7e11c-135">OUTPUTS</span></span>

### <span data-ttu-id="7e11c-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span><span class="sxs-lookup"><span data-stu-id="7e11c-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="7e11c-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7e11c-137">NOTES</span></span>

## <span data-ttu-id="7e11c-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e11c-138">RELATED LINKS</span></span>
