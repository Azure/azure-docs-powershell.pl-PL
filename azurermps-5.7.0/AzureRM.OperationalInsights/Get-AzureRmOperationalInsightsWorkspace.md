---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: b2bd8855d9c8b125b4bef72f42f0bd4a63071adb
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/21/2020
ms.locfileid: "93554418"
---
# <span data-ttu-id="bb2c1-101">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="bb2c1-101">Get-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="bb2c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb2c1-102">SYNOPSIS</span></span>
<span data-ttu-id="bb2c1-103">Pobiera informacje o obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="bb2c1-103">Gets information about a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb2c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb2c1-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb2c1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bb2c1-105">DESCRIPTION</span></span>
<span data-ttu-id="bb2c1-106">Polecenie cmdlet **Get-AzureRmOperationalInsightsWorkspace** pobiera informacje o istniejącym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="bb2c1-106">The **Get-AzureRmOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="bb2c1-107">Jeśli określisz nazwę obszaru roboczego, to polecenie cmdlet będzie pobierać informacje o tym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="bb2c1-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="bb2c1-108">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich obszarach roboczych w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="bb2c1-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="bb2c1-109">Jeśli nie określisz nazwy i grupy zasobów, to polecenie cmdlet będzie pobierać informacje o wszystkich obszarach roboczych w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="bb2c1-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="bb2c1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb2c1-110">EXAMPLES</span></span>

### <span data-ttu-id="bb2c1-111">Przykład 1. Uzyskaj obszar roboczy według nazwy</span><span class="sxs-lookup"><span data-stu-id="bb2c1-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="bb2c1-112">To polecenie pobiera obszar roboczy o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="bb2c1-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="bb2c1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb2c1-113">PARAMETERS</span></span>

### <span data-ttu-id="bb2c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb2c1-114">-DefaultProfile</span></span>
<span data-ttu-id="bb2c1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bb2c1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2c1-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bb2c1-116">-Name</span></span>
<span data-ttu-id="bb2c1-117">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="bb2c1-117">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2c1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb2c1-118">-ResourceGroupName</span></span>
<span data-ttu-id="bb2c1-119">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bb2c1-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2c1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb2c1-120">CommonParameters</span></span>
<span data-ttu-id="bb2c1-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb2c1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb2c1-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb2c1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb2c1-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb2c1-123">INPUTS</span></span>

### <span data-ttu-id="bb2c1-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="bb2c1-124">None</span></span>
<span data-ttu-id="bb2c1-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="bb2c1-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb2c1-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb2c1-126">OUTPUTS</span></span>

### <span data-ttu-id="bb2c1-127">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. OperationalInsights. modele. PSWorkspace]</span><span class="sxs-lookup"><span data-stu-id="bb2c1-127">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace]</span></span>

### <span data-ttu-id="bb2c1-128">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bb2c1-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="bb2c1-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb2c1-129">NOTES</span></span>

## <span data-ttu-id="bb2c1-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb2c1-130">RELATED LINKS</span></span>

[<span data-ttu-id="bb2c1-131">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="bb2c1-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


