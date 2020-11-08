---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: a89b4210fcd498aca3a25451e6f691df20d5510e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223700"
---
# <span data-ttu-id="61130-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="61130-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="61130-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61130-102">SYNOPSIS</span></span>
<span data-ttu-id="61130-103">Pobiera informacje dotyczące gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="61130-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="61130-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61130-104">SYNTAX</span></span>

### <span data-ttu-id="61130-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="61130-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61130-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="61130-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61130-107">Opis</span><span class="sxs-lookup"><span data-stu-id="61130-107">DESCRIPTION</span></span>
<span data-ttu-id="61130-108">Polecenie cmdlet **Get-AzOperationalInsightsStorageInsight** pobiera informacje na temat istniejącego miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="61130-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="61130-109">Jeśli jest określona nazwa informacji o magazynie, to polecenie cmdlet będzie pobierać informacje o tym magazynie.</span><span class="sxs-lookup"><span data-stu-id="61130-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="61130-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich dyskach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="61130-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="61130-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61130-111">EXAMPLES</span></span>

### <span data-ttu-id="61130-112">Przykład 1: uzyskiwanie szczegółowego miejsca do magazynowania na podstawie nazwy</span><span class="sxs-lookup"><span data-stu-id="61130-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="61130-113">To polecenie pobiera szczegółowe dane dotyczące miejsca do magazynowania o nazwie MyStorageInsight z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="61130-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="61130-114">Przykład 2: uzyskiwanie informacji o magazynowaniu przy użyciu obiektu obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="61130-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="61130-115">W pierwszym poleceniu jest używane polecenie cmdlet **Get-AzOperationalInsightsWorkspace** w celu uzyskania obszaru roboczego usługi Insights, a następnie zapisanie go w zmiennej $Workspace.</span><span class="sxs-lookup"><span data-stu-id="61130-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="61130-116">Drugie polecenie pobiera szczegółowe dane o nazwie MyStorageInsight dla obszaru roboczego w $Workspace.</span><span class="sxs-lookup"><span data-stu-id="61130-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="61130-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61130-117">PARAMETERS</span></span>

### <span data-ttu-id="61130-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61130-118">-DefaultProfile</span></span>
<span data-ttu-id="61130-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="61130-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61130-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="61130-120">-Name</span></span>
<span data-ttu-id="61130-121">Określa nazwę usługi gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="61130-121">Specifies the Storage Insight name.</span></span>

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

### <span data-ttu-id="61130-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61130-122">-ResourceGroupName</span></span>
<span data-ttu-id="61130-123">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="61130-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="61130-124">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="61130-124">-Workspace</span></span>
<span data-ttu-id="61130-125">Określa obszar roboczy zawierający informacje dotyczące miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="61130-125">Specifies the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="61130-126">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="61130-126">-WorkspaceName</span></span>
<span data-ttu-id="61130-127">Określa nazwę obszaru roboczego, który zawiera informacje dotyczące miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="61130-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="61130-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61130-128">CommonParameters</span></span>
<span data-ttu-id="61130-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61130-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61130-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61130-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61130-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61130-131">INPUTS</span></span>

### <span data-ttu-id="61130-132">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="61130-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="61130-133">System. String</span><span class="sxs-lookup"><span data-stu-id="61130-133">System.String</span></span>

## <span data-ttu-id="61130-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61130-134">OUTPUTS</span></span>

### <span data-ttu-id="61130-135">Microsoft. Azure. Commands. OperationalInsights. models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="61130-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="61130-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61130-136">NOTES</span></span>

## <span data-ttu-id="61130-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61130-137">RELATED LINKS</span></span>

[<span data-ttu-id="61130-138">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="61130-138">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


