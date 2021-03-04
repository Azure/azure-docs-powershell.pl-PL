---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 1f5c9c619c037c243246f9dec26ae2504a162d9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015722"
---
# <span data-ttu-id="42176-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="42176-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="42176-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42176-102">SYNOPSIS</span></span>
<span data-ttu-id="42176-103">Pobiera informacje o administratorze usługi Azure AD dla obszaru roboczego analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="42176-103">Gets information about an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="42176-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="42176-104">SYNTAX</span></span>

### <span data-ttu-id="42176-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="42176-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42176-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42176-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42176-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42176-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42176-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="42176-108">DESCRIPTION</span></span>
<span data-ttu-id="42176-109">Polecenie cmdlet **Get-AzSynapseSqlActiveDirectoryAdministrator** pobiera informacje o administratorze usługi Azure Active Directory (Azure AD) dla obszaru roboczego analizy Synapse Analytics Azure w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="42176-109">The **Get-AzSynapseSqlActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an Azure Synapse Analytics Workspace in the current subscription.</span></span>

## <span data-ttu-id="42176-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="42176-110">EXAMPLES</span></span>

### <span data-ttu-id="42176-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="42176-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="42176-112">To polecenie pobiera informacje o administratorze usługi Azure AD dla obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="42176-112">This command gets information about an Azure AD administrator for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="42176-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42176-113">PARAMETERS</span></span>

### <span data-ttu-id="42176-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42176-114">-DefaultProfile</span></span>
<span data-ttu-id="42176-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="42176-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42176-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42176-116">-InputObject</span></span>
<span data-ttu-id="42176-117">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="42176-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="42176-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42176-118">-ResourceGroupName</span></span>
<span data-ttu-id="42176-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="42176-119">Resource group name.</span></span>

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

### <span data-ttu-id="42176-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42176-120">-ResourceId</span></span>
<span data-ttu-id="42176-121">Identyfikator zasobu obszaru roboczego programu Synapse.</span><span class="sxs-lookup"><span data-stu-id="42176-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="42176-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="42176-122">-WorkspaceName</span></span>
<span data-ttu-id="42176-123">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="42176-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="42176-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42176-124">CommonParameters</span></span>
<span data-ttu-id="42176-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42176-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42176-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42176-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42176-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42176-127">INPUTS</span></span>

### <span data-ttu-id="42176-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="42176-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="42176-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42176-129">OUTPUTS</span></span>

### <span data-ttu-id="42176-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="42176-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="42176-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="42176-131">NOTES</span></span>

## <span data-ttu-id="42176-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42176-132">RELATED LINKS</span></span>
