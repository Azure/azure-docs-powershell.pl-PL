---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8c17825dca186f4edf856a2de2ef76082253c39e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241731"
---
# <span data-ttu-id="675cd-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="675cd-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="675cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="675cd-102">SYNOPSIS</span></span>
<span data-ttu-id="675cd-103">Pobiera zaawansowane ustawienia ochrony przed zagrożeniami dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="675cd-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="675cd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="675cd-104">SYNTAX</span></span>

### <span data-ttu-id="675cd-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="675cd-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="675cd-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="675cd-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="675cd-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="675cd-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="675cd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="675cd-108">DESCRIPTION</span></span>
<span data-ttu-id="675cd-109">Polecenie **cmdlet Get-AzSynapseSqlAdvancedThreatProtectionSetting** pobiera zaawansowane ustawienia ochrony przed zagrożeniami w obszarze roboczym usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="675cd-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="675cd-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="675cd-110">EXAMPLES</span></span>

### <span data-ttu-id="675cd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="675cd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="675cd-112">To polecenie pobiera zaawansowane ustawienia ochrony przed zagrożeniami dla obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="675cd-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="675cd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="675cd-113">PARAMETERS</span></span>

### <span data-ttu-id="675cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="675cd-114">-DefaultProfile</span></span>
<span data-ttu-id="675cd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="675cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="675cd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="675cd-116">-InputObject</span></span>
<span data-ttu-id="675cd-117">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="675cd-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="675cd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="675cd-118">-ResourceGroupName</span></span>
<span data-ttu-id="675cd-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="675cd-119">Resource group name.</span></span>

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

### <span data-ttu-id="675cd-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="675cd-120">-ResourceId</span></span>
<span data-ttu-id="675cd-121">Identyfikator zasobu obszaru roboczego programu Synapse.</span><span class="sxs-lookup"><span data-stu-id="675cd-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="675cd-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="675cd-122">-WorkspaceName</span></span>
<span data-ttu-id="675cd-123">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="675cd-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="675cd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="675cd-124">CommonParameters</span></span>
<span data-ttu-id="675cd-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="675cd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="675cd-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="675cd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="675cd-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="675cd-127">INPUTS</span></span>

### <span data-ttu-id="675cd-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="675cd-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="675cd-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="675cd-129">OUTPUTS</span></span>

### <span data-ttu-id="675cd-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="675cd-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="675cd-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="675cd-131">NOTES</span></span>

## <span data-ttu-id="675cd-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="675cd-132">RELATED LINKS</span></span>
