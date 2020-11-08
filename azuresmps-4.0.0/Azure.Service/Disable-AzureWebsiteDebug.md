---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2480FA03-09C6-4A4F-8DDD-01F6AFF6117E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3805794cdc6105112175e0524a894f571f8b5bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054657"
---
# <span data-ttu-id="7dd80-101">Disable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="7dd80-101">Disable-AzureWebsiteDebug</span></span>

## <span data-ttu-id="7dd80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7dd80-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd80-103">Wyłącza debugowanie witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="7dd80-103">Disables the website's debugging.</span></span>

## <span data-ttu-id="7dd80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7dd80-104">SYNTAX</span></span>

```
Disable-AzureWebsiteDebug [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7dd80-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7dd80-105">DESCRIPTION</span></span>
<span data-ttu-id="7dd80-106">Wyłącza debugowanie witryny sieci Web w programie Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7dd80-106">Disables the website's debugging in Visual Studio.</span></span>

## <span data-ttu-id="7dd80-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7dd80-107">EXAMPLES</span></span>

### <span data-ttu-id="7dd80-108">--------------Wyłącz debugowanie witryny internetowej--------------</span><span class="sxs-lookup"><span data-stu-id="7dd80-108">--------------  Disable website debugging --------------</span></span>
```
PS C:\> Disable-AzureWebsiteDebug -Name MyWebsite
```

<span data-ttu-id="7dd80-109">Wyłącza debugowanie witryny sieci Web w witrynie Moja witryna.</span><span class="sxs-lookup"><span data-stu-id="7dd80-109">Disables website debugging on website MyWebsite</span></span>

## <span data-ttu-id="7dd80-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7dd80-110">PARAMETERS</span></span>

### <span data-ttu-id="7dd80-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7dd80-111">-Name</span></span>
<span data-ttu-id="7dd80-112">Nazwa witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd80-112">The name of the Azure website.</span></span>

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

### <span data-ttu-id="7dd80-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7dd80-113">-PassThru</span></span>
<span data-ttu-id="7dd80-114">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="7dd80-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7dd80-115">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="7dd80-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7dd80-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="7dd80-116">-Profile</span></span>
<span data-ttu-id="7dd80-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dd80-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7dd80-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="7dd80-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7dd80-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="7dd80-119">-Slot</span></span>
<span data-ttu-id="7dd80-120">Nazwa gniazda witryny sieci Web usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd80-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="7dd80-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd80-121">CommonParameters</span></span>
<span data-ttu-id="7dd80-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dd80-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd80-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dd80-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd80-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7dd80-124">INPUTS</span></span>

## <span data-ttu-id="7dd80-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7dd80-125">OUTPUTS</span></span>

## <span data-ttu-id="7dd80-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7dd80-126">NOTES</span></span>

## <span data-ttu-id="7dd80-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7dd80-127">RELATED LINKS</span></span>

[<span data-ttu-id="7dd80-128">Enable-AzureWebsiteDebug</span><span class="sxs-lookup"><span data-stu-id="7dd80-128">Enable-AzureWebsiteDebug</span></span>](./Enable-AzureWebsiteDebug.md)

[<span data-ttu-id="7dd80-129">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7dd80-129">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="7dd80-130">Nowe — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7dd80-130">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="7dd80-131">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7dd80-131">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="7dd80-132">Start — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="7dd80-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


