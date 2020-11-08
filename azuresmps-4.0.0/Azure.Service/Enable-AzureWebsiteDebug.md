---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1FB590D3-E5D2-45F0-A611-01A1B701938A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 89d0c4dd73e5d921eb447e213876d8906c210b34
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055340"
---
# <span data-ttu-id="a0d8e-101">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="a0d8e-101">Enable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="a0d8e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0d8e-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d8e-103">Włącza debugowanie witryny internetowej.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-103">Enables the website's debug.</span></span>

## <span data-ttu-id="a0d8e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0d8e-104">SYNTAX</span></span>

```
Enable-AzureWebsiteDebug [-PassThru] -Version <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a0d8e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a0d8e-105">DESCRIPTION</span></span>
<span data-ttu-id="a0d8e-106">Umożliwia włączenie funkcji debugowania witryny sieci Web w programie Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-106">Enables the website's debug feature in Visual Studio.</span></span>

## <span data-ttu-id="a0d8e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0d8e-107">EXAMPLES</span></span>

### <span data-ttu-id="a0d8e-108">Włączanie debugowania programu Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="a0d8e-108">Enable debugging of Visual Studio 2013</span></span>
```
PS C:\> Enable-AzureWebsiteDebug -Name MyWebsite -Version VS2013
```

<span data-ttu-id="a0d8e-109">Umożliwia debugowanie z VS 2013.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-109">Enables debugging on VS 2013.</span></span>

## <span data-ttu-id="a0d8e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0d8e-110">PARAMETERS</span></span>

### <span data-ttu-id="a0d8e-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a0d8e-111">-Name</span></span>
<span data-ttu-id="a0d8e-112">Nazwa witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="a0d8e-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0d8e-113">-PassThru</span></span>
<span data-ttu-id="a0d8e-114">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a0d8e-115">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a0d8e-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="a0d8e-116">-Profile</span></span>
<span data-ttu-id="a0d8e-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a0d8e-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a0d8e-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="a0d8e-119">-Slot</span></span>
<span data-ttu-id="a0d8e-120">Nazwa gniazda witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="a0d8e-121">-Version</span><span class="sxs-lookup"><span data-stu-id="a0d8e-121">-Version</span></span>
<span data-ttu-id="a0d8e-122">Wersja programu Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-122">The Visual Studio version.</span></span>

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

### <span data-ttu-id="a0d8e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d8e-123">CommonParameters</span></span>
<span data-ttu-id="a0d8e-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0d8e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d8e-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0d8e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d8e-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0d8e-126">INPUTS</span></span>

## <span data-ttu-id="a0d8e-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0d8e-127">OUTPUTS</span></span>

## <span data-ttu-id="a0d8e-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0d8e-128">NOTES</span></span>

## <span data-ttu-id="a0d8e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0d8e-129">RELATED LINKS</span></span>

[<span data-ttu-id="a0d8e-130">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="a0d8e-130">Disable-AzureWebsiteDebug</span></span>](./Disable-AzureWebsiteDebug.md)

[<span data-ttu-id="a0d8e-131">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a0d8e-131">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="a0d8e-132">Nowe — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a0d8e-132">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="a0d8e-133">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a0d8e-133">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="a0d8e-134">Start — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a0d8e-134">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


