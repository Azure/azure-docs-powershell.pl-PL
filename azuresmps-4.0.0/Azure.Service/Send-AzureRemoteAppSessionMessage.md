---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 6236AD2C-D54D-4013-9977-AD1E6EAC2F21
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac0283f6c9de9a1cd5f17abd6e27ebb2c8629505
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055399"
---
# <span data-ttu-id="89634-101">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="89634-101">Send-AzureRemoteAppSessionMessage</span></span>

## <span data-ttu-id="89634-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89634-102">SYNOPSIS</span></span>
<span data-ttu-id="89634-103">Wysyła wiadomość do użytkownika.</span><span class="sxs-lookup"><span data-stu-id="89634-103">Sends a message to a user.</span></span>

## <span data-ttu-id="89634-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89634-104">SYNTAX</span></span>

```
Send-AzureRemoteAppSessionMessage [-CollectionName] <String> [-UserUpn] <String> [-Message] <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="89634-105">Opis</span><span class="sxs-lookup"><span data-stu-id="89634-105">DESCRIPTION</span></span>
<span data-ttu-id="89634-106">Polecenie cmdlet **send-AzureRemoteAppSessionMessage** umożliwia wysłanie wiadomości do użytkownika, który jest połączony z sesją usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="89634-106">The **Send-AzureRemoteAppSessionMessage** cmdlet sends a message to a user who is connected to an Azure RemoteApp session.</span></span>

## <span data-ttu-id="89634-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89634-107">EXAMPLES</span></span>

### <span data-ttu-id="89634-108">Przykład 1: wysyłanie wiadomości do użytkownika</span><span class="sxs-lookup"><span data-stu-id="89634-108">Example 1: Send a message to a user</span></span>
```
PS C:\> Send-AzureRemoteAppSessionMessage -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com" -Message "The system will be going down for maintenance soon.  Please save your work and close your RemoteApps."
```

<span data-ttu-id="89634-109">To polecenie wysyła wiadomość do użytkownika, którego główną nazwę użytkownika jest PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="89634-109">This command sends a message to the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="89634-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89634-110">PARAMETERS</span></span>

### <span data-ttu-id="89634-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="89634-111">-CollectionName</span></span>
<span data-ttu-id="89634-112">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="89634-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="89634-113">-Message</span><span class="sxs-lookup"><span data-stu-id="89634-113">-Message</span></span>
<span data-ttu-id="89634-114">Określa wiadomość, którą należy wysłać.</span><span class="sxs-lookup"><span data-stu-id="89634-114">Specifies the message to send.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89634-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="89634-115">-Profile</span></span>
<span data-ttu-id="89634-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89634-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="89634-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="89634-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="89634-118">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="89634-118">-UserUpn</span></span>
<span data-ttu-id="89634-119">Określa na przykład główną nazwę użytkownika (UPN) użytkownika PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="89634-119">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="89634-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89634-120">CommonParameters</span></span>
<span data-ttu-id="89634-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89634-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89634-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89634-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89634-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89634-123">INPUTS</span></span>

## <span data-ttu-id="89634-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89634-124">OUTPUTS</span></span>

## <span data-ttu-id="89634-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89634-125">NOTES</span></span>

## <span data-ttu-id="89634-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89634-126">RELATED LINKS</span></span>

[<span data-ttu-id="89634-127">Dodaj-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="89634-127">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="89634-128">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="89634-128">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="89634-129">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="89634-129">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


