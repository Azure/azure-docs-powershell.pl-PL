---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8EF86C66-498F-4183-9070-F178628483F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91c32ca5207efdff7fa65fbba599f44d276dab6d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055296"
---
# <span data-ttu-id="3d5f1-101">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="3d5f1-101">Get-AzureRemoteAppCollectionUsageSummary</span></span>

## <span data-ttu-id="3d5f1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d5f1-102">SYNOPSIS</span></span>
<span data-ttu-id="3d5f1-103">Pobiera Podsumowanie użycia kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3d5f1-103">Retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="3d5f1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d5f1-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageSummary [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3d5f1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3d5f1-105">DESCRIPTION</span></span>
<span data-ttu-id="3d5f1-106">Polecenie cmdlet **Get-AzureRemoteAppCollectionUsageSummary** pobiera podsumowanie użycia kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3d5f1-106">The **Get-AzureRemoteAppCollectionUsageSummary** cmdlet retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="3d5f1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d5f1-107">EXAMPLES</span></span>

### <span data-ttu-id="3d5f1-108">Przykład 1: Uzyskaj Podsumowanie użycia</span><span class="sxs-lookup"><span data-stu-id="3d5f1-108">Example 1: Get a usage summary</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageSummary -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="3d5f1-109">To polecenie pobiera podsumowanie użycia za miesiąc z grudnia w roku 2014 dla kolekcji o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="3d5f1-109">This command gets a usage summary for the month of December in the year 2014, for a collection named Contoso.</span></span>

## <span data-ttu-id="3d5f1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d5f1-110">PARAMETERS</span></span>

### <span data-ttu-id="3d5f1-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="3d5f1-111">-CollectionName</span></span>
<span data-ttu-id="3d5f1-112">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3d5f1-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="3d5f1-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="3d5f1-113">-Profile</span></span>
<span data-ttu-id="3d5f1-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d5f1-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3d5f1-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3d5f1-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3d5f1-116">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="3d5f1-116">-UsageMonth</span></span>
<span data-ttu-id="3d5f1-117">Określa dwa cyfry dla miesiąca, dla którego ma zostać wyświetlone podsumowanie użycia.</span><span class="sxs-lookup"><span data-stu-id="3d5f1-117">Specifies a two digit number for the month for which to get a usage summary.</span></span>
<span data-ttu-id="3d5f1-118">Jeśli ten parametr nie jest określony, to polecenie cmdlet umożliwia użycie bieżącego miesiąca.</span><span class="sxs-lookup"><span data-stu-id="3d5f1-118">If this parameter is not specified, this cmdlet provides usage for the current month.</span></span>

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

### <span data-ttu-id="3d5f1-119">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="3d5f1-119">-UsageYear</span></span>
<span data-ttu-id="3d5f1-120">Określa czterocyfrowy rok, dla którego ma zostać wyświetlone podsumowanie użycia.</span><span class="sxs-lookup"><span data-stu-id="3d5f1-120">Specifies the four-digit year for which to get a usage summary.</span></span>
<span data-ttu-id="3d5f1-121">Jeśli ten parametr nie zostanie określony, zostanie użyte Podsumowanie użycia dla bieżącego roku.</span><span class="sxs-lookup"><span data-stu-id="3d5f1-121">If this parameter is not specified, this cmdlet provides a usage summary for the current year will be used.</span></span>

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

### <span data-ttu-id="3d5f1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d5f1-122">CommonParameters</span></span>
<span data-ttu-id="3d5f1-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d5f1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d5f1-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d5f1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d5f1-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d5f1-125">INPUTS</span></span>

## <span data-ttu-id="3d5f1-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d5f1-126">OUTPUTS</span></span>

## <span data-ttu-id="3d5f1-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d5f1-127">NOTES</span></span>

## <span data-ttu-id="3d5f1-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d5f1-128">RELATED LINKS</span></span>

[<span data-ttu-id="3d5f1-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="3d5f1-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="3d5f1-130">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="3d5f1-130">Get-AzureRemoteAppCollectionUsageDetails</span></span>](./Get-AzureRemoteAppCollectionUsageDetails.md)


