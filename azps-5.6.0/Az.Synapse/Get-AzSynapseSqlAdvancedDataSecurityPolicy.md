---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqladvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 47800968fec9a12255bae01499618f9928416648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015713"
---
# <span data-ttu-id="a77c1-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="a77c1-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="a77c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a77c1-102">SYNOPSIS</span></span>
<span data-ttu-id="a77c1-103">Pobiera zaawansowane zasady zabezpieczeń danych obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a77c1-103">Gets Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="a77c1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a77c1-104">SYNTAX</span></span>

### <span data-ttu-id="a77c1-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a77c1-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a77c1-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a77c1-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a77c1-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a77c1-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a77c1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a77c1-108">DESCRIPTION</span></span>
<span data-ttu-id="a77c1-109">Polecenie **cmdlet Get-AzSynapseSqlAdvancedDataSecurityPolicy** pobiera zasady advanced data security obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a77c1-109">The **Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="a77c1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a77c1-110">EXAMPLES</span></span>

### <span data-ttu-id="a77c1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a77c1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedDataSecurityPolicy -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a77c1-112">To polecenie pobiera zaawansowane zabezpieczenia danych w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a77c1-112">This command gets Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a77c1-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a77c1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAdvancedDataSecurityPolicy
```

<span data-ttu-id="a77c1-114">To polecenie pobiera za pośrednictwem potoku zaawansowane zabezpieczenia danych w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a77c1-114">This command gets Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a77c1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a77c1-115">PARAMETERS</span></span>

### <span data-ttu-id="a77c1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a77c1-116">-DefaultProfile</span></span>
<span data-ttu-id="a77c1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a77c1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a77c1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a77c1-118">-InputObject</span></span>
<span data-ttu-id="a77c1-119">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="a77c1-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a77c1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a77c1-120">-ResourceGroupName</span></span>
<span data-ttu-id="a77c1-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a77c1-121">Resource group name.</span></span>

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

### <span data-ttu-id="a77c1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a77c1-122">-ResourceId</span></span>
<span data-ttu-id="a77c1-123">Identyfikator zasobu obszaru roboczego programu Synapse.</span><span class="sxs-lookup"><span data-stu-id="a77c1-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="a77c1-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a77c1-124">-WorkspaceName</span></span>
<span data-ttu-id="a77c1-125">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="a77c1-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a77c1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a77c1-126">CommonParameters</span></span>
<span data-ttu-id="a77c1-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a77c1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a77c1-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a77c1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a77c1-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a77c1-129">INPUTS</span></span>

### <span data-ttu-id="a77c1-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a77c1-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a77c1-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a77c1-131">OUTPUTS</span></span>

### <span data-ttu-id="a77c1-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="a77c1-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="a77c1-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a77c1-133">NOTES</span></span>

## <span data-ttu-id="a77c1-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a77c1-134">RELATED LINKS</span></span>
