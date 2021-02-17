---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ab1a8f9b91f8a47f5c6b97b537489c65a53e146e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241715"
---
# <span data-ttu-id="f3db7-101">Get-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="f3db7-101">Get-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="f3db7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3db7-102">SYNOPSIS</span></span>
<span data-ttu-id="f3db7-103">Pobiera ustawienia inspekcji w obszarze roboczym analizy Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f3db7-103">Gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="f3db7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f3db7-104">SYNTAX</span></span>

### <span data-ttu-id="f3db7-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f3db7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3db7-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3db7-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3db7-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3db7-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3db7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f3db7-108">DESCRIPTION</span></span>
<span data-ttu-id="f3db7-109">Polecenie **cmdlet Get-AzSynapseSqlAuditSetting** pobiera ustawienia inspekcji obszaru roboczego usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f3db7-109">The **Get-AzSynapseSqlAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="f3db7-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f3db7-110">EXAMPLES</span></span>

### <span data-ttu-id="f3db7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f3db7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="f3db7-112">Pobiera ustawienia inspekcji obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f3db7-112">Gets the auditing settings of a workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="f3db7-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f3db7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAuditSetting
```

<span data-ttu-id="f3db7-114">Pobiera ustawienia inspekcji obszaru roboczego o nazwie ContosoWorkspace przez potok.</span><span class="sxs-lookup"><span data-stu-id="f3db7-114">Gets the auditing settings of a workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="f3db7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3db7-115">PARAMETERS</span></span>

### <span data-ttu-id="f3db7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3db7-116">-DefaultProfile</span></span>
<span data-ttu-id="f3db7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3db7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3db7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3db7-118">-InputObject</span></span>
<span data-ttu-id="f3db7-119">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="f3db7-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3db7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3db7-120">-ResourceGroupName</span></span>
<span data-ttu-id="f3db7-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f3db7-121">Resource group name.</span></span>

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

### <span data-ttu-id="f3db7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3db7-122">-ResourceId</span></span>
<span data-ttu-id="f3db7-123">Identyfikator zasobu obszaru roboczego programu Synapse.</span><span class="sxs-lookup"><span data-stu-id="f3db7-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="f3db7-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f3db7-124">-WorkspaceName</span></span>
<span data-ttu-id="f3db7-125">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="f3db7-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f3db7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3db7-126">CommonParameters</span></span>
<span data-ttu-id="f3db7-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3db7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3db7-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3db7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3db7-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3db7-129">INPUTS</span></span>

### <span data-ttu-id="f3db7-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f3db7-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f3db7-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3db7-131">OUTPUTS</span></span>

### <span data-ttu-id="f3db7-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="f3db7-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="f3db7-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f3db7-133">NOTES</span></span>

## <span data-ttu-id="f3db7-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3db7-134">RELATED LINKS</span></span>
