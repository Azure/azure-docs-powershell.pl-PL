---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4696BB05-F507-4FFB-8D96-6BAA2EBB0F0A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03acdfb16c7f1e7e8ee5e6b95902ef1ed056412a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054424"
---
# <span data-ttu-id="1aaad-101">Save-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="1aaad-101">Save-AzureWebsiteLog</span></span>

## <span data-ttu-id="1aaad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1aaad-102">SYNOPSIS</span></span>
<span data-ttu-id="1aaad-103">Pobiera i zapisuje dzienniki określonej witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1aaad-103">Downloads and saves the logs for a specified website.</span></span>

## <span data-ttu-id="1aaad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1aaad-104">SYNTAX</span></span>

```
Save-AzureWebsiteLog [-Output <String>] [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1aaad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1aaad-105">DESCRIPTION</span></span>
<span data-ttu-id="1aaad-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1aaad-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="1aaad-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="1aaad-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="1aaad-108">Polecenie cmdlet **Save-AzureWebsiteLog** pobiera dzienniki określonej witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1aaad-108">The **Save-AzureWebsiteLog** cmdlet downloads the logs for a specified website.</span></span>

## <span data-ttu-id="1aaad-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1aaad-109">EXAMPLES</span></span>

### <span data-ttu-id="1aaad-110">Przykład 1: pobieranie i zapisywanie dzienników witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="1aaad-110">Example 1: Download and save logs for a website</span></span>
```
PS C:\> Save-AzureWebsiteLogs -Name mySite -Output .\logs.zip
```

<span data-ttu-id="1aaad-111">W tym przykładzie dzienniki środowiska uruchomieniowego i wdrażania witryny Moja witryna witryny internetowej są pobierane do pliku logs.zip w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="1aaad-111">This example downloads the runtime and deployment logs for website mySite to the file logs.zip in the current directory.</span></span>

## <span data-ttu-id="1aaad-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1aaad-112">PARAMETERS</span></span>

### <span data-ttu-id="1aaad-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1aaad-113">-Name</span></span>
<span data-ttu-id="1aaad-114">Określa nazwę witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1aaad-114">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="1aaad-115">— Dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="1aaad-115">-Output</span></span>
<span data-ttu-id="1aaad-116">Określa ścieżkę do przechowania pobranego pliku.</span><span class="sxs-lookup"><span data-stu-id="1aaad-116">Specifies the path to store the downloaded file.</span></span>

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

### <span data-ttu-id="1aaad-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1aaad-117">-PassThru</span></span>
<span data-ttu-id="1aaad-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="1aaad-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1aaad-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1aaad-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1aaad-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="1aaad-120">-Profile</span></span>
<span data-ttu-id="1aaad-121">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1aaad-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1aaad-122">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1aaad-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1aaad-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="1aaad-123">-Slot</span></span>
<span data-ttu-id="1aaad-124">Określa nazwę gniazda.</span><span class="sxs-lookup"><span data-stu-id="1aaad-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="1aaad-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aaad-125">CommonParameters</span></span>
<span data-ttu-id="1aaad-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aaad-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aaad-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aaad-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aaad-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1aaad-128">INPUTS</span></span>

## <span data-ttu-id="1aaad-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1aaad-129">OUTPUTS</span></span>

## <span data-ttu-id="1aaad-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1aaad-130">NOTES</span></span>

## <span data-ttu-id="1aaad-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1aaad-131">RELATED LINKS</span></span>

[<span data-ttu-id="1aaad-132">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="1aaad-132">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


