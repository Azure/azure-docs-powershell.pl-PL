---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055295"
---
# <span data-ttu-id="2408a-101">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="2408a-101">Get-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="2408a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2408a-102">SYNOPSIS</span></span>
<span data-ttu-id="2408a-103">Pobiera informacje o kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="2408a-103">Retrieves information about an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="2408a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2408a-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2408a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2408a-105">DESCRIPTION</span></span>
<span data-ttu-id="2408a-106">Polecenie cmdlet **Get-AzureRemoteAppCollection** pobiera informacje o kolekcjach funkcji Azure RemoteApp na platformie Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2408a-106">The **Get-AzureRemoteAppCollection** cmdlet retrieves information about Azure RemoteApp collections in Microsoft Azure.</span></span>
<span data-ttu-id="2408a-107">Zwraca obiekt z informacją dotyczącą określonej kolekcji lub, jeśli kolekcja nie jest określona, dla wszystkich kolekcji w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2408a-107">It returns an object with information on a specific collection, or if no collection is specified, for all the collections in the current subscription.</span></span>

## <span data-ttu-id="2408a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2408a-108">EXAMPLES</span></span>

### <span data-ttu-id="2408a-109">Przykład 1: Pobieranie listy wszystkich kolekcji</span><span class="sxs-lookup"><span data-stu-id="2408a-109">Example 1: Get a list of all collections</span></span>
```
PS C:\> Get-AzureRemoteAppCollection
```

<span data-ttu-id="2408a-110">To polecenie zwraca listę wszystkich kolekcji funkcji RemoteApp w usłudze Azure w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2408a-110">This command returns a list of all Azure RemoteApp collections in the subscription.</span></span>

### <span data-ttu-id="2408a-111">Przykład 2: uzyskiwanie informacji o określonej kolekcji</span><span class="sxs-lookup"><span data-stu-id="2408a-111">Example 2: Get information about a specified collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

<span data-ttu-id="2408a-112">To polecenie zwraca informacje o kolekcji funkcji Azure RemoteApp o nazwie ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="2408a-112">This command returns information about the Azure RemoteApp collection named ContosoApps.</span></span>

### <span data-ttu-id="2408a-113">Przykład 3: Pobieranie listy kolekcji przy użyciu symboli wieloznacznych</span><span class="sxs-lookup"><span data-stu-id="2408a-113">Example 3: Get a list of collections by using a wildcard</span></span>
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

<span data-ttu-id="2408a-114">To polecenie zwraca listę wszystkich funkcji finansowych dopasowania kolekcji usługi Azure RemoteApp \*.</span><span class="sxs-lookup"><span data-stu-id="2408a-114">This command returns a list of all Azure RemoteApp collections matching Finance\*.</span></span>

## <span data-ttu-id="2408a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2408a-115">PARAMETERS</span></span>

### <span data-ttu-id="2408a-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="2408a-116">-CollectionName</span></span>
<span data-ttu-id="2408a-117">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="2408a-117">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="2408a-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="2408a-118">-Profile</span></span>
<span data-ttu-id="2408a-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2408a-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2408a-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2408a-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2408a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2408a-121">CommonParameters</span></span>
<span data-ttu-id="2408a-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2408a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2408a-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2408a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2408a-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2408a-124">INPUTS</span></span>

## <span data-ttu-id="2408a-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2408a-125">OUTPUTS</span></span>

## <span data-ttu-id="2408a-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2408a-126">NOTES</span></span>

## <span data-ttu-id="2408a-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2408a-127">RELATED LINKS</span></span>

[<span data-ttu-id="2408a-128">Nowe — AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="2408a-128">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="2408a-129">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="2408a-129">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="2408a-130">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="2408a-130">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="2408a-131">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="2408a-131">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


