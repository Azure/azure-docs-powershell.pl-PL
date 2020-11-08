---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 0E5F05B3-F2B0-479C-8222-927C34140416
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74892352afe02ae5eb2f19e05704c23c489d2d75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054598"
---
# <span data-ttu-id="3798d-101">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="3798d-101">Get-AzureRemoteAppCollectionUsageDetails</span></span>

## <span data-ttu-id="3798d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3798d-102">SYNOPSIS</span></span>
<span data-ttu-id="3798d-103">Pobiera szczegóły użycia kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3798d-103">Retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="3798d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3798d-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageDetails [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-AsJob] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3798d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3798d-105">DESCRIPTION</span></span>
<span data-ttu-id="3798d-106">Polecenie cmdlet **Get-AzureRemoteAppCollectionUsageDetails** pobiera szczegóły użycia kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3798d-106">The **Get-AzureRemoteAppCollectionUsageDetails** cmdlet retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="3798d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3798d-107">EXAMPLES</span></span>

### <span data-ttu-id="3798d-108">Przykład 1: uzyskiwanie szczegółowych informacji o użyciu kolekcji</span><span class="sxs-lookup"><span data-stu-id="3798d-108">Example 1: Get usage details for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageDetails -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="3798d-109">To polecenie pobiera szczegóły użycia dla miesiąca z grudnia w roku 2014 dla kolekcji funkcji Azure RemoteApp o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="3798d-109">This command gets usage details for the month of December in the year 2014, for an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="3798d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3798d-110">PARAMETERS</span></span>

### <span data-ttu-id="3798d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3798d-111">-AsJob</span></span>
<span data-ttu-id="3798d-112">Wskazuje, że polecenie cmdlet jest uruchamiane w tle jako zadanie programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3798d-112">Indicates that the cmdlet runs in the background as a Windows PowerShell job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3798d-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="3798d-113">-CollectionName</span></span>
<span data-ttu-id="3798d-114">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3798d-114">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3798d-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="3798d-115">-Profile</span></span>
<span data-ttu-id="3798d-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3798d-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3798d-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3798d-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3798d-118">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="3798d-118">-UsageMonth</span></span>
<span data-ttu-id="3798d-119">Umożliwia określenie dwucyfrowego numeru miesiąca, dla którego mają zostać wyświetlone szczegóły użycia.</span><span class="sxs-lookup"><span data-stu-id="3798d-119">Specifies a two-digit number for the month for which to get usage details.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3798d-120">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="3798d-120">-UsageYear</span></span>
<span data-ttu-id="3798d-121">Określa czterocyfrowy rok, w którym mają zostać wyświetlone szczegóły użycia.</span><span class="sxs-lookup"><span data-stu-id="3798d-121">Specifies the four-digit year for which to get usage details.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3798d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3798d-122">CommonParameters</span></span>
<span data-ttu-id="3798d-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3798d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3798d-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3798d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3798d-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3798d-125">INPUTS</span></span>

## <span data-ttu-id="3798d-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3798d-126">OUTPUTS</span></span>

## <span data-ttu-id="3798d-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3798d-127">NOTES</span></span>

## <span data-ttu-id="3798d-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3798d-128">RELATED LINKS</span></span>

[<span data-ttu-id="3798d-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="3798d-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="3798d-130">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="3798d-130">Get-AzureRemoteAppCollectionUsageSummary</span></span>](./Get-AzureRemoteAppCollectionUsageSummary.md)


