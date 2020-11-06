---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3251e0fabb99a9f16a497a445fa010a01187108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523557"
---
# <span data-ttu-id="618b1-101">Select-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="618b1-101">Select-AzureRmProfile</span></span>

## <span data-ttu-id="618b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="618b1-102">SYNOPSIS</span></span>
<span data-ttu-id="618b1-103">Ładuje informacje o uwierzytelnianiu platformy Azure z pliku.</span><span class="sxs-lookup"><span data-stu-id="618b1-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="618b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="618b1-104">SYNTAX</span></span>

### <span data-ttu-id="618b1-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="618b1-105">InMemoryProfile</span></span>
```
Select-AzureRmProfile [-Profile] <AzureRMProfile> [<CommonParameters>]
```

### <span data-ttu-id="618b1-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="618b1-106">ProfileFromDisk</span></span>
```
Select-AzureRmProfile [-Path] <String> [<CommonParameters>]
```

## <span data-ttu-id="618b1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="618b1-107">DESCRIPTION</span></span>
<span data-ttu-id="618b1-108">Polecenie cmdlet Select-AzureRmProfile ładuje informacje uwierzytelniające z pliku w celu ustawienia środowiska i kontekstu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="618b1-108">The Select-AzureRmProfile cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="618b1-109">Polecenia cmdlet uruchomione w bieżącej sesji używają tych informacji do uwierzytelniania żądań usługi Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="618b1-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="618b1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="618b1-110">EXAMPLES</span></span>

### <span data-ttu-id="618b1-111">Przykład 1. Wybieranie profilu z PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="618b1-111">Example 1: Selecting a profile from a PSAzureProfile</span></span>
```
PS C:\> Select-AzureRmProfile -Profile (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="618b1-112">W tym przykładzie wybrano profil z PSAzureProfile, który przekazano do polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="618b1-112">This example selects a profile from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="618b1-113">Przykład 2: Wybieranie profilu z pliku JSON</span><span class="sxs-lookup"><span data-stu-id="618b1-113">Example 2: Selecting a profile from a JSON file</span></span>
```
PS C:\> Select-AzureRmProfile -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="618b1-114">W tym przykładzie wybrano profil z pliku JSON przekazanego do polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="618b1-114">This example selects a profile from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="618b1-115">Ten plik JSON można utworzyć w usłudze Save-AzureRmProfile.</span><span class="sxs-lookup"><span data-stu-id="618b1-115">This JSON file can be created from Save-AzureRmProfile.</span></span>

## <span data-ttu-id="618b1-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="618b1-116">PARAMETERS</span></span>

### <span data-ttu-id="618b1-117">-Path</span><span class="sxs-lookup"><span data-stu-id="618b1-117">-Path</span></span>
<span data-ttu-id="618b1-118">Określa ścieżkę do informacji o profilu zapisanych przy użyciu polecenia Save-AzureRMProfile.</span><span class="sxs-lookup"><span data-stu-id="618b1-118">Specifies the path to profile information saved by using Save-AzureRMProfile.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="618b1-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="618b1-119">-Profile</span></span>
<span data-ttu-id="618b1-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="618b1-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="618b1-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="618b1-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: InMemoryProfile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="618b1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="618b1-122">CommonParameters</span></span>
<span data-ttu-id="618b1-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="618b1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="618b1-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="618b1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="618b1-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="618b1-125">INPUTS</span></span>

## <span data-ttu-id="618b1-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="618b1-126">OUTPUTS</span></span>

### <span data-ttu-id="618b1-127">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="618b1-127">PSAzureProfile</span></span>

## <span data-ttu-id="618b1-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="618b1-128">NOTES</span></span>

## <span data-ttu-id="618b1-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="618b1-129">RELATED LINKS</span></span>

[<span data-ttu-id="618b1-130">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="618b1-130">Get-AzureRMContext</span></span>]()

