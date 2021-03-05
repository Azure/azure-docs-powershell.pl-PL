---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: 8583227cee19a9429a7dfe4cd6bd8678e72d33ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973850"
---
# <span data-ttu-id="4626a-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="4626a-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="4626a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4626a-102">SYNOPSIS</span></span>
<span data-ttu-id="4626a-103">Pobiera informacje na temat przydziału jednostki strumieniowej dla regionu.</span><span class="sxs-lookup"><span data-stu-id="4626a-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="4626a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4626a-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4626a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4626a-105">DESCRIPTION</span></span>
<span data-ttu-id="4626a-106">Polecenie **cmdlet Get-AzStreamAnalyticsQuota** pobiera informacje o przydziałie jednostki strumieniowej dla regionu.</span><span class="sxs-lookup"><span data-stu-id="4626a-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="4626a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4626a-107">EXAMPLES</span></span>

### <span data-ttu-id="4626a-108">PRZYKŁAD 1. Uzyskiwanie informacji o przydziałie jednostki strumieniowej dla regionu</span><span class="sxs-lookup"><span data-stu-id="4626a-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="4626a-109">To polecenie zwraca informacje o przydziałach i użyciu jednostek strumieniowych w regionie Zachód Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="4626a-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="4626a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4626a-110">PARAMETERS</span></span>

### <span data-ttu-id="4626a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4626a-111">-DefaultProfile</span></span>
<span data-ttu-id="4626a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4626a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4626a-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4626a-113">-Location</span></span>
<span data-ttu-id="4626a-114">Określa nazwę regionu platformy Azure lub lokalizacji centrum danych, dla której mają być zbierane informacje o przydziałach jednostki strumieniowej.</span><span class="sxs-lookup"><span data-stu-id="4626a-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="4626a-115">Zobacz http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services listę obsługiwanych regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4626a-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="4626a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4626a-116">CommonParameters</span></span>
<span data-ttu-id="4626a-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4626a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4626a-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4626a-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4626a-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4626a-119">INPUTS</span></span>

### <span data-ttu-id="4626a-120">System.String</span><span class="sxs-lookup"><span data-stu-id="4626a-120">System.String</span></span>

## <span data-ttu-id="4626a-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4626a-121">OUTPUTS</span></span>

### <span data-ttu-id="4626a-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span><span class="sxs-lookup"><span data-stu-id="4626a-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="4626a-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4626a-123">NOTES</span></span>

## <span data-ttu-id="4626a-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4626a-124">RELATED LINKS</span></span>

[<span data-ttu-id="4626a-125">Polecenia cmdlet usługi Azure Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="4626a-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


