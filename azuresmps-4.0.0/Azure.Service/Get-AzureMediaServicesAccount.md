---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055301"
---
# <span data-ttu-id="51f2a-101">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="51f2a-101">Get-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="51f2a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="51f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="51f2a-103">Pobiera dostępne konta usługi Azure Media Services.</span><span class="sxs-lookup"><span data-stu-id="51f2a-103">Gets the available Azure Media Services accounts.</span></span>

<span data-ttu-id="51f2a-104">**Uwaga:** Ta wersja jest przestarzała, sprawdź [nowszą wersję](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="51f2a-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="51f2a-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="51f2a-105">SYNTAX</span></span>

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="51f2a-106">Opis</span><span class="sxs-lookup"><span data-stu-id="51f2a-106">DESCRIPTION</span></span>
<span data-ttu-id="51f2a-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="51f2a-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="51f2a-108">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="51f2a-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="51f2a-109">Aby wyświetlić listę wszystkich kont, użyj `Get-AzureMediaServicesAccount` polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51f2a-109">To list all the accounts, use the `Get-AzureMediaServicesAccount` cmdlet.</span></span>
<span data-ttu-id="51f2a-110">Aby uzyskać bardziej szczegółowe informacje na temat określonego konta, użyj `Get-AzureMediaServicesAccount -Name YourAccountName` polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51f2a-110">To get more detailed information about a specific account, use the `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet.</span></span>

## <span data-ttu-id="51f2a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="51f2a-111">EXAMPLES</span></span>

### <span data-ttu-id="51f2a-112">Przykład 1: Lista wszystkich kont usług multimedialnych</span><span class="sxs-lookup"><span data-stu-id="51f2a-112">Example 1: List all Media Services accounts</span></span>
```
PS C:\> Get-AzureMediaServicesAccount
```

<span data-ttu-id="51f2a-113">To polecenie wyświetla listę wszystkich dostępnych kont usług multimedialnych.</span><span class="sxs-lookup"><span data-stu-id="51f2a-113">This command lists all available Media Services accounts.</span></span>

### <span data-ttu-id="51f2a-114">Przykład 2: uzyskiwanie szczegółowych informacji o koncie usług multimedialnych</span><span class="sxs-lookup"><span data-stu-id="51f2a-114">Example 2: Get detailed information about a Media Services account</span></span>
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

<span data-ttu-id="51f2a-115">To polecenie wyświetla właściwości konta usług multimedialnych.</span><span class="sxs-lookup"><span data-stu-id="51f2a-115">This command displays properties of a Media Services account.</span></span>

## <span data-ttu-id="51f2a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="51f2a-116">PARAMETERS</span></span>

### <span data-ttu-id="51f2a-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="51f2a-117">-Name</span></span>
<span data-ttu-id="51f2a-118">Nazwa konta usług multimedialnych.</span><span class="sxs-lookup"><span data-stu-id="51f2a-118">The Media Services account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51f2a-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="51f2a-119">-Profile</span></span>
<span data-ttu-id="51f2a-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51f2a-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51f2a-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="51f2a-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51f2a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f2a-122">CommonParameters</span></span>
<span data-ttu-id="51f2a-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51f2a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f2a-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51f2a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f2a-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51f2a-125">INPUTS</span></span>

## <span data-ttu-id="51f2a-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="51f2a-126">OUTPUTS</span></span>

## <span data-ttu-id="51f2a-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="51f2a-127">NOTES</span></span>

## <span data-ttu-id="51f2a-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51f2a-128">RELATED LINKS</span></span>

[<span data-ttu-id="51f2a-129">Jak używać usługi Azure PowerShell dla usług multimedialnych</span><span class="sxs-lookup"><span data-stu-id="51f2a-129">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


