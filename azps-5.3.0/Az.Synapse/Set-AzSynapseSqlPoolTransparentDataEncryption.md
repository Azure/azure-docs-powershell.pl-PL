---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5a8dbd1f21d640d5d1cb38fa403ee05dec9cfc20
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501294"
---
# <span data-ttu-id="0c83a-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="0c83a-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="0c83a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c83a-102">SYNOPSIS</span></span>
<span data-ttu-id="0c83a-103">Modyfikuje Właściwość TDE dla puli SQL.</span><span class="sxs-lookup"><span data-stu-id="0c83a-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="0c83a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c83a-104">SYNTAX</span></span>

### <span data-ttu-id="0c83a-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0c83a-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c83a-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c83a-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c83a-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c83a-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c83a-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c83a-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c83a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="0c83a-109">DESCRIPTION</span></span>
<span data-ttu-id="0c83a-110">Polecenie cmdlet **Set-AzSynapseSqlPoolTransparentDataEncryption** modyfikuje Właściwość przezroczystego szyfrowania danych (TDE) puli platformy Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="0c83a-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0c83a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c83a-111">EXAMPLES</span></span>

### <span data-ttu-id="0c83a-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0c83a-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="0c83a-113">To polecenie włącza TDE dla puli SQL o nazwie ContosoSqlPool w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="0c83a-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="0c83a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c83a-114">PARAMETERS</span></span>

### <span data-ttu-id="0c83a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c83a-115">-AsJob</span></span>
<span data-ttu-id="0c83a-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0c83a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c83a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c83a-117">-DefaultProfile</span></span>
<span data-ttu-id="0c83a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c83a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c83a-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0c83a-119">-InputObject</span></span>
<span data-ttu-id="0c83a-120">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="0c83a-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c83a-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0c83a-121">-Name</span></span>
<span data-ttu-id="0c83a-122">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="0c83a-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c83a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c83a-123">-ResourceGroupName</span></span>
<span data-ttu-id="0c83a-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0c83a-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c83a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c83a-125">-ResourceId</span></span>
<span data-ttu-id="0c83a-126">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="0c83a-126">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c83a-127">-State</span><span class="sxs-lookup"><span data-stu-id="0c83a-127">-State</span></span>
<span data-ttu-id="0c83a-128">Stan szyfrowania danych w puli usługi Azure Synapse analiza SQL z przezroczystością.</span><span class="sxs-lookup"><span data-stu-id="0c83a-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c83a-129">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="0c83a-129">-WorkspaceName</span></span>
<span data-ttu-id="0c83a-130">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="0c83a-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c83a-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="0c83a-131">-WorkspaceObject</span></span>
<span data-ttu-id="0c83a-132">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="0c83a-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c83a-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c83a-133">-Confirm</span></span>
<span data-ttu-id="0c83a-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c83a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c83a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c83a-135">-WhatIf</span></span>
<span data-ttu-id="0c83a-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c83a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c83a-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0c83a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c83a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c83a-138">CommonParameters</span></span>
<span data-ttu-id="0c83a-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c83a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c83a-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c83a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c83a-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c83a-141">INPUTS</span></span>

### <span data-ttu-id="0c83a-142">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0c83a-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0c83a-143">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0c83a-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="0c83a-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c83a-144">OUTPUTS</span></span>

### <span data-ttu-id="0c83a-145">Microsoft. Azure. Commands. Synapse. models. PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="0c83a-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="0c83a-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c83a-146">NOTES</span></span>

## <span data-ttu-id="0c83a-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c83a-147">RELATED LINKS</span></span>
