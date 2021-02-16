---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: ef90211ccca53a94db2651f17b3a666a725ce8b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184058"
---
# <span data-ttu-id="10f54-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="10f54-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="10f54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10f54-102">SYNOPSIS</span></span>
<span data-ttu-id="10f54-103">Aktualizuje źródło danych.</span><span class="sxs-lookup"><span data-stu-id="10f54-103">Updates a data source.</span></span>

## <span data-ttu-id="10f54-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="10f54-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10f54-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="10f54-105">DESCRIPTION</span></span>
<span data-ttu-id="10f54-106">Polecenie **cmdlet Set-AzOperationalInsightsDataSource** aktualizuje źródło danych.</span><span class="sxs-lookup"><span data-stu-id="10f54-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="10f54-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="10f54-107">EXAMPLES</span></span>

## <span data-ttu-id="10f54-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10f54-108">PARAMETERS</span></span>

### <span data-ttu-id="10f54-109">- DataSource</span><span class="sxs-lookup"><span data-stu-id="10f54-109">-DataSource</span></span>
<span data-ttu-id="10f54-110">Określa źródło danych, które będzie aktualizowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10f54-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10f54-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10f54-111">-DefaultProfile</span></span>
<span data-ttu-id="10f54-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="10f54-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10f54-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10f54-113">CommonParameters</span></span>
<span data-ttu-id="10f54-114">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10f54-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10f54-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10f54-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10f54-116">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10f54-116">INPUTS</span></span>

### <span data-ttu-id="10f54-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="10f54-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="10f54-118">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10f54-118">OUTPUTS</span></span>

### <span data-ttu-id="10f54-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="10f54-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="10f54-120">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="10f54-120">NOTES</span></span>
* <span data-ttu-id="10f54-121">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, operacyjny, insights</span><span class="sxs-lookup"><span data-stu-id="10f54-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="10f54-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10f54-122">RELATED LINKS</span></span>

[<span data-ttu-id="10f54-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="10f54-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="10f54-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="10f54-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


