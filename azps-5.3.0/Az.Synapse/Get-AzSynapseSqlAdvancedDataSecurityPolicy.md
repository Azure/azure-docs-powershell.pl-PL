---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
ms.openlocfilehash: b0d21c8d59d2a33671fead2e88d402779f99fb7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383938"
---
# <span data-ttu-id="7b8f0-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="7b8f0-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="7b8f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b8f0-102">SYNOPSIS</span></span>
<span data-ttu-id="7b8f0-103">Pobiera zaawansowane zasady zabezpieczeń danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-103">Gets Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="7b8f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b8f0-104">SYNTAX</span></span>

### <span data-ttu-id="7b8f0-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7b8f0-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b8f0-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b8f0-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b8f0-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b8f0-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b8f0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7b8f0-108">DESCRIPTION</span></span>
<span data-ttu-id="7b8f0-109">Polecenie cmdlet **Get-AzSynapseSqlAdvancedDataSecurityPolicy** pobiera zaawansowane zasady zabezpieczeń danych w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-109">The **Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="7b8f0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b8f0-110">EXAMPLES</span></span>

### <span data-ttu-id="7b8f0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7b8f0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedDataSecurityPolicy -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="7b8f0-112">To polecenie pobiera zaawansowane zabezpieczenia danych w obszarze roboczym o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-112">This command gets Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="7b8f0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7b8f0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAdvancedDataSecurityPolicy
```

<span data-ttu-id="7b8f0-114">To polecenie uzyskuje zaawansowane zabezpieczenia danych w obszarze roboczym o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-114">This command gets Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="7b8f0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b8f0-115">PARAMETERS</span></span>

### <span data-ttu-id="7b8f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b8f0-116">-DefaultProfile</span></span>
<span data-ttu-id="7b8f0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b8f0-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7b8f0-118">-InputObject</span></span>
<span data-ttu-id="7b8f0-119">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-119">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7b8f0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b8f0-120">-ResourceGroupName</span></span>
<span data-ttu-id="7b8f0-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-121">Resource group name.</span></span>

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

### <span data-ttu-id="7b8f0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b8f0-122">-ResourceId</span></span>
<span data-ttu-id="7b8f0-123">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="7b8f0-124">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="7b8f0-124">-WorkspaceName</span></span>
<span data-ttu-id="7b8f0-125">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7b8f0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b8f0-126">CommonParameters</span></span>
<span data-ttu-id="7b8f0-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b8f0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b8f0-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b8f0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b8f0-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b8f0-129">INPUTS</span></span>

### <span data-ttu-id="7b8f0-130">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7b8f0-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7b8f0-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b8f0-131">OUTPUTS</span></span>

### <span data-ttu-id="7b8f0-132">Microsoft. Azure. Commands. Synapse. models. WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="7b8f0-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="7b8f0-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b8f0-133">NOTES</span></span>

## <span data-ttu-id="7b8f0-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b8f0-134">RELATED LINKS</span></span>
