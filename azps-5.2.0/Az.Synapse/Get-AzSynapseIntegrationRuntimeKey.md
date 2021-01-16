---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339241"
---
# <span data-ttu-id="03ef0-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="03ef0-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="03ef0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="03ef0-103">Pobiera klucze dla środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="03ef0-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="03ef0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03ef0-104">SYNTAX</span></span>

### <span data-ttu-id="03ef0-105">GetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="03ef0-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03ef0-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03ef0-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03ef0-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03ef0-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="03ef0-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03ef0-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03ef0-109">Opis</span><span class="sxs-lookup"><span data-stu-id="03ef0-109">DESCRIPTION</span></span>
<span data-ttu-id="03ef0-110">Polecenie cmdlet **Get-AzSynapseIntegrationRuntimeKey** pobiera klucze środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="03ef0-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="03ef0-111">Klucze są używane do rejestrowania węzła środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="03ef0-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="03ef0-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03ef0-112">EXAMPLES</span></span>

### <span data-ttu-id="03ef0-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="03ef0-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="03ef0-114">Polecenie cmdlet pobiera klucze środowiska wykonawczego integracji o nazwie test-SelfHost-IR '.</span><span class="sxs-lookup"><span data-stu-id="03ef0-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="03ef0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03ef0-115">PARAMETERS</span></span>

### <span data-ttu-id="03ef0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ef0-116">-DefaultProfile</span></span>
<span data-ttu-id="03ef0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03ef0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03ef0-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="03ef0-118">-InputObject</span></span>
<span data-ttu-id="03ef0-119">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="03ef0-119">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03ef0-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03ef0-120">-Name</span></span>
<span data-ttu-id="03ef0-121">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="03ef0-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ef0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03ef0-122">-ResourceGroupName</span></span>
<span data-ttu-id="03ef0-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="03ef0-123">Resource group name.</span></span>

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

### <span data-ttu-id="03ef0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03ef0-124">-ResourceId</span></span>
<span data-ttu-id="03ef0-125">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="03ef0-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="03ef0-126">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="03ef0-126">-WorkspaceName</span></span>
<span data-ttu-id="03ef0-127">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="03ef0-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="03ef0-128">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="03ef0-128">-WorkspaceObject</span></span>
<span data-ttu-id="03ef0-129">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="03ef0-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="03ef0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ef0-130">CommonParameters</span></span>
<span data-ttu-id="03ef0-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03ef0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ef0-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03ef0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ef0-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03ef0-133">INPUTS</span></span>

### <span data-ttu-id="03ef0-134">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="03ef0-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="03ef0-135">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="03ef0-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="03ef0-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03ef0-136">OUTPUTS</span></span>

### <span data-ttu-id="03ef0-137">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="03ef0-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="03ef0-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03ef0-138">NOTES</span></span>

## <span data-ttu-id="03ef0-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03ef0-139">RELATED LINKS</span></span>
