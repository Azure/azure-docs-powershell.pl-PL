---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: EFBC8DCD-00CC-4BBF-9383-EA15376535F3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42780f62bc68659874f7aae1e64ad5ce89038fdf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054809"
---
# <span data-ttu-id="2feed-101">Update-AzureWebsiteRepository</span><span class="sxs-lookup"><span data-stu-id="2feed-101">Update-AzureWebsiteRepository</span></span>

## <span data-ttu-id="2feed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2feed-102">SYNOPSIS</span></span>
<span data-ttu-id="2feed-103">Aktualizuje zdalne repozytoria lokalnego repozytorium git dla wszystkich gniazd.</span><span class="sxs-lookup"><span data-stu-id="2feed-103">Updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="2feed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2feed-104">SYNTAX</span></span>

```
Update-AzureWebsiteRepository [-Name <String>] -PublishingUsername <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2feed-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2feed-105">DESCRIPTION</span></span>
<span data-ttu-id="2feed-106">Polecenie cmdlet **Update-AzureWebsiteRepository** aktualizuje zdalne repozytoria lokalnego repozytorium git dla wszystkich gniazd.</span><span class="sxs-lookup"><span data-stu-id="2feed-106">The **Update-AzureWebsiteRepository** cmdlet updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="2feed-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2feed-107">EXAMPLES</span></span>

### <span data-ttu-id="2feed-108">Przykład 1: aktualizowanie zdalnych repozytoriów w witrynie internetowej</span><span class="sxs-lookup"><span data-stu-id="2feed-108">Example 1: Update Website Remote Repositories</span></span>
```
PS C:\> Update-AzureWebsiteRepository -Name MyWebsite
```

<span data-ttu-id="2feed-109">Aktualizuje zdalne repozytoria lokalnego repozytorium git dla wszystkich gniazd na witrynę Moja witryna sieci Web.</span><span class="sxs-lookup"><span data-stu-id="2feed-109">Updates the remote repositories of a local git repository for all the slots for website MyWebsite.</span></span>

## <span data-ttu-id="2feed-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2feed-110">PARAMETERS</span></span>

### <span data-ttu-id="2feed-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2feed-111">-Name</span></span>
<span data-ttu-id="2feed-112">Nazwa witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="2feed-112">The name of the website.</span></span>

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

### <span data-ttu-id="2feed-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="2feed-113">-Profile</span></span>
<span data-ttu-id="2feed-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2feed-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2feed-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2feed-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2feed-116">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="2feed-116">-PublishingUsername</span></span>
<span data-ttu-id="2feed-117">Nazwa użytkownika określona w portalu Microsoft Azure w celu wdrożenia git.</span><span class="sxs-lookup"><span data-stu-id="2feed-117">The username you have specified in the Microsoft Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="2feed-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2feed-118">-Confirm</span></span>
<span data-ttu-id="2feed-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2feed-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2feed-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2feed-120">-WhatIf</span></span>
<span data-ttu-id="2feed-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2feed-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2feed-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2feed-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2feed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2feed-123">CommonParameters</span></span>
<span data-ttu-id="2feed-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2feed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2feed-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2feed-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2feed-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2feed-126">INPUTS</span></span>

## <span data-ttu-id="2feed-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2feed-127">OUTPUTS</span></span>

## <span data-ttu-id="2feed-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2feed-128">NOTES</span></span>

## <span data-ttu-id="2feed-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2feed-129">RELATED LINKS</span></span>

[<span data-ttu-id="2feed-130">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2feed-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="2feed-131">Nowe — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2feed-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="2feed-132">Start — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2feed-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="2feed-133">Zatrzymaj — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2feed-133">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


