---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: cd7dad03d8542685339778d0b0cdac967f83ea21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718139"
---
# <span data-ttu-id="6ca2b-101">Get-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="6ca2b-101">Get-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="6ca2b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ca2b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca2b-103">Pobiera informacje dotyczące gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="6ca2b-103">Gets information about a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ca2b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ca2b-104">SYNTAX</span></span>

### <span data-ttu-id="6ca2b-105">ByWorkspaceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6ca2b-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ca2b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6ca2b-106">ByWorkspaceObject</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ca2b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6ca2b-107">DESCRIPTION</span></span>
<span data-ttu-id="6ca2b-108">Polecenie cmdlet **Get-AzureRmOperationalInsightsStorageInsight** pobiera informacje na temat istniejącego miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="6ca2b-108">The **Get-AzureRmOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="6ca2b-109">Jeśli jest określona nazwa informacji o magazynie, to polecenie cmdlet będzie pobierać informacje o tym magazynie.</span><span class="sxs-lookup"><span data-stu-id="6ca2b-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="6ca2b-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich dyskach w obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="6ca2b-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="6ca2b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ca2b-111">EXAMPLES</span></span>

### <span data-ttu-id="6ca2b-112">Przykład 1: uzyskiwanie szczegółowego miejsca do magazynowania na podstawie nazwy</span><span class="sxs-lookup"><span data-stu-id="6ca2b-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="6ca2b-113">To polecenie pobiera szczegółowe dane dotyczące miejsca do magazynowania o nazwie MyStorageInsight z obszaru roboczego o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="6ca2b-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="6ca2b-114">Przykład 2: uzyskiwanie informacji o magazynowaniu przy użyciu obiektu obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="6ca2b-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="6ca2b-115">W pierwszym poleceniu jest używane polecenie cmdlet **Get-AzureRmOperationalInsightsWorkspace** w celu uzyskania obszaru roboczego usługi Insights, a następnie zapisanie go w zmiennej $Workspace.</span><span class="sxs-lookup"><span data-stu-id="6ca2b-115">The first command uses the **Get-AzureRmOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="6ca2b-116">Drugie polecenie pobiera szczegółowe dane o nazwie MyStorageInsight dla obszaru roboczego w $Workspace.</span><span class="sxs-lookup"><span data-stu-id="6ca2b-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="6ca2b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ca2b-117">PARAMETERS</span></span>

### <span data-ttu-id="6ca2b-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6ca2b-118">-Name</span></span>
<span data-ttu-id="6ca2b-119">Określa nazwę usługi gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="6ca2b-119">Specifies the Storage Insight name.</span></span>

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

### <span data-ttu-id="6ca2b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca2b-120">-ResourceGroupName</span></span>
<span data-ttu-id="6ca2b-121">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6ca2b-121">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="6ca2b-122">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="6ca2b-122">-Workspace</span></span>
<span data-ttu-id="6ca2b-123">Określa obszar roboczy zawierający informacje dotyczące miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="6ca2b-123">Specifies the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="6ca2b-124">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="6ca2b-124">-WorkspaceName</span></span>
<span data-ttu-id="6ca2b-125">Określa nazwę obszaru roboczego, który zawiera informacje dotyczące miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="6ca2b-125">Specifies the name of the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="6ca2b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca2b-126">-DefaultProfile</span></span>
<span data-ttu-id="6ca2b-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ca2b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ca2b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca2b-128">CommonParameters</span></span>
<span data-ttu-id="6ca2b-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca2b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca2b-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ca2b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca2b-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ca2b-131">INPUTS</span></span>

### <span data-ttu-id="6ca2b-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6ca2b-132">PSWorkspace</span></span>
<span data-ttu-id="6ca2b-133">Parametr "obszar roboczy" akceptuje wartość typu "PSWorkspace" z potoku</span><span class="sxs-lookup"><span data-stu-id="6ca2b-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="6ca2b-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ca2b-134">OUTPUTS</span></span>

### <span data-ttu-id="6ca2b-135">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. OperationalInsights. modele. PSStorageInsight]</span><span class="sxs-lookup"><span data-stu-id="6ca2b-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight]</span></span>

### <span data-ttu-id="6ca2b-136">Microsoft. Azure. Commands. OperationalInsights. models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="6ca2b-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="6ca2b-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ca2b-137">NOTES</span></span>

## <span data-ttu-id="6ca2b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ca2b-138">RELATED LINKS</span></span>

[<span data-ttu-id="6ca2b-139">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="6ca2b-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


