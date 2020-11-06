---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: 281bc9cd39891ab2794901d0425b299cc72c4644
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524241"
---
# <span data-ttu-id="34e7a-101">Get-AzureRmStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="34e7a-101">Get-AzureRmStreamAnalyticsQuota</span></span>

## <span data-ttu-id="34e7a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="34e7a-103">Pobiera informacje na temat przydziału jednostki transmisji strumieniowej dla regionu.</span><span class="sxs-lookup"><span data-stu-id="34e7a-103">Gets information about the Streaming Unit quota for a region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34e7a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34e7a-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34e7a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34e7a-105">DESCRIPTION</span></span>
<span data-ttu-id="34e7a-106">Polecenie cmdlet **Get-AzureRmStreamAnalyticsQuota** pobiera informacje na temat przydziału jednostki transmisji strumieniowej dla regionu.</span><span class="sxs-lookup"><span data-stu-id="34e7a-106">The **Get-AzureRmStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="34e7a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34e7a-107">EXAMPLES</span></span>

### <span data-ttu-id="34e7a-108">PRZYKŁAD 1: uzyskiwanie informacji na temat przydziału jednostek transmisji strumieniowej dla regionu</span><span class="sxs-lookup"><span data-stu-id="34e7a-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="34e7a-109">To polecenie zwraca informacje na temat przydziału jednostek transmisji strumieniowej i użytkowania w zachodnim regionie Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="34e7a-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="34e7a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34e7a-110">PARAMETERS</span></span>

### <span data-ttu-id="34e7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e7a-111">-DefaultProfile</span></span>
<span data-ttu-id="34e7a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34e7a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34e7a-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="34e7a-113">-Location</span></span>
<span data-ttu-id="34e7a-114">Określa nazwę obszaru platformy Azure lub lokalizacji centrum danych, dla którego mają być uzyskiwane informacje o przydziałach jednostki transmisji strumieniowej.</span><span class="sxs-lookup"><span data-stu-id="34e7a-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="34e7a-115">Zobacz https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services listę obsługiwanych regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="34e7a-115">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="34e7a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e7a-116">CommonParameters</span></span>
<span data-ttu-id="34e7a-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e7a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e7a-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34e7a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e7a-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34e7a-119">INPUTS</span></span>

### <span data-ttu-id="34e7a-120">System. String</span><span class="sxs-lookup"><span data-stu-id="34e7a-120">System.String</span></span>

## <span data-ttu-id="34e7a-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34e7a-121">OUTPUTS</span></span>

### <span data-ttu-id="34e7a-122">Microsoft. Azure. Commands. StreamAnalytics. models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="34e7a-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="34e7a-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34e7a-123">NOTES</span></span>

## <span data-ttu-id="34e7a-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34e7a-124">RELATED LINKS</span></span>

[<span data-ttu-id="34e7a-125">Polecenia cmdlet usługi Analiza strumienia Azure</span><span class="sxs-lookup"><span data-stu-id="34e7a-125">Azure Stream Analytics Cmdlets</span></span>](./AzureRM.StreamAnalytics.md)


