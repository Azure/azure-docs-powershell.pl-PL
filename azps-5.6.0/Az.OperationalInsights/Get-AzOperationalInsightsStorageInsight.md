---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: adbe725557ccf1535a83f5f411cfdc44fd69c6a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981690"
---
# <span data-ttu-id="e0578-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="e0578-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="e0578-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0578-102">SYNOPSIS</span></span>
<span data-ttu-id="e0578-103">Pobiera informacje o szczegółowych informacjach o przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="e0578-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="e0578-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0578-104">SYNTAX</span></span>

### <span data-ttu-id="e0578-105">ByWorkspaceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="e0578-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0578-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e0578-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0578-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0578-107">DESCRIPTION</span></span>
<span data-ttu-id="e0578-108">Polecenie **cmdlet Get-AzOperationalInsightsStorageInsight pobiera** informacje o istniejącej wiedzę na temat magazynu.</span><span class="sxs-lookup"><span data-stu-id="e0578-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="e0578-109">Jeśli zostanie określona nazwa szczegółowej informacji o magazynie, to polecenie cmdlet pobiera informacje o tym szczegółowe informacje o magazynie.</span><span class="sxs-lookup"><span data-stu-id="e0578-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="e0578-110">Jeśli nie określisz nazwy, to polecenie cmdlet pobiera informacje o wszystkich szczegółowych informacjach dotyczących magazynu w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="e0578-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="e0578-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0578-111">EXAMPLES</span></span>

### <span data-ttu-id="e0578-112">Przykład 1. Uzyskiwanie szczegółowych informacji o przestrzeni dyskowej według nazwy</span><span class="sxs-lookup"><span data-stu-id="e0578-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="e0578-113">To polecenie pobiera szczegółowe informacje o magazynie o nazwie MyStorageInsight z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e0578-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e0578-114">Przykład 2. Uzyskiwanie szczegółowych informacji o magazynie przy użyciu obiektu obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="e0578-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="e0578-115">Pierwsze polecenie używa polecenia cmdlet **Get-AzOperationalInsightsWorkspace** w celu uzyskania obszaru roboczego szczegółowych informacji operacyjnych, a następnie zapisuje go w $Workspace danych.</span><span class="sxs-lookup"><span data-stu-id="e0578-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="e0578-116">Drugie polecenie pobiera szczegółowe informacje o przestrzeni dyskowej o nazwie MyStorageInsight dla obszaru roboczego w $Workspace.</span><span class="sxs-lookup"><span data-stu-id="e0578-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="e0578-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0578-117">PARAMETERS</span></span>

### <span data-ttu-id="e0578-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0578-118">-DefaultProfile</span></span>
<span data-ttu-id="e0578-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e0578-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0578-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e0578-120">-Name</span></span>
<span data-ttu-id="e0578-121">Określa nazwę szczegółowej informacji o magazynie.</span><span class="sxs-lookup"><span data-stu-id="e0578-121">Specifies the Storage Insight name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0578-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0578-122">-ResourceGroupName</span></span>
<span data-ttu-id="e0578-123">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0578-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0578-124">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="e0578-124">-Workspace</span></span>
<span data-ttu-id="e0578-125">Określa obszar roboczy zawierający szczegółowe informacje o przestrzeni dyskowej.</span><span class="sxs-lookup"><span data-stu-id="e0578-125">Specifies the workspace that contains the Storage Insights.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0578-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e0578-126">-WorkspaceName</span></span>
<span data-ttu-id="e0578-127">Określa nazwę obszaru roboczego zawierającego szczegółowe informacje o magazynie.</span><span class="sxs-lookup"><span data-stu-id="e0578-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0578-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0578-128">CommonParameters</span></span>
<span data-ttu-id="e0578-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0578-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0578-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0578-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0578-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0578-131">INPUTS</span></span>

### <span data-ttu-id="e0578-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e0578-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e0578-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e0578-133">System.String</span></span>

## <span data-ttu-id="e0578-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0578-134">OUTPUTS</span></span>

### <span data-ttu-id="e0578-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="e0578-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="e0578-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0578-136">NOTES</span></span>

## <span data-ttu-id="e0578-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0578-137">RELATED LINKS</span></span>

[<span data-ttu-id="e0578-138">Polecenia cmdlet usługi Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="e0578-138">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


