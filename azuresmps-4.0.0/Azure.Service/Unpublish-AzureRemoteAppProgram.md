---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DB3F85D6-5962-4288-AD75-0C30448B769C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88438fa66e39b5ad63db7b6d2609107d224f7faf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054986"
---
# <span data-ttu-id="f04fc-101">Unpublish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="f04fc-101">Unpublish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="f04fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f04fc-102">SYNOPSIS</span></span>
<span data-ttu-id="f04fc-103">Cofnięcie publikowania programu Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="f04fc-103">Unpublishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="f04fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f04fc-104">SYNTAX</span></span>

```
Unpublish-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String[]>] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f04fc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f04fc-105">DESCRIPTION</span></span>
<span data-ttu-id="f04fc-106">Polecenie cmdlet **cofnięcia publikowania — AzureRemoteAppProgram** powoduje cofnięcie publikowania programu Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="f04fc-106">The **Unpublish-AzureRemoteAppProgram** cmdlet unpublishes an Azure RemoteApp program.</span></span>
<span data-ttu-id="f04fc-107">Po cofnięciu publikowania program nie jest już dostępny dla użytkowników kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="f04fc-107">After you unpublish a program, it is no longer available to the users of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="f04fc-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f04fc-108">EXAMPLES</span></span>

## <span data-ttu-id="f04fc-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f04fc-109">PARAMETERS</span></span>

### <span data-ttu-id="f04fc-110">-Alias</span><span class="sxs-lookup"><span data-stu-id="f04fc-110">-Alias</span></span>
<span data-ttu-id="f04fc-111">Określa tablicę aliasów programów do cofnięcia publikowania.</span><span class="sxs-lookup"><span data-stu-id="f04fc-111">Specifies an array of aliases of the programs to unpublish.</span></span>
<span data-ttu-id="f04fc-112">Użyj polecenia **Get-AzureRemoteAppProgram** , aby odzyskać alias programu do cofnięcia publikowania.</span><span class="sxs-lookup"><span data-stu-id="f04fc-112">Use **Get-AzureRemoteAppProgram** to retrieve the alias of a program to unpublish.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f04fc-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="f04fc-113">-CollectionName</span></span>
<span data-ttu-id="f04fc-114">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="f04fc-114">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="f04fc-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="f04fc-115">-Profile</span></span>
<span data-ttu-id="f04fc-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f04fc-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f04fc-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="f04fc-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f04fc-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f04fc-118">-Confirm</span></span>
<span data-ttu-id="f04fc-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f04fc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f04fc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f04fc-120">-WhatIf</span></span>
<span data-ttu-id="f04fc-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f04fc-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f04fc-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f04fc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f04fc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f04fc-123">CommonParameters</span></span>
<span data-ttu-id="f04fc-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f04fc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f04fc-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f04fc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f04fc-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f04fc-126">INPUTS</span></span>

## <span data-ttu-id="f04fc-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f04fc-127">OUTPUTS</span></span>

## <span data-ttu-id="f04fc-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f04fc-128">NOTES</span></span>

## <span data-ttu-id="f04fc-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f04fc-129">RELATED LINKS</span></span>

[<span data-ttu-id="f04fc-130">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="f04fc-130">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="f04fc-131">Publikowanie — AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="f04fc-131">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)


