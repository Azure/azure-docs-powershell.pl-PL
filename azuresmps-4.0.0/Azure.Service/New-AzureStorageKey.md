---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 09ABE9E2-1080-4DEF-92DD-B8FF4C8B308C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9afdaafa57592239d0c24870e4459d650fac84c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055169"
---
# <span data-ttu-id="2f673-101">New-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="2f673-101">New-AzureStorageKey</span></span>

## <span data-ttu-id="2f673-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f673-102">SYNOPSIS</span></span>
<span data-ttu-id="2f673-103">Generuje klucze magazynowania dla konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2f673-103">Regenerates storage keys for an Azure storage account.</span></span>

## <span data-ttu-id="2f673-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f673-104">SYNTAX</span></span>

```
New-AzureStorageKey [-KeyType] <String> [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2f673-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2f673-105">DESCRIPTION</span></span>
<span data-ttu-id="2f673-106">Polecenie cmdlet **New-AzureStorageKey** generuje klucz podstawowy lub pomocniczy konta usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="2f673-106">The **New-AzureStorageKey** cmdlet regenerates the primary or secondary key for an Azure Storage account.</span></span>
<span data-ttu-id="2f673-107">Zwraca obiekt zawierający nazwę konta magazynu, klucz podstawowy i klucz pomocniczy jako właściwości.</span><span class="sxs-lookup"><span data-stu-id="2f673-107">It returns an object that contains the storage account name, primary key, and secondary key as properties.</span></span>

## <span data-ttu-id="2f673-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f673-108">EXAMPLES</span></span>

### <span data-ttu-id="2f673-109">Przykład 1. Regeneruj podstawowy klucz magazynu</span><span class="sxs-lookup"><span data-stu-id="2f673-109">Example 1: Regenerate a primary storage key</span></span>
```
PS C:\> New-AzureStorageKey -KeyType "Primary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="2f673-110">To polecenie generuje podstawowy klucz magazynu dla konta magazynu usługi ContosoStore01.</span><span class="sxs-lookup"><span data-stu-id="2f673-110">This command regenerates the primary storage key for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="2f673-111">Przykład 2: ponowne wygenerowanie pomocniczego klucza magazynu i zapisanie go w zmiennej</span><span class="sxs-lookup"><span data-stu-id="2f673-111">Example 2: Regenerate a secondary storage key and save it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = New-AzureStorageKey -KeyType "Secondary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="2f673-112">To polecenie powoduje ponowne wygenerowanie pomocniczego klucza magazynu dla konta magazynu usługi ContosoStore01 i przechowywanie zaktualizowanych informacji o kluczu konta magazynu w $ContosoStoreKey.</span><span class="sxs-lookup"><span data-stu-id="2f673-112">This command regenerate the secondary storage key for the ContosoStore01 storage account and stores the updated storage account key information in the $ContosoStoreKey.</span></span>

## <span data-ttu-id="2f673-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f673-113">PARAMETERS</span></span>

### <span data-ttu-id="2f673-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2f673-114">-InformationAction</span></span>
<span data-ttu-id="2f673-115">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="2f673-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2f673-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2f673-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2f673-117">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="2f673-117">Continue</span></span>
- <span data-ttu-id="2f673-118">Ignorować</span><span class="sxs-lookup"><span data-stu-id="2f673-118">Ignore</span></span>
- <span data-ttu-id="2f673-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="2f673-119">Inquire</span></span>
- <span data-ttu-id="2f673-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2f673-120">SilentlyContinue</span></span>
- <span data-ttu-id="2f673-121">Przestaw</span><span class="sxs-lookup"><span data-stu-id="2f673-121">Stop</span></span>
- <span data-ttu-id="2f673-122">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="2f673-122">Suspend</span></span>

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

### <span data-ttu-id="2f673-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2f673-123">-InformationVariable</span></span>
<span data-ttu-id="2f673-124">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="2f673-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2f673-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="2f673-125">-KeyType</span></span>
<span data-ttu-id="2f673-126">Określa klucz, który należy wygenerować.</span><span class="sxs-lookup"><span data-stu-id="2f673-126">Specifies which key to regenerate.</span></span>
<span data-ttu-id="2f673-127">Prawidłowe wartości: podstawowy i pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="2f673-127">Valid values are: Primary and Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f673-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="2f673-128">-Profile</span></span>
<span data-ttu-id="2f673-129">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f673-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2f673-130">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2f673-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2f673-131">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2f673-131">-StorageAccountName</span></span>
<span data-ttu-id="2f673-132">Określa nazwę konta usługi Azure Storage, dla którego ma zostać ponownie wygenerowany klucz.</span><span class="sxs-lookup"><span data-stu-id="2f673-132">Specifies the name of the Azure Storage account for which to regenerate a key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f673-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f673-133">CommonParameters</span></span>
<span data-ttu-id="2f673-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f673-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f673-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f673-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f673-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f673-136">INPUTS</span></span>

## <span data-ttu-id="2f673-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f673-137">OUTPUTS</span></span>

### <span data-ttu-id="2f673-138">StorageServiceKeys</span><span class="sxs-lookup"><span data-stu-id="2f673-138">StorageServiceKeys</span></span>

## <span data-ttu-id="2f673-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f673-139">NOTES</span></span>

## <span data-ttu-id="2f673-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f673-140">RELATED LINKS</span></span>

[<span data-ttu-id="2f673-141">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="2f673-141">Get-AzureStorageKey</span></span>](./Get-AzureStorageKey.md)


