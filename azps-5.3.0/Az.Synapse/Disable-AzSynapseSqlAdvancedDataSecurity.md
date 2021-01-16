---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/disable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: 2cbc79314d9e5fc7dac524786b8ba0bfa349573b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384148"
---
# <span data-ttu-id="b0e5c-101">Disable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="b0e5c-101">Disable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="b0e5c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0e5c-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e5c-103">Wyłącza zaawansowane zabezpieczenia danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="b0e5c-103">Disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="b0e5c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0e5c-104">SYNTAX</span></span>

### <span data-ttu-id="b0e5c-105">DisableByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b0e5c-105">DisableByNameParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e5c-106">DisableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0e5c-106">DisableByInputObjectParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e5c-107">DisableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0e5c-107">DisableByResourceIdParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0e5c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b0e5c-108">DESCRIPTION</span></span>
<span data-ttu-id="b0e5c-109">Polecenie cmdlet **disable-AzSynapseSqlAdvancedDataSecurity** wyłącza zaawansowane zabezpieczenia danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="b0e5c-109">The **Disable-AzSynapseSqlAdvancedDataSecurity** cmdlet disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="b0e5c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0e5c-110">EXAMPLES</span></span>

### <span data-ttu-id="b0e5c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b0e5c-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="b0e5c-112">To polecenie wyłącza zaawansowane zabezpieczenia danych w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b0e5c-112">This command disables Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="b0e5c-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b0e5c-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Disable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="b0e5c-114">To polecenie wyłącza zaawansowane zabezpieczenia danych w obszarze roboczym o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="b0e5c-114">This command disables Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="b0e5c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0e5c-115">PARAMETERS</span></span>

### <span data-ttu-id="b0e5c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0e5c-116">-AsJob</span></span>
<span data-ttu-id="b0e5c-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b0e5c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0e5c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e5c-118">-DefaultProfile</span></span>
<span data-ttu-id="b0e5c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0e5c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0e5c-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b0e5c-120">-InputObject</span></span>
<span data-ttu-id="b0e5c-121">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="b0e5c-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DisableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0e5c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0e5c-122">-ResourceGroupName</span></span>
<span data-ttu-id="b0e5c-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b0e5c-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e5c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0e5c-124">-ResourceId</span></span>
<span data-ttu-id="b0e5c-125">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="b0e5c-125">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e5c-126">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="b0e5c-126">-WorkspaceName</span></span>
<span data-ttu-id="b0e5c-127">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="b0e5c-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e5c-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b0e5c-128">-Confirm</span></span>
<span data-ttu-id="b0e5c-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0e5c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0e5c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0e5c-130">-WhatIf</span></span>
<span data-ttu-id="b0e5c-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0e5c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0e5c-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b0e5c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0e5c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e5c-133">CommonParameters</span></span>
<span data-ttu-id="b0e5c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0e5c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e5c-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0e5c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e5c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0e5c-136">INPUTS</span></span>

### <span data-ttu-id="b0e5c-137">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b0e5c-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b0e5c-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0e5c-138">OUTPUTS</span></span>

### <span data-ttu-id="b0e5c-139">Microsoft. Azure. Commands. Synapse. models. WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="b0e5c-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="b0e5c-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0e5c-140">NOTES</span></span>

## <span data-ttu-id="b0e5c-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0e5c-141">RELATED LINKS</span></span>
