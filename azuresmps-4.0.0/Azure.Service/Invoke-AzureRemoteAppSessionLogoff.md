---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 87163619-DEA4-4183-BB11-2D7B16F4BE8A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee4e094c1e38c54b1f9ad4e78723ec49fff1f75b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055213"
---
# <span data-ttu-id="d39da-101">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="d39da-101">Invoke-AzureRemoteAppSessionLogoff</span></span>

## <span data-ttu-id="d39da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d39da-102">SYNOPSIS</span></span>
<span data-ttu-id="d39da-103">Natychmiast wylogowuje sesję Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="d39da-103">Logs off an Azure RemoteApp session immediately.</span></span>

## <span data-ttu-id="d39da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d39da-104">SYNTAX</span></span>

```
Invoke-AzureRemoteAppSessionLogoff [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d39da-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d39da-105">DESCRIPTION</span></span>
<span data-ttu-id="d39da-106">Polecenie cmdlet **Invoke-AzureRemoteAppSessionLogoff** umożliwia natychmiastowe wylogowanie użytkownika z sesji zdalnej uruchomionej w usłudze Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="d39da-106">The **Invoke-AzureRemoteAppSessionLogoff** cmdlet immediately logs off a user from a remote session running in Azure RemoteApp.</span></span>

## <span data-ttu-id="d39da-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d39da-107">EXAMPLES</span></span>

### <span data-ttu-id="d39da-108">Przykład 1: wylogowywanie użytkownika</span><span class="sxs-lookup"><span data-stu-id="d39da-108">Example 1: Log off a user</span></span>
```
PS C:\> Invoke-AzureRemoteAppSessionLogoff -CollectionName ContosoApps -UserUpn PattiFuller@contoso.com
```

<span data-ttu-id="d39da-109">To polecenie wylogowuje użytkownika, którego główną nazwę użytkownika jest PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="d39da-109">This command logs off the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="d39da-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d39da-110">PARAMETERS</span></span>

### <span data-ttu-id="d39da-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="d39da-111">-CollectionName</span></span>
<span data-ttu-id="d39da-112">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="d39da-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="d39da-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="d39da-113">-Profile</span></span>
<span data-ttu-id="d39da-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d39da-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d39da-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d39da-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d39da-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="d39da-116">-UserUpn</span></span>
<span data-ttu-id="d39da-117">Specifes główną nazwę użytkownika (UPN) użytkownika, na przykład PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="d39da-117">Specifes the user Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39da-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d39da-118">-Confirm</span></span>
<span data-ttu-id="d39da-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d39da-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d39da-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d39da-120">-WhatIf</span></span>
<span data-ttu-id="d39da-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d39da-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d39da-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d39da-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d39da-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d39da-123">CommonParameters</span></span>
<span data-ttu-id="d39da-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d39da-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d39da-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d39da-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d39da-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d39da-126">INPUTS</span></span>

## <span data-ttu-id="d39da-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d39da-127">OUTPUTS</span></span>

## <span data-ttu-id="d39da-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d39da-128">NOTES</span></span>

## <span data-ttu-id="d39da-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d39da-129">RELATED LINKS</span></span>

[<span data-ttu-id="d39da-130">Dodaj-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="d39da-130">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="d39da-131">Disconnect-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="d39da-131">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="d39da-132">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="d39da-132">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)


