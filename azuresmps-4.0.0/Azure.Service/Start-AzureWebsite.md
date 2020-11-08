---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A9542EA9-C709-48D7-8066-496015AB977E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1e7aab4f7818cbfc7200b521a535d54fb08dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054736"
---
# <span data-ttu-id="5c68d-101">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5c68d-101">Start-AzureWebsite</span></span>

## <span data-ttu-id="5c68d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c68d-102">SYNOPSIS</span></span>
<span data-ttu-id="5c68d-103">Uruchamia określoną witrynę sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5c68d-103">Starts the specified website.</span></span>

## <span data-ttu-id="5c68d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c68d-104">SYNTAX</span></span>

```
Start-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c68d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5c68d-105">DESCRIPTION</span></span>
<span data-ttu-id="5c68d-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5c68d-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5c68d-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5c68d-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5c68d-108">Polecenie cmdlet **Start-AzureWebsite** uruchamia określoną witrynę sieci Web działającą na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="5c68d-108">The **Start-AzureWebsite** cmdlet starts a specified website running in Azure.</span></span>

## <span data-ttu-id="5c68d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c68d-109">EXAMPLES</span></span>

## <span data-ttu-id="5c68d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c68d-110">PARAMETERS</span></span>

### <span data-ttu-id="5c68d-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5c68d-111">-Name</span></span>
<span data-ttu-id="5c68d-112">Określa nazwę witryny sieci Web, która ma zostać uruchomiona.</span><span class="sxs-lookup"><span data-stu-id="5c68d-112">Specifies the name of the website to start.</span></span>

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

### <span data-ttu-id="5c68d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c68d-113">-PassThru</span></span>
<span data-ttu-id="5c68d-114">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="5c68d-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5c68d-115">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5c68d-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5c68d-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="5c68d-116">-Profile</span></span>
<span data-ttu-id="5c68d-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c68d-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5c68d-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="5c68d-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5c68d-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="5c68d-119">-Slot</span></span>
<span data-ttu-id="5c68d-120">Określa nazwę gniazda witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5c68d-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="5c68d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c68d-121">CommonParameters</span></span>
<span data-ttu-id="5c68d-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c68d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c68d-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c68d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c68d-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c68d-124">INPUTS</span></span>

## <span data-ttu-id="5c68d-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c68d-125">OUTPUTS</span></span>

## <span data-ttu-id="5c68d-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c68d-126">NOTES</span></span>

## <span data-ttu-id="5c68d-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c68d-127">RELATED LINKS</span></span>

[<span data-ttu-id="5c68d-128">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5c68d-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="5c68d-129">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5c68d-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="5c68d-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5c68d-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)

[<span data-ttu-id="5c68d-131">Pokaż — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5c68d-131">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)

[<span data-ttu-id="5c68d-132">Zatrzymaj — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5c68d-132">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


