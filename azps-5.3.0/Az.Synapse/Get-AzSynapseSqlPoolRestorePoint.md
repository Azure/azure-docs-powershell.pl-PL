---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: f9f921368f55b5901657ca4e366927a284302745
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383831"
---
# <span data-ttu-id="ccc78-101">Get-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="ccc78-101">Get-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="ccc78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ccc78-102">SYNOPSIS</span></span>
<span data-ttu-id="ccc78-103">Pobiera różne punkty przywracania, z których można przywrócić pulę SQL analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="ccc78-103">Retrieves the distinct restore points from which a Synapse Analytics SQL pool can be restored.</span></span>

## <span data-ttu-id="ccc78-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ccc78-104">SYNTAX</span></span>

### <span data-ttu-id="ccc78-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ccc78-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccc78-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccc78-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccc78-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccc78-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ccc78-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccc78-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccc78-109">Opis</span><span class="sxs-lookup"><span data-stu-id="ccc78-109">DESCRIPTION</span></span>
<span data-ttu-id="ccc78-110">Polecenie cmdlet **Get-AzSynapseSqlPoolRestorePoint** pobiera oddzielne punkty przywracania, z których można przywrócić pulę SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ccc78-110">The **Get-AzSynapseSqlPoolRestorePoint** cmdlet retrieves the distinct restore points that an Azure Synapse Analytics SQL pool can be restored from.</span></span>

## <span data-ttu-id="ccc78-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ccc78-111">EXAMPLES</span></span>

### <span data-ttu-id="ccc78-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ccc78-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolRestorePoint -WorkspaceName -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="ccc78-113">To polecenie zwraca wszystkie dostępne punkty przywracania dla puli SQL usługi Azure Synapse analiza o nazwie ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="ccc78-113">This command returns all available restore points for the Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

## <span data-ttu-id="ccc78-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ccc78-114">PARAMETERS</span></span>

### <span data-ttu-id="ccc78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccc78-115">-DefaultProfile</span></span>
<span data-ttu-id="ccc78-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ccc78-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccc78-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ccc78-117">-InputObject</span></span>
<span data-ttu-id="ccc78-118">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="ccc78-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ccc78-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ccc78-119">-Name</span></span>
<span data-ttu-id="ccc78-120">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="ccc78-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="ccc78-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccc78-121">-ResourceGroupName</span></span>
<span data-ttu-id="ccc78-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ccc78-122">Resource group name.</span></span>

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

### <span data-ttu-id="ccc78-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccc78-123">-ResourceId</span></span>
<span data-ttu-id="ccc78-124">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="ccc78-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="ccc78-125">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="ccc78-125">-WorkspaceName</span></span>
<span data-ttu-id="ccc78-126">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="ccc78-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ccc78-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="ccc78-127">-WorkspaceObject</span></span>
<span data-ttu-id="ccc78-128">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="ccc78-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ccc78-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccc78-129">CommonParameters</span></span>
<span data-ttu-id="ccc78-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccc78-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccc78-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccc78-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccc78-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ccc78-132">INPUTS</span></span>

### <span data-ttu-id="ccc78-133">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ccc78-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ccc78-134">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ccc78-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="ccc78-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ccc78-135">OUTPUTS</span></span>

### <span data-ttu-id="ccc78-136">Microsoft. Azure. Management. Synapse. MODELES. RestorePoint</span><span class="sxs-lookup"><span data-stu-id="ccc78-136">Microsoft.Azure.Management.Synapse.Models.RestorePoint</span></span>

## <span data-ttu-id="ccc78-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ccc78-137">NOTES</span></span>

## <span data-ttu-id="ccc78-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ccc78-138">RELATED LINKS</span></span>
