---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DE89F1C4-8441-4438-B235-F5E0F726EFF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc3bad916830cb638d13f39964e12dc874f7d9f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054832"
---
# <span data-ttu-id="9a534-101">Remove-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="9a534-101">Remove-AzureRemoteAppUser</span></span>

## <span data-ttu-id="9a534-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a534-102">SYNOPSIS</span></span>
<span data-ttu-id="9a534-103">Usuwa użytkownika z kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="9a534-103">Removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="9a534-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a534-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUser [-CollectionName] <String> [-Type] <PrincipalProviderType> [-UserUpn] <String[]>
 [-Alias <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9a534-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9a534-105">DESCRIPTION</span></span>
<span data-ttu-id="9a534-106">Polecenie cmdlet **Remove-AzureRemoteAppUser** umożliwia usunięcie użytkownika z kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="9a534-106">The **Remove-AzureRemoteAppUser** cmdlet removes a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="9a534-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a534-107">EXAMPLES</span></span>

### <span data-ttu-id="9a534-108">Example1: Usuwanie użytkownika z kolekcji</span><span class="sxs-lookup"><span data-stu-id="9a534-108">Example1: Remove a user from a collection</span></span>
```
PS C:\> Remove-AzureRemoteAppUser -CollectionName "Contoso" -Type OrgId -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="9a534-109">To polecenie usuwa użytkownika usługi Azure pozycji PattiFuller@contoso.com z kolekcji contoso.</span><span class="sxs-lookup"><span data-stu-id="9a534-109">This command removes the Azure ActiveDirectory user PattiFuller@contoso.com from the Contoso collection.</span></span>

## <span data-ttu-id="9a534-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a534-110">PARAMETERS</span></span>

### <span data-ttu-id="9a534-111">-Alias</span><span class="sxs-lookup"><span data-stu-id="9a534-111">-Alias</span></span>
<span data-ttu-id="9a534-112">Określa opublikowany alias programu.</span><span class="sxs-lookup"><span data-stu-id="9a534-112">Specifies a published program alias.</span></span>
<span data-ttu-id="9a534-113">Tego parametru można używać tylko w trybie publikowania dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9a534-113">You can use this parameter only in per-app publishing mode.</span></span>

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

### <span data-ttu-id="9a534-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="9a534-114">-CollectionName</span></span>
<span data-ttu-id="9a534-115">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="9a534-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="9a534-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="9a534-116">-Profile</span></span>
<span data-ttu-id="9a534-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a534-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9a534-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9a534-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9a534-119">-Type</span><span class="sxs-lookup"><span data-stu-id="9a534-119">-Type</span></span>
<span data-ttu-id="9a534-120">Określa typ użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9a534-120">Specifies a user type.</span></span>
<span data-ttu-id="9a534-121">Dopuszczalne wartości tego parametru to: identyfikator organizacji lub MicrosoftAccount.</span><span class="sxs-lookup"><span data-stu-id="9a534-121">The acceptable values for this parameter are: OrgId or MicrosoftAccount.</span></span>

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

### <span data-ttu-id="9a534-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="9a534-122">-UserUpn</span></span>
<span data-ttu-id="9a534-123">Określa na przykład główną nazwę użytkownika (UPN) użytkownika user@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="9a534-123">Specifies the User Principal Name (UPN) of a user, for example, user@contoso.com.</span></span>

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

### <span data-ttu-id="9a534-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a534-124">CommonParameters</span></span>
<span data-ttu-id="9a534-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a534-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a534-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a534-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a534-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a534-127">INPUTS</span></span>

## <span data-ttu-id="9a534-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a534-128">OUTPUTS</span></span>

## <span data-ttu-id="9a534-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a534-129">NOTES</span></span>

## <span data-ttu-id="9a534-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a534-130">RELATED LINKS</span></span>

[<span data-ttu-id="9a534-131">Dodaj-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="9a534-131">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="9a534-132">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="9a534-132">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


