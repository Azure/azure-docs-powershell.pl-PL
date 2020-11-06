---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
ms.openlocfilehash: 198f0db3cab8b2e0f6e8f9b466ac3e0027e4638c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545292"
---
# <span data-ttu-id="21d58-101">Get-AzureRmHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="21d58-101">Get-AzureRmHDInsightProperties</span></span>

## <span data-ttu-id="21d58-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21d58-102">SYNOPSIS</span></span>
<span data-ttu-id="21d58-103">Pobiera właściwości usługi HDInsight, takie jak dostępne lokalizacje i pojemność.</span><span class="sxs-lookup"><span data-stu-id="21d58-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21d58-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21d58-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightProperties [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21d58-105">Opis</span><span class="sxs-lookup"><span data-stu-id="21d58-105">DESCRIPTION</span></span>
<span data-ttu-id="21d58-106">Polecenie cmdlet **Get-AzureRmHDInsightProperties** pobiera właściwości specyficzne dla usługi Azure HDInsight, takie jak lista dostępnych lokalizacji, wersje klastra usługi HDInsight i dostępne zdolności obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="21d58-106">The **Get-AzureRmHDInsightProperties** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="21d58-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21d58-107">EXAMPLES</span></span>

### <span data-ttu-id="21d58-108">Przykład 1: uzyskiwanie właściwości klastra usługi Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="21d58-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightProperties -Location "East US 2"
```

<span data-ttu-id="21d58-109">To polecenie pobiera właściwości z usługi HDInsight z lokalizacji wschód US 2.</span><span class="sxs-lookup"><span data-stu-id="21d58-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="21d58-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21d58-110">PARAMETERS</span></span>

### <span data-ttu-id="21d58-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d58-111">-DefaultProfile</span></span>
<span data-ttu-id="21d58-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="21d58-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21d58-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="21d58-113">-Location</span></span>
<span data-ttu-id="21d58-114">Określa lokalizację, w której mają zostać pobrane właściwości usługi HDInsight.</span><span class="sxs-lookup"><span data-stu-id="21d58-114">Specifies the location for which to fetch HDInsight properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21d58-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d58-115">CommonParameters</span></span>
<span data-ttu-id="21d58-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21d58-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d58-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21d58-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d58-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21d58-118">INPUTS</span></span>

### <span data-ttu-id="21d58-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="21d58-119">None</span></span>

## <span data-ttu-id="21d58-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21d58-120">OUTPUTS</span></span>

### <span data-ttu-id="21d58-121">Microsoft. Azure. Management. HDInsight. MODELES. CapabilitiesResponse</span><span class="sxs-lookup"><span data-stu-id="21d58-121">Microsoft.Azure.Management.HDInsight.Models.CapabilitiesResponse</span></span>

## <span data-ttu-id="21d58-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21d58-122">NOTES</span></span>

## <span data-ttu-id="21d58-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21d58-123">RELATED LINKS</span></span>
