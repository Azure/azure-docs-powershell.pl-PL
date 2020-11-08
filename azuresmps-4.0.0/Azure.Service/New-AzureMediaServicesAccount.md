---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6C4081EE-0BCD-4285-8ABB-778BD95BFE4F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37f6e5b1152af79b2fc199199bf2b872bfbfa4ec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054877"
---
# <span data-ttu-id="b7a7b-101">New-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b7a7b-101">New-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="b7a7b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7a7b-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a7b-103">Tworzy konto usługi Azure Media Services.</span><span class="sxs-lookup"><span data-stu-id="b7a7b-103">Creates an Azure Media Services account.</span></span>

<span data-ttu-id="b7a7b-104">**Uwaga:** Ta wersja jest przestarzała, sprawdź [nowszą wersję](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="b7a7b-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="b7a7b-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7a7b-105">SYNTAX</span></span>

```
New-AzureMediaServicesAccount -Name <String> -Location <String> -StorageAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b7a7b-106">Opis</span><span class="sxs-lookup"><span data-stu-id="b7a7b-106">DESCRIPTION</span></span>
<span data-ttu-id="b7a7b-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a7b-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b7a7b-108">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b7a7b-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b7a7b-109">Polecenie cmdlet **New-AzureMediaServicesAccount** tworzy nowe konto usług multimedialnych z określoną nazwą konta usług multimedialnych, lokalizacją Datacenter, w której chcesz utworzyć konto, oraz nazwą istniejącego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b7a7b-109">The **New-AzureMediaServicesAccount** cmdlet creates a new Media Services account with the specified Media Services account name, datacenter location where you want to create the account, and an existing storage account name.</span></span>
<span data-ttu-id="b7a7b-110">Konto magazynu musi znajdować się w tym samym centrum danych co nowe konto usług multimedialnych.</span><span class="sxs-lookup"><span data-stu-id="b7a7b-110">The storage account has to be located in the same data center as the new Media Services account.</span></span>

## <span data-ttu-id="b7a7b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7a7b-111">EXAMPLES</span></span>

### <span data-ttu-id="b7a7b-112">Przykład 1: Tworzenie nowego konta usług multimedialnych</span><span class="sxs-lookup"><span data-stu-id="b7a7b-112">Example 1: Create a new Media Services account</span></span>
```
PS C:\> New-AzureMediaServicesAccount -Name "mediaserviceaccount" -StorageAccountName "storageaccount " -Location "West US"
```

## <span data-ttu-id="b7a7b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7a7b-113">PARAMETERS</span></span>

### <span data-ttu-id="b7a7b-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b7a7b-114">-Location</span></span>
<span data-ttu-id="b7a7b-115">Określa lokalizację centrum usług multimedialnych.</span><span class="sxs-lookup"><span data-stu-id="b7a7b-115">Specifies the Media Services datacenter location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a7b-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b7a7b-116">-Name</span></span>
<span data-ttu-id="b7a7b-117">Określa nazwę konta usług multimedialnych.</span><span class="sxs-lookup"><span data-stu-id="b7a7b-117">Specifies the Media Services account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a7b-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="b7a7b-118">-Profile</span></span>
<span data-ttu-id="b7a7b-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7a7b-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b7a7b-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b7a7b-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b7a7b-121">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b7a7b-121">-StorageAccountName</span></span>
<span data-ttu-id="b7a7b-122">Określa nazwę konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b7a7b-122">Specifies the storage account name.</span></span>
<span data-ttu-id="b7a7b-123">Konto magazynu musi już istnieć w tym samym centrum danych, co nowe konto usług multimedialnych.</span><span class="sxs-lookup"><span data-stu-id="b7a7b-123">The storage account must already exist in the same datacenter as the new Media Services account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a7b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a7b-124">CommonParameters</span></span>
<span data-ttu-id="b7a7b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7a7b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a7b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7a7b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a7b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7a7b-127">INPUTS</span></span>

## <span data-ttu-id="b7a7b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7a7b-128">OUTPUTS</span></span>

## <span data-ttu-id="b7a7b-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7a7b-129">NOTES</span></span>

## <span data-ttu-id="b7a7b-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7a7b-130">RELATED LINKS</span></span>

[<span data-ttu-id="b7a7b-131">Jak używać usługi Azure PowerShell dla usług multimedialnych</span><span class="sxs-lookup"><span data-stu-id="b7a7b-131">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="b7a7b-132">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b7a7b-132">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="b7a7b-133">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b7a7b-133">Remove-AzureMediaServicesAccount</span></span>](./Remove-AzureMediaServicesAccount.md)


