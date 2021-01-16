---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384008"
---
# <span data-ttu-id="3a7bb-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3a7bb-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="3a7bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="3a7bb-103">Pobiera definicję roli Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="3a7bb-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="3a7bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a7bb-104">SYNTAX</span></span>

### <span data-ttu-id="3a7bb-105">GetByWorkspaceNameAndIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3a7bb-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a7bb-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a7bb-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a7bb-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a7bb-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a7bb-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a7bb-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a7bb-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3a7bb-109">DESCRIPTION</span></span>
<span data-ttu-id="3a7bb-110">Polecenie cmdlet **Get-AzSynapseRoleDefinition** pobiera definicję roli Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="3a7bb-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="3a7bb-111">Jeśli nie określisz nazwy roli lub identyfikatora roli, to polecenie cmdlet otrzyma wszystkie definicje ról.</span><span class="sxs-lookup"><span data-stu-id="3a7bb-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="3a7bb-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a7bb-112">EXAMPLES</span></span>

### <span data-ttu-id="3a7bb-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3a7bb-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="3a7bb-114">To polecenie pobiera wszystkie definicje ról w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="3a7bb-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="3a7bb-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3a7bb-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="3a7bb-116">To polecenie pobiera definicję roli w obszarze roboczym ContosoWorkspace z nazwą ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="3a7bb-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="3a7bb-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3a7bb-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="3a7bb-118">To polecenie pobiera wszystkie definicje ról w obszarze roboczym za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="3a7bb-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="3a7bb-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a7bb-119">PARAMETERS</span></span>

### <span data-ttu-id="3a7bb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a7bb-120">-DefaultProfile</span></span>
<span data-ttu-id="3a7bb-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a7bb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a7bb-122">-ID</span><span class="sxs-lookup"><span data-stu-id="3a7bb-122">-Id</span></span>
<span data-ttu-id="3a7bb-123">Identyfikator roli przypisanej do podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="3a7bb-123">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="3a7bb-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a7bb-124">-Name</span></span>
<span data-ttu-id="3a7bb-125">Nazwa roli przypisanej do podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="3a7bb-125">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="3a7bb-126">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="3a7bb-126">-WorkspaceName</span></span>
<span data-ttu-id="3a7bb-127">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="3a7bb-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3a7bb-128">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="3a7bb-128">-WorkspaceObject</span></span>
<span data-ttu-id="3a7bb-129">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="3a7bb-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3a7bb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a7bb-130">CommonParameters</span></span>
<span data-ttu-id="3a7bb-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a7bb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a7bb-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a7bb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a7bb-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a7bb-133">INPUTS</span></span>

### <span data-ttu-id="3a7bb-134">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3a7bb-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3a7bb-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a7bb-135">OUTPUTS</span></span>

### <span data-ttu-id="3a7bb-136">Microsoft. Azure. Commands. Synapse. models. PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="3a7bb-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="3a7bb-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a7bb-137">NOTES</span></span>

## <span data-ttu-id="3a7bb-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a7bb-138">RELATED LINKS</span></span>
