---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 420b95d8d20d21758e4f42db6c31e2d1ead557ac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334693"
---
# <span data-ttu-id="e6c5a-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="e6c5a-101">Reset-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="e6c5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c5a-103">Usuwa zaawansowane ustawienia ochrony przed zagrożeniami z obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="e6c5a-103">Removes the advanced threat protection settings from a workspace.</span></span>

## <span data-ttu-id="e6c5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6c5a-104">SYNTAX</span></span>

### <span data-ttu-id="e6c5a-105">ClearByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e6c5a-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6c5a-106">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6c5a-106">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6c5a-107">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6c5a-107">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6c5a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e6c5a-108">DESCRIPTION</span></span>
<span data-ttu-id="e6c5a-109">Polecenie cmdlet **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** usuwa zaawansowane ustawienia ochrony przed zagrożeniami z obszaru roboczego funkcji Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="e6c5a-109">The **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="e6c5a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6c5a-110">EXAMPLES</span></span>

### <span data-ttu-id="e6c5a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e6c5a-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e6c5a-112">To polecenie usuwa zaawansowane ustawienia ochrony przed zagrożeniami z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e6c5a-112">This command removes the advanced threat protection settings from a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="e6c5a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6c5a-113">PARAMETERS</span></span>

### <span data-ttu-id="e6c5a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6c5a-114">-AsJob</span></span>
<span data-ttu-id="e6c5a-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e6c5a-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6c5a-116">-DefaultProfile</span></span>
<span data-ttu-id="e6c5a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6c5a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6c5a-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e6c5a-118">-InputObject</span></span>
<span data-ttu-id="e6c5a-119">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="e6c5a-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6c5a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6c5a-120">-PassThru</span></span>
<span data-ttu-id="e6c5a-121">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="e6c5a-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e6c5a-122">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="e6c5a-122">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c5a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6c5a-123">-ResourceGroupName</span></span>
<span data-ttu-id="e6c5a-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e6c5a-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c5a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6c5a-125">-ResourceId</span></span>
<span data-ttu-id="e6c5a-126">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="e6c5a-126">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c5a-127">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="e6c5a-127">-WorkspaceName</span></span>
<span data-ttu-id="e6c5a-128">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="e6c5a-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c5a-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e6c5a-129">-Confirm</span></span>
<span data-ttu-id="e6c5a-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6c5a-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c5a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6c5a-131">-WhatIf</span></span>
<span data-ttu-id="e6c5a-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6c5a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6c5a-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e6c5a-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c5a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c5a-134">CommonParameters</span></span>
<span data-ttu-id="e6c5a-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6c5a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c5a-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6c5a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c5a-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6c5a-137">INPUTS</span></span>

### <span data-ttu-id="e6c5a-138">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e6c5a-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e6c5a-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6c5a-139">OUTPUTS</span></span>

### <span data-ttu-id="e6c5a-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6c5a-140">System.Boolean</span></span>

## <span data-ttu-id="e6c5a-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6c5a-141">NOTES</span></span>

## <span data-ttu-id="e6c5a-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6c5a-142">RELATED LINKS</span></span>
