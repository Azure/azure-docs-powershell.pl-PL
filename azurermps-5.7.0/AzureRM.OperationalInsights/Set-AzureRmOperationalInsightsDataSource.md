---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: e45dcbfad9b4b92695f310d7d2c56fc46fc57bd7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525070"
---
# <span data-ttu-id="be630-101">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="be630-101">Set-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="be630-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be630-102">SYNOPSIS</span></span>
<span data-ttu-id="be630-103">Umożliwia zaktualizowanie źródła danych.</span><span class="sxs-lookup"><span data-stu-id="be630-103">Updates a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be630-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be630-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsDataSource [-DataSource] <PSDataSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be630-105">Opis</span><span class="sxs-lookup"><span data-stu-id="be630-105">DESCRIPTION</span></span>
<span data-ttu-id="be630-106">Polecenie cmdlet **Set-AzureRmOperationalInsightsDataSource** umożliwia zaktualizowanie źródła danych.</span><span class="sxs-lookup"><span data-stu-id="be630-106">The **Set-AzureRmOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="be630-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be630-107">EXAMPLES</span></span>

## <span data-ttu-id="be630-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be630-108">PARAMETERS</span></span>

### <span data-ttu-id="be630-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="be630-109">-DataSource</span></span>
<span data-ttu-id="be630-110">Określa źródło danych, które jest aktualizowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be630-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: PSDataSource
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be630-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be630-111">-DefaultProfile</span></span>
<span data-ttu-id="be630-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="be630-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be630-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be630-113">CommonParameters</span></span>
<span data-ttu-id="be630-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be630-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be630-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be630-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be630-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be630-116">INPUTS</span></span>

### <span data-ttu-id="be630-117">PSDataSource</span><span class="sxs-lookup"><span data-stu-id="be630-117">PSDataSource</span></span>
<span data-ttu-id="be630-118">Parametr "DataSource" przyjmuje wartość typu "PSDataSource" z potoku</span><span class="sxs-lookup"><span data-stu-id="be630-118">Parameter 'DataSource' accepts value of type 'PSDataSource' from the pipeline</span></span>

## <span data-ttu-id="be630-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be630-119">OUTPUTS</span></span>

### <span data-ttu-id="be630-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="be630-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="be630-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be630-121">NOTES</span></span>
* <span data-ttu-id="be630-122">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, operacyjne, Insights</span><span class="sxs-lookup"><span data-stu-id="be630-122">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="be630-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be630-123">RELATED LINKS</span></span>

[<span data-ttu-id="be630-124">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="be630-124">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="be630-125">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="be630-125">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)


