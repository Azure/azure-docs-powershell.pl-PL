---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-help.xml
ms.assetid: 02F429EA-FE9A-427F-86B5-C9C4275FD3EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 289cc21b6edd2a841b8121672d838aaa056db4f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054664"
---
# <span data-ttu-id="1feed-101">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="1feed-101">Copy-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="1feed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1feed-102">SYNOPSIS</span></span>
<span data-ttu-id="1feed-103">Kopiuje dysk użytkownika użytkownika z jednej kolekcji funkcji Azure RemoteApp na inną.</span><span class="sxs-lookup"><span data-stu-id="1feed-103">Copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="1feed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1feed-104">SYNTAX</span></span>

```
Copy-AzureRemoteAppUserDisk [-SourceCollectionName] <String> [-DestinationCollectionName] <String>
 [-UserUpn] <String> [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1feed-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1feed-105">DESCRIPTION</span></span>
<span data-ttu-id="1feed-106">Polecenie cmdlet **copy-AzureRemoteAppUserDisk** kopiuje dysk użytkownika użytkownika z jednej kolekcji funkcji Azure RemoteApp na inną.</span><span class="sxs-lookup"><span data-stu-id="1feed-106">The **Copy-AzureRemoteAppUserDisk** cmdlet copies the user disk of a user from one Azure RemoteApp collection to another.</span></span>

## <span data-ttu-id="1feed-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1feed-107">EXAMPLES</span></span>

### <span data-ttu-id="1feed-108">Przykład 1: Kopiowanie dysku użytkownika</span><span class="sxs-lookup"><span data-stu-id="1feed-108">Example 1: Copy a user disk</span></span>
```
PS C:\> Copy-AzureRemoteAppUserDisk -DestinationCollectionName "Contoso02" -SourceCollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com" -OverwriteExistingUserDisk
```

<span data-ttu-id="1feed-109">To polecenie kopiuje dysk użytkownika użytkownika usługi Azure Active Directory, który ma główną nazwę użytkownika PattiFuller@contoso.com kolekcji Contoso01 do Contoso02 kolekcji.</span><span class="sxs-lookup"><span data-stu-id="1feed-109">This command copies the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01 to the collection Contoso02.</span></span>
<span data-ttu-id="1feed-110">Jeśli dysk użytkownika PattiFuller@contoso.com już istnieje w Contoso02, to polecenie zastępuje je.</span><span class="sxs-lookup"><span data-stu-id="1feed-110">If a user disk for PattiFuller@contoso.com already exists on Contoso02, this command overwrites it.</span></span>

## <span data-ttu-id="1feed-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1feed-111">PARAMETERS</span></span>

### <span data-ttu-id="1feed-112">-DestinationCollectionName</span><span class="sxs-lookup"><span data-stu-id="1feed-112">-DestinationCollectionName</span></span>
<span data-ttu-id="1feed-113">Określa nazwę kolekcji funkcji RemoteApp w lokalizacji docelowej Azure.</span><span class="sxs-lookup"><span data-stu-id="1feed-113">Specifies the name of the destination Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="1feed-114">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="1feed-114">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="1feed-115">Wskazuje, że to polecenie cmdlet zastępuje istniejący dysk użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1feed-115">Indicates that this cmdlet overwrites an existing user disk.</span></span>

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

### <span data-ttu-id="1feed-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="1feed-116">-Profile</span></span>
<span data-ttu-id="1feed-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1feed-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1feed-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1feed-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1feed-119">-SourceCollectionName</span><span class="sxs-lookup"><span data-stu-id="1feed-119">-SourceCollectionName</span></span>
<span data-ttu-id="1feed-120">Określa nazwę źródłowej kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="1feed-120">Specifies the name of the source Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="1feed-121">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="1feed-121">-UserUpn</span></span>
<span data-ttu-id="1feed-122">Określa główną nazwę użytkownika (UPN) użytkownika, dla którego ten aplet polecenia kopiuje dysk.</span><span class="sxs-lookup"><span data-stu-id="1feed-122">Specifies the user principal name (UPN) of the user for whom this cmdlet copies the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1feed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1feed-123">CommonParameters</span></span>
<span data-ttu-id="1feed-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1feed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1feed-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1feed-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1feed-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1feed-126">INPUTS</span></span>

## <span data-ttu-id="1feed-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1feed-127">OUTPUTS</span></span>

## <span data-ttu-id="1feed-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1feed-128">NOTES</span></span>

## <span data-ttu-id="1feed-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1feed-129">RELATED LINKS</span></span>

[<span data-ttu-id="1feed-130">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="1feed-130">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


