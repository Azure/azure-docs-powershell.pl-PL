---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: d3ea1a67d8afa15549c19d6099dc727aab43adc5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334069"
---
# <span data-ttu-id="993ba-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="993ba-101">Get-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="993ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="993ba-102">SYNOPSIS</span></span>
<span data-ttu-id="993ba-103">Pobiera informacje o administratorze usługi Azure AD dla obszaru roboczego analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="993ba-103">Gets information about an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="993ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="993ba-104">SYNTAX</span></span>

### <span data-ttu-id="993ba-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="993ba-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="993ba-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="993ba-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="993ba-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="993ba-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="993ba-108">Opis</span><span class="sxs-lookup"><span data-stu-id="993ba-108">DESCRIPTION</span></span>
<span data-ttu-id="993ba-109">Polecenie cmdlet **Get-AzSynapseSqlActiveDirectoryAdministrator** pobiera informacje dotyczące administratora usługi Azure Active Directory (Azure AD) dla obszaru roboczego analiza Azure Synapse w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="993ba-109">The **Get-AzSynapseSqlActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an Azure Synapse Analytics Workspace in the current subscription.</span></span>

## <span data-ttu-id="993ba-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="993ba-110">EXAMPLES</span></span>

### <span data-ttu-id="993ba-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="993ba-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="993ba-112">To polecenie pobiera informacje o administratorze usługi Azure AD dla obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="993ba-112">This command gets information about an Azure AD administrator for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="993ba-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="993ba-113">PARAMETERS</span></span>

### <span data-ttu-id="993ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="993ba-114">-DefaultProfile</span></span>
<span data-ttu-id="993ba-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="993ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="993ba-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="993ba-116">-InputObject</span></span>
<span data-ttu-id="993ba-117">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="993ba-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="993ba-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="993ba-118">-ResourceGroupName</span></span>
<span data-ttu-id="993ba-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="993ba-119">Resource group name.</span></span>

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

### <span data-ttu-id="993ba-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="993ba-120">-ResourceId</span></span>
<span data-ttu-id="993ba-121">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="993ba-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="993ba-122">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="993ba-122">-WorkspaceName</span></span>
<span data-ttu-id="993ba-123">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="993ba-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="993ba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="993ba-124">CommonParameters</span></span>
<span data-ttu-id="993ba-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="993ba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="993ba-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="993ba-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="993ba-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="993ba-127">INPUTS</span></span>

### <span data-ttu-id="993ba-128">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="993ba-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="993ba-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="993ba-129">OUTPUTS</span></span>

### <span data-ttu-id="993ba-130">Microsoft. Azure. Commands. Synapse. models. PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="993ba-130">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="993ba-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="993ba-131">NOTES</span></span>

## <span data-ttu-id="993ba-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="993ba-132">RELATED LINKS</span></span>
