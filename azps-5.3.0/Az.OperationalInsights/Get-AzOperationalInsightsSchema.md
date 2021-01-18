---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 12c3e54725abfd5addf33a3d31edcb8f8016e9dd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504332"
---
# <span data-ttu-id="1c8f6-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="1c8f6-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="1c8f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c8f6-102">SYNOPSIS</span></span>
<span data-ttu-id="1c8f6-103">Zwraca schemat skojarzony z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="1c8f6-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="1c8f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c8f6-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c8f6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1c8f6-105">DESCRIPTION</span></span>
<span data-ttu-id="1c8f6-106">Polecenie cmdlet **Get-AzOperationalInsightsSchema** zwraca schemat skojarzony z określonym obszarem roboczym w tej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c8f6-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="1c8f6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c8f6-107">EXAMPLES</span></span>

### <span data-ttu-id="1c8f6-108">Przykład 1. Pobieranie schematów dla obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="1c8f6-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="1c8f6-109">To polecenie umożliwia pobieranie schematów skojarzonych z obszarem roboczym.</span><span class="sxs-lookup"><span data-stu-id="1c8f6-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="1c8f6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c8f6-110">PARAMETERS</span></span>

### <span data-ttu-id="1c8f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c8f6-111">-DefaultProfile</span></span>
<span data-ttu-id="1c8f6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1c8f6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c8f6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c8f6-113">-ResourceGroupName</span></span>
<span data-ttu-id="1c8f6-114">Określa nazwę grupy zasobów platformy Azure zawierającej obszar roboczy.</span><span class="sxs-lookup"><span data-stu-id="1c8f6-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="1c8f6-115">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="1c8f6-115">-WorkspaceName</span></span>
<span data-ttu-id="1c8f6-116">Określa nazwę obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="1c8f6-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="1c8f6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c8f6-117">CommonParameters</span></span>
<span data-ttu-id="1c8f6-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c8f6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c8f6-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c8f6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c8f6-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c8f6-120">INPUTS</span></span>

### <span data-ttu-id="1c8f6-121">System. String</span><span class="sxs-lookup"><span data-stu-id="1c8f6-121">System.String</span></span>

## <span data-ttu-id="1c8f6-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c8f6-122">OUTPUTS</span></span>

### <span data-ttu-id="1c8f6-123">Microsoft. Azure. Commands. OperationalInsights. models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="1c8f6-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="1c8f6-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c8f6-124">NOTES</span></span>

## <span data-ttu-id="1c8f6-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c8f6-125">RELATED LINKS</span></span>

[<span data-ttu-id="1c8f6-126">Polecenia cmdlet usługi Azure Operations Insights</span><span class="sxs-lookup"><span data-stu-id="1c8f6-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


