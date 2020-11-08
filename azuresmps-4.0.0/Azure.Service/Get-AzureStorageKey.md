---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 35588231-CBAC-4411-9531-9A06BD298ACA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7fdcad4b3a0f41f0589e49d4b33a767b93267855
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054514"
---
# <span data-ttu-id="19656-101">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="19656-101">Get-AzureStorageKey</span></span>

## <span data-ttu-id="19656-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19656-102">SYNOPSIS</span></span>
<span data-ttu-id="19656-103">Zwraca klucze konta podstawowego i pomocniczego magazynu dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="19656-103">Returns the primary and secondary storage account keys for an Azure storage account.</span></span>

## <span data-ttu-id="19656-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19656-104">SYNTAX</span></span>

```
Get-AzureStorageKey [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="19656-105">Opis</span><span class="sxs-lookup"><span data-stu-id="19656-105">DESCRIPTION</span></span>
<span data-ttu-id="19656-106">Polecenie cmdlet **Get-AzureStorageKey** zwraca obiekt o nazwie konta usługi Azure Storage, podstawowym kluczu konta oraz kluczu konta pomocniczego określonego konta usługi Azure Storage jako właściwości.</span><span class="sxs-lookup"><span data-stu-id="19656-106">The **Get-AzureStorageKey** cmdlet returns an object with the Azure Storage account name, the primary account key, and the secondary account key of the specified Azure storage account as properties.</span></span>

## <span data-ttu-id="19656-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19656-107">EXAMPLES</span></span>

### <span data-ttu-id="19656-108">Przykład 1: uzyskiwanie obiektu zawierającego klucze magazynu podstawowego i pomocniczego</span><span class="sxs-lookup"><span data-stu-id="19656-108">Example 1: Get an object that contains primary and secondary storage keys</span></span>
```
PS C:\> Get-AzureStorageKey -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="19656-109">To polecenie pobiera obiekt z podstawowym i pomocniczym kluczem magazynu dla konta magazynu usługi ContosoStore01.</span><span class="sxs-lookup"><span data-stu-id="19656-109">This command gets an object with the primary and secondary storage keys for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="19656-110">Przykład 2: Uzyskiwanie klucza podstawowego konta magazynu i przechowywanie go w zmiennej</span><span class="sxs-lookup"><span data-stu-id="19656-110">Example 2: Get the primary storage account key and store it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = (Get-AzureStorageKey -StorageAccountName "ContosoStore01").Primary
```

<span data-ttu-id="19656-111">To polecenie powoduje umieszczenie klucza podstawowego konta magazynu dla konta magazynu ContosoStore01 w zmiennej $ContosoStoreKey.</span><span class="sxs-lookup"><span data-stu-id="19656-111">This command puts the primary storage account key for the ContosoStore01 storage account in the $ContosoStoreKey variable.</span></span>

## <span data-ttu-id="19656-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19656-112">PARAMETERS</span></span>

### <span data-ttu-id="19656-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="19656-113">-InformationAction</span></span>
<span data-ttu-id="19656-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="19656-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="19656-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="19656-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19656-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="19656-116">Continue</span></span>
- <span data-ttu-id="19656-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="19656-117">Ignore</span></span>
- <span data-ttu-id="19656-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="19656-118">Inquire</span></span>
- <span data-ttu-id="19656-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="19656-119">SilentlyContinue</span></span>
- <span data-ttu-id="19656-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="19656-120">Stop</span></span>
- <span data-ttu-id="19656-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="19656-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19656-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="19656-122">-InformationVariable</span></span>
<span data-ttu-id="19656-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="19656-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19656-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="19656-124">-Profile</span></span>
<span data-ttu-id="19656-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19656-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="19656-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="19656-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="19656-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="19656-127">-StorageAccountName</span></span>
<span data-ttu-id="19656-128">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="19656-128">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19656-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19656-129">CommonParameters</span></span>
<span data-ttu-id="19656-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19656-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19656-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19656-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19656-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19656-132">INPUTS</span></span>

## <span data-ttu-id="19656-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19656-133">OUTPUTS</span></span>

## <span data-ttu-id="19656-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19656-134">NOTES</span></span>
* <span data-ttu-id="19656-135">Aby uzyskać pomoc dotyczącą Node.js, użyj `help node-dev` polecenia.</span><span class="sxs-lookup"><span data-stu-id="19656-135">To get help with Node.js, use the `help node-dev` command.</span></span> <span data-ttu-id="19656-136">Aby uzyskać pomoc dotyczącą rozszerzeń PHP, użyj `help php-dev` polecenia.</span><span class="sxs-lookup"><span data-stu-id="19656-136">For help with PHP extensions, use the `help php-dev` command.</span></span>

## <span data-ttu-id="19656-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19656-137">RELATED LINKS</span></span>

[<span data-ttu-id="19656-138">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19656-138">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="19656-139">Nowe — AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19656-139">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="19656-140">Nowe — AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="19656-140">New-AzureStorageKey</span></span>](./New-AzureStorageKey.md)

[<span data-ttu-id="19656-141">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19656-141">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)

[<span data-ttu-id="19656-142">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19656-142">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


