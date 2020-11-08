---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6F2CC9F-8C95-484D-8676-7DAA5E0AA617
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf2a5cc1390db2a6ae5eb49894a47d1ccf0aca4c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055282"
---
# <span data-ttu-id="5c479-101">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="5c479-101">Get-AzureRemoteAppUser</span></span>

## <span data-ttu-id="5c479-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c479-102">SYNOPSIS</span></span>
<span data-ttu-id="5c479-103">Wyświetla listę użytkowników w kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="5c479-103">Lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="5c479-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c479-104">SYNTAX</span></span>

```
Get-AzureRemoteAppUser [-CollectionName] <String> [[-UserUpn] <String>] [-Alias <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5c479-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5c479-105">DESCRIPTION</span></span>
<span data-ttu-id="5c479-106">Polecenie cmdlet **Get-AzureRemoteAppUser** wyświetla listę użytkowników w kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="5c479-106">The **Get-AzureRemoteAppUser** cmdlet lists the users in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="5c479-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c479-107">EXAMPLES</span></span>

### <span data-ttu-id="5c479-108">Przykład 1: Wyświetlanie listy użytkowników kolekcji</span><span class="sxs-lookup"><span data-stu-id="5c479-108">Example 1: List the users of a collection</span></span>
```
PS C:\> Get-AzureRemoteAppUser -CollectionName "Contoso"
```

<span data-ttu-id="5c479-109">To polecenie umożliwia wyświetlenie listy użytkowników, którzy mają dostęp do kolekcji funkcji Azure RemoteApp o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="5c479-109">This command lists the users who have access to the Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="5c479-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c479-110">PARAMETERS</span></span>

### <span data-ttu-id="5c479-111">-Alias</span><span class="sxs-lookup"><span data-stu-id="5c479-111">-Alias</span></span>
<span data-ttu-id="5c479-112">Określa opublikowany alias programu.</span><span class="sxs-lookup"><span data-stu-id="5c479-112">Specifies a published program alias.</span></span>
<span data-ttu-id="5c479-113">Tego parametru można używać tylko w trybie publikowania dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5c479-113">You can use this parameter only in per-app publishing mode.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c479-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="5c479-114">-CollectionName</span></span>
<span data-ttu-id="5c479-115">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="5c479-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="5c479-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="5c479-116">-Profile</span></span>
<span data-ttu-id="5c479-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c479-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5c479-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="5c479-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5c479-119">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="5c479-119">-UserUpn</span></span>
<span data-ttu-id="5c479-120">Określa główną nazwę użytkownika (UPN) użytkownika, dla którego należy wyświetlić informacje.</span><span class="sxs-lookup"><span data-stu-id="5c479-120">Specifies the User Principal Name (UPN) of a user for which to list information.</span></span>
<span data-ttu-id="5c479-121">Na przykład PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="5c479-121">For example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="5c479-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c479-122">CommonParameters</span></span>
<span data-ttu-id="5c479-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c479-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c479-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c479-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c479-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c479-125">INPUTS</span></span>

## <span data-ttu-id="5c479-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c479-126">OUTPUTS</span></span>

## <span data-ttu-id="5c479-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c479-127">NOTES</span></span>

## <span data-ttu-id="5c479-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c479-128">RELATED LINKS</span></span>

[<span data-ttu-id="5c479-129">Dodaj-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="5c479-129">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="5c479-130">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="5c479-130">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="5c479-131">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="5c479-131">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


