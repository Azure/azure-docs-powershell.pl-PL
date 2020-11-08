---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7785F288-1CDF-444E-B72F-597E75B76074
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1e6e6d9921710bbed81eab727d2fe60927d2ed7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054751"
---
# <span data-ttu-id="95a40-101">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="95a40-101">Show-AzureWebsite</span></span>

## <span data-ttu-id="95a40-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95a40-102">SYNOPSIS</span></span>
<span data-ttu-id="95a40-103">Otwiera przeglądarkę w określonej witrynie sieci Web.</span><span class="sxs-lookup"><span data-stu-id="95a40-103">Opens a browser on a specified website.</span></span>

## <span data-ttu-id="95a40-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95a40-104">SYNTAX</span></span>

```
Show-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="95a40-105">Opis</span><span class="sxs-lookup"><span data-stu-id="95a40-105">DESCRIPTION</span></span>
<span data-ttu-id="95a40-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="95a40-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="95a40-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="95a40-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="95a40-108">Polecenie cmdlet **show-AzureWebsite** umożliwia otwarcie przeglądarki w określonej witrynie sieci Web.</span><span class="sxs-lookup"><span data-stu-id="95a40-108">The **Show-AzureWebsite** cmdlet opens a browser on a specified website.</span></span>

## <span data-ttu-id="95a40-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95a40-109">EXAMPLES</span></span>

## <span data-ttu-id="95a40-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95a40-110">PARAMETERS</span></span>

### <span data-ttu-id="95a40-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="95a40-111">-Name</span></span>
<span data-ttu-id="95a40-112">Określa nazwę witryny, którą należy otworzyć w przeglądarce.</span><span class="sxs-lookup"><span data-stu-id="95a40-112">Specifies the name of the site to open in the browser.</span></span>

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

### <span data-ttu-id="95a40-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="95a40-113">-Profile</span></span>
<span data-ttu-id="95a40-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95a40-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="95a40-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="95a40-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="95a40-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="95a40-116">-Slot</span></span>
<span data-ttu-id="95a40-117">Określa nazwę gniazda witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="95a40-117">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="95a40-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95a40-118">CommonParameters</span></span>
<span data-ttu-id="95a40-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95a40-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95a40-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95a40-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95a40-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95a40-121">INPUTS</span></span>

## <span data-ttu-id="95a40-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95a40-122">OUTPUTS</span></span>

## <span data-ttu-id="95a40-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95a40-123">NOTES</span></span>

## <span data-ttu-id="95a40-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95a40-124">RELATED LINKS</span></span>

[<span data-ttu-id="95a40-125">Pokaż — AzurePortal</span><span class="sxs-lookup"><span data-stu-id="95a40-125">Show-AzurePortal</span></span>](./Show-AzurePortal.md)

[<span data-ttu-id="95a40-126">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="95a40-126">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="95a40-127">Nowe — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="95a40-127">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="95a40-128">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="95a40-128">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="95a40-129">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="95a40-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="95a40-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="95a40-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


