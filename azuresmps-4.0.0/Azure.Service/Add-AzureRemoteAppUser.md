---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A121B341-091D-42AD-B56A-3C75E25A1BF6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8383240f9c1db58a6a22f6754f98211580d31a73
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055347"
---
# <span data-ttu-id="44a38-101">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="44a38-101">Add-AzureRemoteAppUser</span></span>

## <span data-ttu-id="44a38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44a38-102">SYNOPSIS</span></span>
<span data-ttu-id="44a38-103">Dodaje użytkownika do kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="44a38-103">Adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="44a38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44a38-104">SYNTAX</span></span>

```
Add-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="44a38-105">Opis</span><span class="sxs-lookup"><span data-stu-id="44a38-105">DESCRIPTION</span></span>
<span data-ttu-id="44a38-106">Polecenie cmdlet **Add-AzureRemoteAppUser** umożliwia dodanie użytkownika do kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="44a38-106">The **Add-AzureRemoteAppUser** cmdlet adds a user to an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="44a38-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44a38-107">EXAMPLES</span></span>

### <span data-ttu-id="44a38-108">Przykład 1. Dodawanie użytkownika za pomocą konta Microsoft</span><span class="sxs-lookup"><span data-stu-id="44a38-108">Example 1: Add a user using a Microsoft Account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType MicrosoftAccount -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="44a38-109">To polecenie dodaje konto Microsoft PattiFuller@contoso.com do kolekcji o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="44a38-109">This command adds the Microsoft Account PattiFuller@contoso.com to the collection named Contoso.</span></span>

### <span data-ttu-id="44a38-110">Przykład 2: Dodawanie użytkownika przy użyciu konta usługi Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="44a38-110">Example 2: Add a user using an Azure Active Directory account</span></span>
```
PS C:\> Add-AzureRemoteAppUser -CollectionName "Contoso" -UserType OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="44a38-111">To polecenie dodaje konto usługi Azure Active Directory PattiFuller@contoso.com do kolekcji o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="44a38-111">This command adds the Azure Active Directory account PattiFuller@contoso.com to the collection named Contoso.</span></span>

## <span data-ttu-id="44a38-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44a38-112">PARAMETERS</span></span>

### <span data-ttu-id="44a38-113">-Alias</span><span class="sxs-lookup"><span data-stu-id="44a38-113">-Alias</span></span>
<span data-ttu-id="44a38-114">Określa opublikowany alias programu.</span><span class="sxs-lookup"><span data-stu-id="44a38-114">Specifies a published program alias.</span></span>
<span data-ttu-id="44a38-115">Tego parametru można używać tylko w trybie publikowania dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="44a38-115">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="44a38-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="44a38-116">-CollectionName</span></span>
<span data-ttu-id="44a38-117">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="44a38-117">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="44a38-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="44a38-118">-Profile</span></span>
<span data-ttu-id="44a38-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44a38-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="44a38-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="44a38-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44a38-121">-Type</span><span class="sxs-lookup"><span data-stu-id="44a38-121">-Type</span></span>
<span data-ttu-id="44a38-122">Określa typ użytkownika.</span><span class="sxs-lookup"><span data-stu-id="44a38-122">Specifies a user type.</span></span>
<span data-ttu-id="44a38-123">Dopuszczalne wartości tego parametru to: identyfikator organizacji lub MicrosoftAccount.</span><span class="sxs-lookup"><span data-stu-id="44a38-123">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

```yaml
Type: PrincipalProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: OrgId, MicrosoftAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a38-124">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="44a38-124">-UserUpn</span></span>
<span data-ttu-id="44a38-125">Określa na przykład główną nazwę użytkownika (UPN) użytkownika PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="44a38-125">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a38-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44a38-126">CommonParameters</span></span>
<span data-ttu-id="44a38-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44a38-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44a38-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44a38-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44a38-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44a38-129">INPUTS</span></span>

## <span data-ttu-id="44a38-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44a38-130">OUTPUTS</span></span>

## <span data-ttu-id="44a38-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44a38-131">NOTES</span></span>

## <span data-ttu-id="44a38-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44a38-132">RELATED LINKS</span></span>

[<span data-ttu-id="44a38-133">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="44a38-133">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)

[<span data-ttu-id="44a38-134">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="44a38-134">Remove-AzureRemoteAppUser</span></span>](./Remove-AzureRemoteAppUser.md)


