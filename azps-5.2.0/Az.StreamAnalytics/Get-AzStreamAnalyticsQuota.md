---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: abce6b39b0dfa77ed4aa815ed9551b3ebff427ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366401"
---
# <span data-ttu-id="85bda-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="85bda-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="85bda-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85bda-102">SYNOPSIS</span></span>
<span data-ttu-id="85bda-103">Pobiera informacje na temat przydziału jednostki transmisji strumieniowej dla regionu.</span><span class="sxs-lookup"><span data-stu-id="85bda-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="85bda-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85bda-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85bda-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85bda-105">DESCRIPTION</span></span>
<span data-ttu-id="85bda-106">Polecenie cmdlet **Get-AzStreamAnalyticsQuota** pobiera informacje na temat przydziału jednostki transmisji strumieniowej dla regionu.</span><span class="sxs-lookup"><span data-stu-id="85bda-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="85bda-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85bda-107">EXAMPLES</span></span>

### <span data-ttu-id="85bda-108">PRZYKŁAD 1: uzyskiwanie informacji na temat przydziału jednostek transmisji strumieniowej dla regionu</span><span class="sxs-lookup"><span data-stu-id="85bda-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="85bda-109">To polecenie zwraca informacje na temat przydziału jednostek transmisji strumieniowej i użytkowania w zachodnim regionie Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="85bda-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="85bda-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85bda-110">PARAMETERS</span></span>

### <span data-ttu-id="85bda-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85bda-111">-DefaultProfile</span></span>
<span data-ttu-id="85bda-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="85bda-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85bda-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="85bda-113">-Location</span></span>
<span data-ttu-id="85bda-114">Określa nazwę obszaru platformy Azure lub lokalizacji centrum danych, dla którego mają być uzyskiwane informacje o przydziałach jednostki transmisji strumieniowej.</span><span class="sxs-lookup"><span data-stu-id="85bda-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="85bda-115">Zobacz http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services listę obsługiwanych regionów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="85bda-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="85bda-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85bda-116">CommonParameters</span></span>
<span data-ttu-id="85bda-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85bda-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85bda-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85bda-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85bda-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85bda-119">INPUTS</span></span>

### <span data-ttu-id="85bda-120">System. String</span><span class="sxs-lookup"><span data-stu-id="85bda-120">System.String</span></span>

## <span data-ttu-id="85bda-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85bda-121">OUTPUTS</span></span>

### <span data-ttu-id="85bda-122">Microsoft. Azure. Commands. StreamAnalytics. models. PSQuota</span><span class="sxs-lookup"><span data-stu-id="85bda-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="85bda-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85bda-123">NOTES</span></span>

## <span data-ttu-id="85bda-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85bda-124">RELATED LINKS</span></span>

[<span data-ttu-id="85bda-125">Polecenia cmdlet usługi Analiza strumienia Azure</span><span class="sxs-lookup"><span data-stu-id="85bda-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


