---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8E67D1A4-4247-4603-8D26-42D6D48FE686
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90c654432760061d5c2ba36675c958135329b225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054834"
---
# <span data-ttu-id="2e6b2-101">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="2e6b2-101">Remove-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="2e6b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e6b2-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6b2-103">Usuwa kolekcję funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="2e6b2-103">Removes an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="2e6b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e6b2-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppCollection [-CollectionName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e6b2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e6b2-105">DESCRIPTION</span></span>
<span data-ttu-id="2e6b2-106">Polecenie cmdlet **Remove-AzureRemoteAppCollection** usuwa kolekcję funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="2e6b2-106">The **Remove-AzureRemoteAppCollection** cmdlet removes an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="2e6b2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e6b2-107">EXAMPLES</span></span>

## <span data-ttu-id="2e6b2-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e6b2-108">PARAMETERS</span></span>

### <span data-ttu-id="2e6b2-109">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="2e6b2-109">-CollectionName</span></span>
<span data-ttu-id="2e6b2-110">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="2e6b2-110">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="2e6b2-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="2e6b2-111">-Profile</span></span>
<span data-ttu-id="2e6b2-112">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e6b2-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2e6b2-113">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2e6b2-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2e6b2-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e6b2-114">-Confirm</span></span>
<span data-ttu-id="2e6b2-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e6b2-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e6b2-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e6b2-116">-WhatIf</span></span>
<span data-ttu-id="2e6b2-117">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e6b2-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e6b2-118">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2e6b2-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e6b2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6b2-119">CommonParameters</span></span>
<span data-ttu-id="2e6b2-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e6b2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6b2-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e6b2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6b2-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e6b2-122">INPUTS</span></span>

## <span data-ttu-id="2e6b2-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e6b2-123">OUTPUTS</span></span>

## <span data-ttu-id="2e6b2-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e6b2-124">NOTES</span></span>

## <span data-ttu-id="2e6b2-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e6b2-125">RELATED LINKS</span></span>

[<span data-ttu-id="2e6b2-126">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="2e6b2-126">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="2e6b2-127">Nowe — AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="2e6b2-127">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="2e6b2-128">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="2e6b2-128">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="2e6b2-129">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="2e6b2-129">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


