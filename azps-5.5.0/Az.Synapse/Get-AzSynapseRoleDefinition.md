---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241739"
---
# <span data-ttu-id="ab8b1-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ab8b1-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="ab8b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab8b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ab8b1-103">Pobiera definicję ról analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="ab8b1-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="ab8b1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ab8b1-104">SYNTAX</span></span>

### <span data-ttu-id="ab8b1-105">GetByWorkspaceNameAndIdParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ab8b1-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab8b1-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab8b1-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab8b1-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab8b1-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab8b1-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab8b1-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab8b1-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="ab8b1-109">DESCRIPTION</span></span>
<span data-ttu-id="ab8b1-110">Polecenie **cmdlet Get-AzSynapseRoleDefinition** pobiera definicję ról analizy Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="ab8b1-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="ab8b1-111">Jeśli nie określisz nazwy roli ani identyfikatora roli, to polecenie cmdlet pobiera wszystkie definicje ról.</span><span class="sxs-lookup"><span data-stu-id="ab8b1-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="ab8b1-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ab8b1-112">EXAMPLES</span></span>

### <span data-ttu-id="ab8b1-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ab8b1-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="ab8b1-114">To polecenie pobiera wszystkie definicje ról w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="ab8b1-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="ab8b1-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ab8b1-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="ab8b1-116">To polecenie pobiera definicję roli w obszarze obszaru roboczego ContosoWorkspace o nazwie ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="ab8b1-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="ab8b1-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ab8b1-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="ab8b1-118">To polecenie pobiera wszystkie definicje ról w obszarze roboczym za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="ab8b1-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="ab8b1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab8b1-119">PARAMETERS</span></span>

### <span data-ttu-id="ab8b1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab8b1-120">-DefaultProfile</span></span>
<span data-ttu-id="ab8b1-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab8b1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab8b1-122">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="ab8b1-122">-Id</span></span>
<span data-ttu-id="ab8b1-123">Identyfikator roli przypisanej do podmiotu głównego.</span><span class="sxs-lookup"><span data-stu-id="ab8b1-123">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8b1-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ab8b1-124">-Name</span></span>
<span data-ttu-id="ab8b1-125">Nazwa roli przypisanej do podmiotu głównego.</span><span class="sxs-lookup"><span data-stu-id="ab8b1-125">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8b1-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ab8b1-126">-WorkspaceName</span></span>
<span data-ttu-id="ab8b1-127">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="ab8b1-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8b1-128">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ab8b1-128">-WorkspaceObject</span></span>
<span data-ttu-id="ab8b1-129">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="ab8b1-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8b1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8b1-130">CommonParameters</span></span>
<span data-ttu-id="ab8b1-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab8b1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8b1-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab8b1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8b1-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab8b1-133">INPUTS</span></span>

### <span data-ttu-id="ab8b1-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ab8b1-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ab8b1-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab8b1-135">OUTPUTS</span></span>

### <span data-ttu-id="ab8b1-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="ab8b1-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="ab8b1-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ab8b1-137">NOTES</span></span>

## <span data-ttu-id="ab8b1-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab8b1-138">RELATED LINKS</span></span>
