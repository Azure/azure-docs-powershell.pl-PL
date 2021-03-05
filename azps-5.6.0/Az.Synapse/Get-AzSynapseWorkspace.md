---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: 25107456afbf85aa41dd0be600a20f7a5fcbb640
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970106"
---
# <span data-ttu-id="5d7cb-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5d7cb-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="5d7cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d7cb-102">SYNOPSIS</span></span>
<span data-ttu-id="5d7cb-103">Pobiera obszar roboczy analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="5d7cb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5d7cb-104">SYNTAX</span></span>

### <span data-ttu-id="5d7cb-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5d7cb-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d7cb-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d7cb-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d7cb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5d7cb-107">DESCRIPTION</span></span>
<span data-ttu-id="5d7cb-108">Polecenie **cmdlet Get-AzSynapseWorkspace** pobiera informacje o obszarze roboczym usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="5d7cb-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5d7cb-109">EXAMPLES</span></span>

### <span data-ttu-id="5d7cb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5d7cb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="5d7cb-111">To polecenie pobiera wszystkie obszary robocze usługi Azure Synapse Analytics w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="5d7cb-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5d7cb-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="5d7cb-113">To polecenie pobiera wszystkie obszary robocze usługi Azure Synapse Analytics w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="5d7cb-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="5d7cb-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="5d7cb-115">To polecenie pobiera obszar roboczy usługi Azure Synapse Analytics o określonej nazwie.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="5d7cb-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="5d7cb-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="5d7cb-117">To polecenie pobiera obszar roboczy usługi Azure Synapse Analytics z określonym identyfikatorem zasobu.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="5d7cb-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d7cb-118">PARAMETERS</span></span>

### <span data-ttu-id="5d7cb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d7cb-119">-DefaultProfile</span></span>
<span data-ttu-id="5d7cb-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d7cb-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5d7cb-121">-Name</span></span>
<span data-ttu-id="5d7cb-122">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-122">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d7cb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d7cb-123">-ResourceGroupName</span></span>
<span data-ttu-id="5d7cb-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-124">Resource group name.</span></span>

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

### <span data-ttu-id="5d7cb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d7cb-125">-ResourceId</span></span>
<span data-ttu-id="5d7cb-126">Identyfikator zasobu obszaru roboczego programu Synapse.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="5d7cb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d7cb-127">CommonParameters</span></span>
<span data-ttu-id="5d7cb-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d7cb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d7cb-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d7cb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d7cb-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d7cb-130">INPUTS</span></span>

### <span data-ttu-id="5d7cb-131">Brak</span><span class="sxs-lookup"><span data-stu-id="5d7cb-131">None</span></span>

## <span data-ttu-id="5d7cb-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d7cb-132">OUTPUTS</span></span>

### <span data-ttu-id="5d7cb-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5d7cb-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5d7cb-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5d7cb-134">NOTES</span></span>

## <span data-ttu-id="5d7cb-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d7cb-135">RELATED LINKS</span></span>
