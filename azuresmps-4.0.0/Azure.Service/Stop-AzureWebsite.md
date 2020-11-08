---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7E1A3988-CEEA-49E1-B6F4-1EFA39E170C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06cc64eb67f1e338ff5be28712d1c183bfefd5ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055554"
---
# <span data-ttu-id="82166-101">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="82166-101">Stop-AzureWebsite</span></span>

## <span data-ttu-id="82166-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82166-102">SYNOPSIS</span></span>
<span data-ttu-id="82166-103">Zatrzymuje określoną witrynę internetową.</span><span class="sxs-lookup"><span data-stu-id="82166-103">Stops the specified website.</span></span>

## <span data-ttu-id="82166-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82166-104">SYNTAX</span></span>

```
Stop-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="82166-105">Opis</span><span class="sxs-lookup"><span data-stu-id="82166-105">DESCRIPTION</span></span>
<span data-ttu-id="82166-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="82166-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="82166-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="82166-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="82166-108">Polecenie cmdlet **stop-AzureWebsite** zatrzymuje określoną witrynę sieci Web hostowaną na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="82166-108">The **Stop-AzureWebsite** cmdlet stops the specified website hosted in Azure.</span></span>

## <span data-ttu-id="82166-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82166-109">EXAMPLES</span></span>

## <span data-ttu-id="82166-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82166-110">PARAMETERS</span></span>

### <span data-ttu-id="82166-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="82166-111">-Name</span></span>
<span data-ttu-id="82166-112">Określa nazwę witryny sieci Web, która ma zostać zatrzymana.</span><span class="sxs-lookup"><span data-stu-id="82166-112">Specifies the name of the website to stop.</span></span>

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

### <span data-ttu-id="82166-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82166-113">-PassThru</span></span>
<span data-ttu-id="82166-114">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="82166-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="82166-115">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="82166-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="82166-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="82166-116">-Profile</span></span>
<span data-ttu-id="82166-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82166-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="82166-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="82166-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="82166-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="82166-119">-Slot</span></span>
<span data-ttu-id="82166-120">Określa nazwę gniazda witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="82166-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="82166-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82166-121">CommonParameters</span></span>
<span data-ttu-id="82166-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82166-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82166-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82166-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82166-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82166-124">INPUTS</span></span>

## <span data-ttu-id="82166-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82166-125">OUTPUTS</span></span>

## <span data-ttu-id="82166-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82166-126">NOTES</span></span>

## <span data-ttu-id="82166-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82166-127">RELATED LINKS</span></span>

[<span data-ttu-id="82166-128">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="82166-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="82166-129">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="82166-129">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


