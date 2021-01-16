---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 592c35a3407bd42846e8c24786716a73d5729c9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383845"
---
# <span data-ttu-id="a4de9-101">Get-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="a4de9-101">Get-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="a4de9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4de9-102">SYNOPSIS</span></span>
<span data-ttu-id="a4de9-103">Pobiera ustawienia inspekcji puli SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a4de9-103">Gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a4de9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4de9-104">SYNTAX</span></span>

### <span data-ttu-id="a4de9-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a4de9-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4de9-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4de9-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4de9-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4de9-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4de9-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4de9-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4de9-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a4de9-109">DESCRIPTION</span></span>
<span data-ttu-id="a4de9-110">Polecenie cmdlet **Get-AzSynapseSqlPoolAuditSetting** pobiera ustawienia inspekcji puli SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a4de9-110">The **Get-AzSynapseSqlPoolAuditSetting** cmdlet gets the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a4de9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4de9-111">EXAMPLES</span></span>

### <span data-ttu-id="a4de9-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4de9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="a4de9-113">To polecenie pobiera ustawienia inspekcji puli SQL o nazwie ContosoSqlPool w obszarze roboczym ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a4de9-113">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a4de9-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a4de9-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="a4de9-115">To polecenie pobiera ustawienia inspekcji puli SQL o nazwie ContosoSqlPool w obszarze roboczym ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="a4de9-115">This command gets the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a4de9-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4de9-116">PARAMETERS</span></span>

### <span data-ttu-id="a4de9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4de9-117">-DefaultProfile</span></span>
<span data-ttu-id="a4de9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4de9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4de9-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a4de9-119">-InputObject</span></span>
<span data-ttu-id="a4de9-120">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="a4de9-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a4de9-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a4de9-121">-Name</span></span>
<span data-ttu-id="a4de9-122">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="a4de9-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="a4de9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4de9-123">-ResourceGroupName</span></span>
<span data-ttu-id="a4de9-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4de9-124">Resource group name.</span></span>

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

### <span data-ttu-id="a4de9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4de9-125">-ResourceId</span></span>
<span data-ttu-id="a4de9-126">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="a4de9-126">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="a4de9-127">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="a4de9-127">-WorkspaceName</span></span>
<span data-ttu-id="a4de9-128">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="a4de9-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a4de9-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="a4de9-129">-WorkspaceObject</span></span>
<span data-ttu-id="a4de9-130">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="a4de9-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a4de9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4de9-131">CommonParameters</span></span>
<span data-ttu-id="a4de9-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4de9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4de9-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4de9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4de9-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4de9-134">INPUTS</span></span>

### <span data-ttu-id="a4de9-135">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a4de9-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a4de9-136">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a4de9-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a4de9-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4de9-137">OUTPUTS</span></span>

### <span data-ttu-id="a4de9-138">Microsoft. Azure. Commands. Synapse. models. SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="a4de9-138">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="a4de9-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4de9-139">NOTES</span></span>

## <span data-ttu-id="a4de9-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4de9-140">RELATED LINKS</span></span>
