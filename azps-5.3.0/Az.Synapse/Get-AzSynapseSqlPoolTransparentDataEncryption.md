---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5e127388b756c19422990bf27ee40e351bfc2581
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383798"
---
# <span data-ttu-id="df3a0-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="df3a0-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="df3a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df3a0-102">SYNOPSIS</span></span>
<span data-ttu-id="df3a0-103">Pobiera stan TDE dla puli SQL.</span><span class="sxs-lookup"><span data-stu-id="df3a0-103">Gets the TDE state for a SQL pool.</span></span>

## <span data-ttu-id="df3a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df3a0-104">SYNTAX</span></span>

### <span data-ttu-id="df3a0-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="df3a0-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df3a0-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df3a0-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df3a0-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df3a0-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df3a0-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df3a0-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df3a0-109">Opis</span><span class="sxs-lookup"><span data-stu-id="df3a0-109">DESCRIPTION</span></span>
<span data-ttu-id="df3a0-110">Polecenie cmdlet **Get-AzSynapseSqlPoolTransparentDataEncryption** Pobiera stan przezroczystego szyfrowania danych (TDE) dla puli platformy Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="df3a0-110">The **Get-AzSynapseSqlPoolTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="df3a0-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df3a0-111">EXAMPLES</span></span>

### <span data-ttu-id="df3a0-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="df3a0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="df3a0-113">To polecenie pobiera stan TDE dla puli SQL o nazwie ContosoSqlPool w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="df3a0-113">This command gets the status of TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="df3a0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df3a0-114">PARAMETERS</span></span>

### <span data-ttu-id="df3a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df3a0-115">-DefaultProfile</span></span>
<span data-ttu-id="df3a0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df3a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df3a0-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="df3a0-117">-InputObject</span></span>
<span data-ttu-id="df3a0-118">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="df3a0-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df3a0-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df3a0-119">-Name</span></span>
<span data-ttu-id="df3a0-120">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="df3a0-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df3a0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df3a0-121">-ResourceGroupName</span></span>
<span data-ttu-id="df3a0-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="df3a0-122">Resource group name.</span></span>

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

### <span data-ttu-id="df3a0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df3a0-123">-ResourceId</span></span>
<span data-ttu-id="df3a0-124">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="df3a0-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="df3a0-125">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="df3a0-125">-WorkspaceName</span></span>
<span data-ttu-id="df3a0-126">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="df3a0-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="df3a0-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="df3a0-127">-WorkspaceObject</span></span>
<span data-ttu-id="df3a0-128">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="df3a0-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df3a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df3a0-129">CommonParameters</span></span>
<span data-ttu-id="df3a0-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df3a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df3a0-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df3a0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df3a0-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df3a0-132">INPUTS</span></span>

### <span data-ttu-id="df3a0-133">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="df3a0-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="df3a0-134">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="df3a0-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="df3a0-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df3a0-135">OUTPUTS</span></span>

### <span data-ttu-id="df3a0-136">Microsoft. Azure. Commands. Synapse. models. PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="df3a0-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="df3a0-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df3a0-137">NOTES</span></span>

## <span data-ttu-id="df3a0-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df3a0-138">RELATED LINKS</span></span>
