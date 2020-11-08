---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A4E9C9A7-7FD2-4FD5-AB35-CFF717607B44
online version: ''
schema: 2.0.0
ms.openlocfilehash: c6da222e6cbfe02e181e4a863d8ce8d585215bdd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055113"
---
# <span data-ttu-id="970e0-101">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="970e0-101">Remove-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="970e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="970e0-102">SYNOPSIS</span></span>
<span data-ttu-id="970e0-103">Usuwa dysk użytkownika użytkownika z kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="970e0-103">Removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="970e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="970e0-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUserDisk [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="970e0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="970e0-105">DESCRIPTION</span></span>
<span data-ttu-id="970e0-106">Polecenie cmdlet **Remove-AzureRemoteAppUserDisk** usuwa dysk użytkownika użytkownika z kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="970e0-106">The **Remove-AzureRemoteAppUserDisk** cmdlet removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="970e0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="970e0-107">EXAMPLES</span></span>

### <span data-ttu-id="970e0-108">Przykład 1: usuwanie dysku użytkownika</span><span class="sxs-lookup"><span data-stu-id="970e0-108">Example 1: Remove a user disk</span></span>
```
PS C:\> Remove-AzureRemoteAppUserDisk -CollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="970e0-109">To polecenie usuwa dysk użytkownika użytkownika usługi Azure Active Directory, który ma główną nazwę użytkownika PattiFuller@contoso.com z kolekcji Contoso01.</span><span class="sxs-lookup"><span data-stu-id="970e0-109">This command removes the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01.</span></span>

## <span data-ttu-id="970e0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="970e0-110">PARAMETERS</span></span>

### <span data-ttu-id="970e0-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="970e0-111">-CollectionName</span></span>
<span data-ttu-id="970e0-112">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="970e0-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="970e0-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="970e0-113">-Profile</span></span>
<span data-ttu-id="970e0-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="970e0-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="970e0-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="970e0-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="970e0-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="970e0-116">-UserUpn</span></span>
<span data-ttu-id="970e0-117">Określa główną nazwę użytkownika (UPN) użytkownika, dla którego to polecenie cmdlet usuwa dysk.</span><span class="sxs-lookup"><span data-stu-id="970e0-117">Specifies the user principal name (UPN) of the user for whom this cmdlet removes the disk.</span></span>

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

### <span data-ttu-id="970e0-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="970e0-118">-Confirm</span></span>
<span data-ttu-id="970e0-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="970e0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="970e0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="970e0-120">-WhatIf</span></span>
<span data-ttu-id="970e0-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="970e0-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="970e0-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="970e0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="970e0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="970e0-123">CommonParameters</span></span>
<span data-ttu-id="970e0-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="970e0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="970e0-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="970e0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="970e0-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="970e0-126">INPUTS</span></span>

## <span data-ttu-id="970e0-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="970e0-127">OUTPUTS</span></span>

## <span data-ttu-id="970e0-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="970e0-128">NOTES</span></span>

## <span data-ttu-id="970e0-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="970e0-129">RELATED LINKS</span></span>

[<span data-ttu-id="970e0-130">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="970e0-130">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)


