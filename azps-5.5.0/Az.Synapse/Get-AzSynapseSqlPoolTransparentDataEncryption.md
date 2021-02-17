---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5e127388b756c19422990bf27ee40e351bfc2581
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190634"
---
# <span data-ttu-id="b109f-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="b109f-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="b109f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b109f-102">SYNOPSIS</span></span>
<span data-ttu-id="b109f-103">Pobiera stan TDE dla puli SQL.</span><span class="sxs-lookup"><span data-stu-id="b109f-103">Gets the TDE state for a SQL pool.</span></span>

## <span data-ttu-id="b109f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b109f-104">SYNTAX</span></span>

### <span data-ttu-id="b109f-105">GetByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b109f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b109f-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b109f-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b109f-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b109f-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b109f-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b109f-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b109f-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="b109f-109">DESCRIPTION</span></span>
<span data-ttu-id="b109f-110">Polecenie **cmdlet Get-AzSynapseSqlPoolTransparentDataEncryption** pobiera stan transparentnego szyfrowania danych (TDE, Transparent Data Encryption) dla puli sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b109f-110">The **Get-AzSynapseSqlPoolTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="b109f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b109f-111">EXAMPLES</span></span>

### <span data-ttu-id="b109f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b109f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="b109f-113">To polecenie otrzymuje stan TDE dla puli SQL o nazwie ContosoSqlPool w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="b109f-113">This command gets the status of TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="b109f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b109f-114">PARAMETERS</span></span>

### <span data-ttu-id="b109f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b109f-115">-DefaultProfile</span></span>
<span data-ttu-id="b109f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b109f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b109f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b109f-117">-InputObject</span></span>
<span data-ttu-id="b109f-118">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="b109f-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b109f-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b109f-119">-Name</span></span>
<span data-ttu-id="b109f-120">Nazwa puli języka SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="b109f-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="b109f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b109f-121">-ResourceGroupName</span></span>
<span data-ttu-id="b109f-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b109f-122">Resource group name.</span></span>

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

### <span data-ttu-id="b109f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b109f-123">-ResourceId</span></span>
<span data-ttu-id="b109f-124">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="b109f-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="b109f-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b109f-125">-WorkspaceName</span></span>
<span data-ttu-id="b109f-126">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="b109f-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b109f-127">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b109f-127">-WorkspaceObject</span></span>
<span data-ttu-id="b109f-128">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="b109f-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b109f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b109f-129">CommonParameters</span></span>
<span data-ttu-id="b109f-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b109f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b109f-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b109f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b109f-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b109f-132">INPUTS</span></span>

### <span data-ttu-id="b109f-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b109f-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b109f-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="b109f-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="b109f-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b109f-135">OUTPUTS</span></span>

### <span data-ttu-id="b109f-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="b109f-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="b109f-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b109f-137">NOTES</span></span>

## <span data-ttu-id="b109f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b109f-138">RELATED LINKS</span></span>
