---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 496ABC97-A493-4E42-B998-28A907DFBC19
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0641fd7bc8dcfa5048ac3e9d922bade199af2bab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054905"
---
# <span data-ttu-id="b3cbc-101">Switch-AzureWebsiteSlot</span><span class="sxs-lookup"><span data-stu-id="b3cbc-101">Switch-AzureWebsiteSlot</span></span>

## <span data-ttu-id="b3cbc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="b3cbc-103">Zamienia miejsce produkcyjne witryny sieci Web na inne gniazdo.</span><span class="sxs-lookup"><span data-stu-id="b3cbc-103">Swaps the production slot for a website with another slot.</span></span>

## <span data-ttu-id="b3cbc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3cbc-104">SYNTAX</span></span>

```
Switch-AzureWebsiteSlot [-Name <String>] [-Slot1 <String>] [-Slot2 <String>] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3cbc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b3cbc-105">DESCRIPTION</span></span>
<span data-ttu-id="b3cbc-106">Polecenie cmdlet **Switch-AzureWebsiteSlot** umożliwia zamianę miejsca produkcyjnego witryny sieci Web na inne gniazdo.</span><span class="sxs-lookup"><span data-stu-id="b3cbc-106">The **Switch-AzureWebsiteSlot** cmdlet swaps the production slot for a website with another slot.</span></span>
<span data-ttu-id="b3cbc-107">Ta funkcja działa w witrynach internetowych tylko z dwoma gniazdami.</span><span class="sxs-lookup"><span data-stu-id="b3cbc-107">This works on websites with two slots only.</span></span>

## <span data-ttu-id="b3cbc-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3cbc-108">EXAMPLES</span></span>

### <span data-ttu-id="b3cbc-109">Przykład 1: Przełącz gniazdo witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="b3cbc-109">Example 1: Switch Website Slot</span></span>
```
PS C:\> Switch-AzureWebsiteSlot -Name MyWebsite
```

<span data-ttu-id="b3cbc-110">Przełącz gniazdo kopii zapasowej witryny internetowej platformy Azure z miejscem produkcyjnym.</span><span class="sxs-lookup"><span data-stu-id="b3cbc-110">Switch the azure website MyWebsite backup slot with production slot.</span></span>

## <span data-ttu-id="b3cbc-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3cbc-111">PARAMETERS</span></span>

### <span data-ttu-id="b3cbc-112">-Force</span><span class="sxs-lookup"><span data-stu-id="b3cbc-112">-Force</span></span>
<span data-ttu-id="b3cbc-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b3cbc-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b3cbc-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b3cbc-114">-Name</span></span>
<span data-ttu-id="b3cbc-115">Nazwa witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="b3cbc-115">The name of the website.</span></span>

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

### <span data-ttu-id="b3cbc-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="b3cbc-116">-Profile</span></span>
<span data-ttu-id="b3cbc-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3cbc-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b3cbc-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b3cbc-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b3cbc-119">-Slot1</span><span class="sxs-lookup"><span data-stu-id="b3cbc-119">-Slot1</span></span>
<span data-ttu-id="b3cbc-120">Określa pierwsze gniazdo.</span><span class="sxs-lookup"><span data-stu-id="b3cbc-120">Specifies the first slot.</span></span>

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

### <span data-ttu-id="b3cbc-121">-Slot2</span><span class="sxs-lookup"><span data-stu-id="b3cbc-121">-Slot2</span></span>
<span data-ttu-id="b3cbc-122">Określa drugie gniazdo.</span><span class="sxs-lookup"><span data-stu-id="b3cbc-122">Specifies the second slot.</span></span>

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

### <span data-ttu-id="b3cbc-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3cbc-123">-Confirm</span></span>
<span data-ttu-id="b3cbc-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3cbc-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3cbc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3cbc-125">-WhatIf</span></span>
<span data-ttu-id="b3cbc-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3cbc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3cbc-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b3cbc-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3cbc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3cbc-128">CommonParameters</span></span>
<span data-ttu-id="b3cbc-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3cbc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3cbc-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3cbc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3cbc-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3cbc-131">INPUTS</span></span>

## <span data-ttu-id="b3cbc-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3cbc-132">OUTPUTS</span></span>

## <span data-ttu-id="b3cbc-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3cbc-133">NOTES</span></span>

## <span data-ttu-id="b3cbc-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3cbc-134">RELATED LINKS</span></span>

[<span data-ttu-id="b3cbc-135">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b3cbc-135">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="b3cbc-136">Nowe — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b3cbc-136">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="b3cbc-137">Start — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b3cbc-137">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="b3cbc-138">Zatrzymaj — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b3cbc-138">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


