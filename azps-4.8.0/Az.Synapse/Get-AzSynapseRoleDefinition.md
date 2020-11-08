---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219692"
---
# <span data-ttu-id="f7cb5-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f7cb5-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="f7cb5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="f7cb5-103">Pobiera definicję roli Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="f7cb5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7cb5-104">SYNTAX</span></span>

### <span data-ttu-id="f7cb5-105">GetByWorkspaceNameAndIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f7cb5-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7cb5-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7cb5-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7cb5-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7cb5-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7cb5-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7cb5-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7cb5-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f7cb5-109">DESCRIPTION</span></span>
<span data-ttu-id="f7cb5-110">Polecenie cmdlet **Get-AzSynapseRoleDefinition** pobiera definicję roli Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="f7cb5-111">Jeśli nie określisz nazwy roli lub identyfikatora roli, to polecenie cmdlet otrzyma wszystkie definicje ról.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="f7cb5-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7cb5-112">EXAMPLES</span></span>

### <span data-ttu-id="f7cb5-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f7cb5-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="f7cb5-114">To polecenie pobiera wszystkie definicje ról w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="f7cb5-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f7cb5-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="f7cb5-116">To polecenie pobiera definicję roli w obszarze roboczym ContosoWorkspace z nazwą ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="f7cb5-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f7cb5-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="f7cb5-118">To polecenie pobiera wszystkie definicje ról w obszarze roboczym za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="f7cb5-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7cb5-119">PARAMETERS</span></span>

### <span data-ttu-id="f7cb5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7cb5-120">-DefaultProfile</span></span>
<span data-ttu-id="f7cb5-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7cb5-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f7cb5-122">-Id</span></span>
<span data-ttu-id="f7cb5-123">Identyfikator roli przypisanej do podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-123">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="f7cb5-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f7cb5-124">-Name</span></span>
<span data-ttu-id="f7cb5-125">Nazwa roli przypisanej do podmiotu zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-125">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="f7cb5-126">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="f7cb5-126">-WorkspaceName</span></span>
<span data-ttu-id="f7cb5-127">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f7cb5-128">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="f7cb5-128">-WorkspaceObject</span></span>
<span data-ttu-id="f7cb5-129">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f7cb5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7cb5-130">CommonParameters</span></span>
<span data-ttu-id="f7cb5-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7cb5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7cb5-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7cb5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7cb5-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7cb5-133">INPUTS</span></span>

### <span data-ttu-id="f7cb5-134">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f7cb5-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f7cb5-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7cb5-135">OUTPUTS</span></span>

### <span data-ttu-id="f7cb5-136">Microsoft. Azure. Commands. Synapse. models. PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="f7cb5-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="f7cb5-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7cb5-137">NOTES</span></span>

## <span data-ttu-id="f7cb5-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7cb5-138">RELATED LINKS</span></span>
