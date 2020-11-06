---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: de676da4e276cf7e2b49558c81e9d7f6876d158b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547835"
---
# <span data-ttu-id="6a805-101">Get-AzureRmStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="6a805-101">Get-AzureRmStreamAnalyticsQuota</span></span>

## <span data-ttu-id="6a805-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a805-102">SYNOPSIS</span></span>
<span data-ttu-id="6a805-103">Pobiera informacje na temat przydziału jednostki transmisji strumieniowej dla regionu.</span><span class="sxs-lookup"><span data-stu-id="6a805-103">Gets information about the Streaming Unit quota for a region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a805-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a805-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a805-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a805-105">DESCRIPTION</span></span>
<span data-ttu-id="6a805-106">Polecenie cmdlet **Get-AzureRmStreamAnalyticsQuota** pobiera informacje na temat przydziału jednostki transmisji strumieniowej dla regionu.</span><span class="sxs-lookup"><span data-stu-id="6a805-106">The **Get-AzureRmStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="6a805-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a805-107">EXAMPLES</span></span>

### <span data-ttu-id="6a805-108">PRZYKŁAD 1: uzyskiwanie informacji na temat przydziału jednostek transmisji strumieniowej dla regionu</span><span class="sxs-lookup"><span data-stu-id="6a805-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="6a805-109">To polecenie zwraca informacje na temat przydziału jednostek transmisji strumieniowej i użytkowania w zachodnim regionie Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="6a805-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="6a805-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a805-110">PARAMETERS</span></span>

### <span data-ttu-id="6a805-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a805-111">-DefaultProfile</span></span>
<span data-ttu-id="6a805-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a805-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a805-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6a805-113">-Location</span></span>
<span data-ttu-id="6a805-114">Określa nazwę obszaru platformy Azure lub lokalizacji centrum danych, dla którego mają być uzyskiwane informacje o przydziałach jednostki transmisji strumieniowej.</span><span class="sxs-lookup"><span data-stu-id="6a805-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="6a805-115">Zobacz https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services listę obsługiwanych regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6a805-115">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a805-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a805-116">CommonParameters</span></span>
<span data-ttu-id="6a805-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a805-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a805-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a805-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a805-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a805-119">INPUTS</span></span>

### <span data-ttu-id="6a805-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6a805-120">None</span></span>
<span data-ttu-id="6a805-121">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6a805-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6a805-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a805-122">OUTPUTS</span></span>

### <span data-ttu-id="6a805-123">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. StreamAnalytics. MODELES. PSQuota, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. modele. PSQuota</span><span class="sxs-lookup"><span data-stu-id="6a805-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="6a805-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a805-124">NOTES</span></span>

## <span data-ttu-id="6a805-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a805-125">RELATED LINKS</span></span>

[<span data-ttu-id="6a805-126">Polecenia cmdlet usługi Analiza strumienia Azure</span><span class="sxs-lookup"><span data-stu-id="6a805-126">Azure Stream Analytics Cmdlets</span></span>](./AzureRM.StreamAnalytics.md)


