---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 042597d8d300f57600680282dadb16e8ec221e59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718136"
---
# <span data-ttu-id="38c5d-101">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="38c5d-101">Get-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="38c5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="38c5d-103">Pobiera informacje o obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="38c5d-103">Gets information about a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38c5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38c5d-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38c5d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="38c5d-105">DESCRIPTION</span></span>
<span data-ttu-id="38c5d-106">Polecenie cmdlet **Get-AzureRmOperationalInsightsWorkspace** pobiera informacje o istniejącym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="38c5d-106">The **Get-AzureRmOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="38c5d-107">Jeśli określisz nazwę obszaru roboczego, to polecenie cmdlet będzie pobierać informacje o tym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="38c5d-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="38c5d-108">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje o wszystkich obszarach roboczych w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="38c5d-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="38c5d-109">Jeśli nie określisz nazwy i grupy zasobów, to polecenie cmdlet będzie pobierać informacje o wszystkich obszarach roboczych w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="38c5d-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="38c5d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38c5d-110">EXAMPLES</span></span>

### <span data-ttu-id="38c5d-111">Przykład 1. Uzyskaj obszar roboczy według nazwy</span><span class="sxs-lookup"><span data-stu-id="38c5d-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="38c5d-112">To polecenie pobiera obszar roboczy o nazwie Moja przestrzeń robocza w grupie zasobów o nazwie ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="38c5d-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="38c5d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38c5d-113">PARAMETERS</span></span>

### <span data-ttu-id="38c5d-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="38c5d-114">-Name</span></span>
<span data-ttu-id="38c5d-115">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="38c5d-115">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c5d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38c5d-116">-ResourceGroupName</span></span>
<span data-ttu-id="38c5d-117">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="38c5d-117">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c5d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c5d-118">-DefaultProfile</span></span>
<span data-ttu-id="38c5d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="38c5d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38c5d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c5d-120">CommonParameters</span></span>
<span data-ttu-id="38c5d-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38c5d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c5d-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38c5d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c5d-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38c5d-123">INPUTS</span></span>

## <span data-ttu-id="38c5d-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38c5d-124">OUTPUTS</span></span>

### <span data-ttu-id="38c5d-125">System. Collections. Generic. list "1 [Microsoft. Azure. Commands. OperationalInsights. modele. PSWorkspace]</span><span class="sxs-lookup"><span data-stu-id="38c5d-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace]</span></span>

### <span data-ttu-id="38c5d-126">Microsoft. Azure. Commands. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="38c5d-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="38c5d-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38c5d-127">NOTES</span></span>

## <span data-ttu-id="38c5d-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38c5d-128">RELATED LINKS</span></span>

[<span data-ttu-id="38c5d-129">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="38c5d-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


