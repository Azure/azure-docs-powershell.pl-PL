---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
ms.openlocfilehash: 0dcac3fac32094cf2d9a0e42abcffd6222783e78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547391"
---
# <span data-ttu-id="77a29-101">Get-AzureRmOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="77a29-101">Get-AzureRmOperationalInsightsSchema</span></span>

## <span data-ttu-id="77a29-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77a29-102">SYNOPSIS</span></span>
<span data-ttu-id="77a29-103">Zwraca schemat skojarzony z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="77a29-103">Returns the schema associated with a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77a29-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77a29-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77a29-105">Opis</span><span class="sxs-lookup"><span data-stu-id="77a29-105">DESCRIPTION</span></span>
<span data-ttu-id="77a29-106">Polecenie cmdlet **Get-AzureRmOperationalInsightsSchema** zwraca schemat skojarzony z określonym obszarem roboczym w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="77a29-106">The **Get-AzureRmOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="77a29-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77a29-107">EXAMPLES</span></span>

### <span data-ttu-id="77a29-108">Przykład 1. Pobieranie schematów dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="77a29-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="77a29-109">To polecenie umożliwia pobieranie schematów skojarzonych z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="77a29-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="77a29-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77a29-110">PARAMETERS</span></span>

### <span data-ttu-id="77a29-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77a29-111">-DefaultProfile</span></span>
<span data-ttu-id="77a29-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="77a29-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77a29-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77a29-113">-ResourceGroupName</span></span>
<span data-ttu-id="77a29-114">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="77a29-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77a29-115">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="77a29-115">-WorkspaceName</span></span>
<span data-ttu-id="77a29-116">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="77a29-116">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77a29-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77a29-117">CommonParameters</span></span>
<span data-ttu-id="77a29-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77a29-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77a29-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77a29-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77a29-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77a29-120">INPUTS</span></span>

### <span data-ttu-id="77a29-121">System. String</span><span class="sxs-lookup"><span data-stu-id="77a29-121">System.String</span></span>

## <span data-ttu-id="77a29-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77a29-122">OUTPUTS</span></span>

### <span data-ttu-id="77a29-123">Microsoft. Azure. Commands. OperationalInsights. models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="77a29-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="77a29-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77a29-124">NOTES</span></span>

## <span data-ttu-id="77a29-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77a29-125">RELATED LINKS</span></span>

[<span data-ttu-id="77a29-126">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="77a29-126">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


