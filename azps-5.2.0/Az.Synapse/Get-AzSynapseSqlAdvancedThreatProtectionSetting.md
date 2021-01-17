---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 8c17825dca186f4edf856a2de2ef76082253c39e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359438"
---
# <span data-ttu-id="21fa2-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="21fa2-101">Get-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="21fa2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="21fa2-103">Pobiera zaawansowane ustawienia ochrony przed zagrożeniami dla obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="21fa2-103">Gets the advanced threat protection settings for a workspace.</span></span>

## <span data-ttu-id="21fa2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21fa2-104">SYNTAX</span></span>

### <span data-ttu-id="21fa2-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="21fa2-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21fa2-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21fa2-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21fa2-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21fa2-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21fa2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="21fa2-108">DESCRIPTION</span></span>
<span data-ttu-id="21fa2-109">Polecenie cmdlet **Get-AzSynapseSqlAdvancedThreatProtectionSetting** pobiera zaawansowane ustawienia ochrony przed zagrożeniami w obszarze roboczym funkcji Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="21fa2-109">The **Get-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="21fa2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21fa2-110">EXAMPLES</span></span>

### <span data-ttu-id="21fa2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="21fa2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="21fa2-112">To polecenie pobiera zaawansowane ustawienia ochrony przed zagrożeniami dla obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="21fa2-112">This command gets the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="21fa2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21fa2-113">PARAMETERS</span></span>

### <span data-ttu-id="21fa2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21fa2-114">-DefaultProfile</span></span>
<span data-ttu-id="21fa2-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21fa2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21fa2-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="21fa2-116">-InputObject</span></span>
<span data-ttu-id="21fa2-117">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="21fa2-117">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="21fa2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21fa2-118">-ResourceGroupName</span></span>
<span data-ttu-id="21fa2-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="21fa2-119">Resource group name.</span></span>

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

### <span data-ttu-id="21fa2-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21fa2-120">-ResourceId</span></span>
<span data-ttu-id="21fa2-121">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="21fa2-121">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="21fa2-122">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="21fa2-122">-WorkspaceName</span></span>
<span data-ttu-id="21fa2-123">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="21fa2-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="21fa2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21fa2-124">CommonParameters</span></span>
<span data-ttu-id="21fa2-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21fa2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21fa2-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21fa2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21fa2-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21fa2-127">INPUTS</span></span>

### <span data-ttu-id="21fa2-128">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="21fa2-128">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="21fa2-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21fa2-129">OUTPUTS</span></span>

### <span data-ttu-id="21fa2-130">Microsoft. Azure. Commands. Synapse. models. PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="21fa2-130">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="21fa2-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21fa2-131">NOTES</span></span>

## <span data-ttu-id="21fa2-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21fa2-132">RELATED LINKS</span></span>
