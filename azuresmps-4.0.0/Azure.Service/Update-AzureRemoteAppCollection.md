---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 67890A2A-7922-4E4A-96B4-B58CF532D2DE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a949128309e2777984be0dac33f27b0bc53aab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054703"
---
# <span data-ttu-id="19c16-101">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="19c16-101">Update-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="19c16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19c16-102">SYNOPSIS</span></span>
<span data-ttu-id="19c16-103">Umożliwia zaktualizowanie kolekcji funkcji Azure RemoteApp przy użyciu nowego obrazu szablonu.</span><span class="sxs-lookup"><span data-stu-id="19c16-103">Updates an Azure RemoteApp collection with a new template image.</span></span>

## <span data-ttu-id="19c16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19c16-104">SYNTAX</span></span>

```
Update-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [[-SubnetName] <String>]
 [-ForceLogoffWhenUpdateComplete] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19c16-105">Opis</span><span class="sxs-lookup"><span data-stu-id="19c16-105">DESCRIPTION</span></span>
<span data-ttu-id="19c16-106">Polecenie cmdlet **Update-AzureRemoteAppCollection** umożliwia zaktualizowanie kolekcji funkcji Azure RemoteApp przy użyciu nowego obrazu szablonu.</span><span class="sxs-lookup"><span data-stu-id="19c16-106">The **Update-AzureRemoteAppCollection** cmdlet updates an Azure RemoteApp collection with a new template image.</span></span>
<span data-ttu-id="19c16-107">Po ukończeniu aktualizacji użytkownicy korzystający z istniejących sesji będą mogli wylogować się po jednej godzinie, zanim zostaną wylogowani automatycznie. Gdy zalogują się ponownie, nawiąże połączenie z nowo zaktualizowaną kolekcją.</span><span class="sxs-lookup"><span data-stu-id="19c16-107">After the update completes, users with existing sessions have one hour to sign out before they are automatically signed out. When they sign in again, they connect to the newly updated collection.</span></span>
<span data-ttu-id="19c16-108">Aby zmusić użytkowników do natychmiastowego wylogowania się zaraz po zaktualizowaniu kolekcji, określ parametr *ForceLogoffWhenUpdateComplete* .</span><span class="sxs-lookup"><span data-stu-id="19c16-108">To force users to be immediately signed out as soon as the collection is updated, specify the *ForceLogoffWhenUpdateComplete* parameter.</span></span>

## <span data-ttu-id="19c16-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19c16-109">EXAMPLES</span></span>

## <span data-ttu-id="19c16-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19c16-110">PARAMETERS</span></span>

### <span data-ttu-id="19c16-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="19c16-111">-CollectionName</span></span>
<span data-ttu-id="19c16-112">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="19c16-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c16-113">-ForceLogoffWhenUpdateComplete</span><span class="sxs-lookup"><span data-stu-id="19c16-113">-ForceLogoffWhenUpdateComplete</span></span>
<span data-ttu-id="19c16-114">Wskazuje, że to polecenie cmdlet sygnalizuje użytkownikom istniejące sesje zaraz po zakończeniu aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="19c16-114">Indicates that this cmdlet signs users out of their existing sessions as soon as the update is complete.</span></span>
<span data-ttu-id="19c16-115">Gdy użytkownicy zalogują się ponownie, nawiążą połączenie z nowo zaktualizowaną kolekcją.</span><span class="sxs-lookup"><span data-stu-id="19c16-115">When users sign in again, they connect to the newly updated collection.</span></span>

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

### <span data-ttu-id="19c16-116">-ImageName</span><span class="sxs-lookup"><span data-stu-id="19c16-116">-ImageName</span></span>
<span data-ttu-id="19c16-117">Określa nazwę obrazu szablonu usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="19c16-117">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c16-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="19c16-118">-Profile</span></span>
<span data-ttu-id="19c16-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19c16-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="19c16-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="19c16-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="19c16-121">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="19c16-121">-SubnetName</span></span>
<span data-ttu-id="19c16-122">Określa nazwę podsieci, do której ma zostać przeniesiona kolekcja.</span><span class="sxs-lookup"><span data-stu-id="19c16-122">Specifies the name of the subnet into which to move the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c16-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19c16-123">-Confirm</span></span>
<span data-ttu-id="19c16-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19c16-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19c16-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c16-125">-WhatIf</span></span>
<span data-ttu-id="19c16-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19c16-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19c16-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="19c16-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19c16-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c16-128">CommonParameters</span></span>
<span data-ttu-id="19c16-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c16-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c16-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c16-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c16-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19c16-131">INPUTS</span></span>

## <span data-ttu-id="19c16-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19c16-132">OUTPUTS</span></span>

## <span data-ttu-id="19c16-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19c16-133">NOTES</span></span>

## <span data-ttu-id="19c16-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19c16-134">RELATED LINKS</span></span>

[<span data-ttu-id="19c16-135">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="19c16-135">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="19c16-136">Nowe — AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="19c16-136">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="19c16-137">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="19c16-137">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)


