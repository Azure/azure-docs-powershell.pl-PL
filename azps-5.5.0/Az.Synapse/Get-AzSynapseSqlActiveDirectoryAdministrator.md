---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: d3ea1a67d8afa15549c19d6099dc727aab43adc5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197371"
---
# <span data-ttu-id="2c8da-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="2c8da-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="2c8da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c8da-102">SYNOPSIS</span></span>
<span data-ttu-id="2c8da-103">Pobiera informacje o administratorze usługi Azure AD dla obszaru roboczego analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="2c8da-103">Gets information about an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="2c8da-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2c8da-104">SYNTAX</span></span>

### <span data-ttu-id="2c8da-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="2c8da-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c8da-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c8da-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c8da-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c8da-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c8da-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="2c8da-108">DESCRIPTION</span></span>
<span data-ttu-id="2c8da-109">Polecenie cmdlet **Get-AzSynapseSqlActiveDirectoryAdministrator** pobiera informacje o administratorze usługi Azure Active Directory (Azure AD) dla obszaru roboczego analizy Azure Synapse Analytics w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2c8da-109">The **Get-AzSynapseSqlActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an Azure Synapse Analytics Workspace in the current subscription.</span></span>

## <span data-ttu-id="2c8da-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2c8da-110">EXAMPLES</span></span>

### <span data-ttu-id="2c8da-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2c8da-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="2c8da-112">To polecenie pobiera informacje o administratorze usługi Azure AD dla obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="2c8da-112">This command gets information about an Azure AD administrator for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="2c8da-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c8da-113">PARAMETERS</span></span>

### <span data-ttu-id="2c8da-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c8da-114">-DefaultProfile</span></span>
<span data-ttu-id="2c8da-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c8da-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c8da-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c8da-116">-InputObject</span></span>
<span data-ttu-id="2c8da-117">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="2c8da-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2c8da-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c8da-118">-ResourceGroupName</span></span>
<span data-ttu-id="2c8da-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2c8da-119">Resource group name.</span></span>

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

### <span data-ttu-id="2c8da-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c8da-120">-ResourceId</span></span>
<span data-ttu-id="2c8da-121">Identyfikator zasobu obszaru roboczego programu Synapse.</span><span class="sxs-lookup"><span data-stu-id="2c8da-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="2c8da-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2c8da-122">-WorkspaceName</span></span>
<span data-ttu-id="2c8da-123">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="2c8da-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2c8da-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c8da-124">CommonParameters</span></span>
<span data-ttu-id="2c8da-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c8da-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c8da-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c8da-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c8da-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c8da-127">INPUTS</span></span>

### <span data-ttu-id="2c8da-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2c8da-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2c8da-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2c8da-129">OUTPUTS</span></span>

### <span data-ttu-id="2c8da-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="2c8da-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="2c8da-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2c8da-131">NOTES</span></span>

## <span data-ttu-id="2c8da-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c8da-132">RELATED LINKS</span></span>
