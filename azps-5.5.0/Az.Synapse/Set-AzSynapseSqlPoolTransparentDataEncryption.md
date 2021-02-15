---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5a8dbd1f21d640d5d1cb38fa403ee05dec9cfc20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197323"
---
# <span data-ttu-id="95284-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="95284-101">Set-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="95284-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95284-102">SYNOPSIS</span></span>
<span data-ttu-id="95284-103">Modyfikuje właściwość TDE dla puli sql.</span><span class="sxs-lookup"><span data-stu-id="95284-103">Modifies TDE property for a SQL pool.</span></span>

## <span data-ttu-id="95284-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="95284-104">SYNTAX</span></span>

### <span data-ttu-id="95284-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="95284-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95284-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95284-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95284-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95284-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 -State <TransparentDataEncryptionStateType> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95284-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95284-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> -State <TransparentDataEncryptionStateType>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95284-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="95284-109">DESCRIPTION</span></span>
<span data-ttu-id="95284-110">Polecenie cmdlet **Set-AzSynapseSqlPoolTransparentDataEncryption** modyfikuje właściwość Transparent Data Encryption (TDE) puli SQL Synapse Analytics platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="95284-110">The **Set-AzSynapseSqlPoolTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="95284-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="95284-111">EXAMPLES</span></span>

### <span data-ttu-id="95284-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="95284-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -State Enabled
```

<span data-ttu-id="95284-113">To polecenie umożliwia TDE dla puli sql o nazwie ContosoSqlPool w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="95284-113">This command enables TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="95284-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95284-114">PARAMETERS</span></span>

### <span data-ttu-id="95284-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="95284-115">-AsJob</span></span>
<span data-ttu-id="95284-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="95284-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95284-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95284-117">-DefaultProfile</span></span>
<span data-ttu-id="95284-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="95284-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95284-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95284-119">-InputObject</span></span>
<span data-ttu-id="95284-120">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="95284-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="95284-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="95284-121">-Name</span></span>
<span data-ttu-id="95284-122">Nazwa puli języka SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="95284-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="95284-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95284-123">-ResourceGroupName</span></span>
<span data-ttu-id="95284-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="95284-124">Resource group name.</span></span>

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

### <span data-ttu-id="95284-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95284-125">-ResourceId</span></span>
<span data-ttu-id="95284-126">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="95284-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="95284-127">— województwo</span><span class="sxs-lookup"><span data-stu-id="95284-127">-State</span></span>
<span data-ttu-id="95284-128">Stan szyfrowania danych przezroczystych puli danych analizy Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="95284-128">The Azure Synapse Analytics Sql Pool Transparent Data Encryption state.</span></span>

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

### <span data-ttu-id="95284-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="95284-129">-WorkspaceName</span></span>
<span data-ttu-id="95284-130">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="95284-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="95284-131">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="95284-131">-WorkspaceObject</span></span>
<span data-ttu-id="95284-132">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="95284-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="95284-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="95284-133">-Confirm</span></span>
<span data-ttu-id="95284-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="95284-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95284-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95284-135">-WhatIf</span></span>
<span data-ttu-id="95284-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95284-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95284-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="95284-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95284-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95284-138">CommonParameters</span></span>
<span data-ttu-id="95284-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95284-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95284-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95284-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95284-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95284-141">INPUTS</span></span>

### <span data-ttu-id="95284-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="95284-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="95284-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="95284-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="95284-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95284-144">OUTPUTS</span></span>

### <span data-ttu-id="95284-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="95284-145">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="95284-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="95284-146">NOTES</span></span>

## <span data-ttu-id="95284-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95284-147">RELATED LINKS</span></span>
