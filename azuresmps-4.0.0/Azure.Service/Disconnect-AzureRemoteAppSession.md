---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 514C33F8-F0B8-4F37-AB2D-BB54DD754931
online version: ''
schema: 2.0.0
ms.openlocfilehash: c256ce8ba720eb08ffec2ab56ecca40ab74f4948
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054652"
---
# <span data-ttu-id="49e31-101">Disconnect-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="49e31-101">Disconnect-AzureRemoteAppSession</span></span>

## <span data-ttu-id="49e31-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49e31-102">SYNOPSIS</span></span>
<span data-ttu-id="49e31-103">Rozłącza sesję usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="49e31-103">Disconnects an Azure RemoteApp session.</span></span>

## <span data-ttu-id="49e31-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49e31-104">SYNTAX</span></span>

```
Disconnect-AzureRemoteAppSession [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="49e31-105">Opis</span><span class="sxs-lookup"><span data-stu-id="49e31-105">DESCRIPTION</span></span>
<span data-ttu-id="49e31-106">Polecenie cmdlet **Disconnect-AzureRemoteAppSession** rozłącza sesję użytkownika usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="49e31-106">The **Disconnect-AzureRemoteAppSession** cmdlet disconnects a user's Azure RemoteApp session.</span></span>
<span data-ttu-id="49e31-107">Klient użytkownika rozłącza połączenie z sesją usługi Azure RemoteApp, ale programy użytkownika nadal działają.</span><span class="sxs-lookup"><span data-stu-id="49e31-107">The user's client disconnects from their Azure RemoteApp session, but the user's programs continue to run.</span></span>

## <span data-ttu-id="49e31-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49e31-108">EXAMPLES</span></span>

### <span data-ttu-id="49e31-109">Przykład 1. Rozłączanie sesji użytkownika</span><span class="sxs-lookup"><span data-stu-id="49e31-109">Example 1: Disconnect a user's session</span></span>
```
PS C:\> Disconnect-AzureRemoteAppSession -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="49e31-110">To polecenie rozłącza sesję usługi Azure RemoteApp w kolekcji ContosoApps dla użytkownika, którego nazwa UPN to PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="49e31-110">This command disconnects the Azure RemoteApp session in the ContosoApps collection for the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="49e31-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49e31-111">PARAMETERS</span></span>

### <span data-ttu-id="49e31-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="49e31-112">-CollectionName</span></span>
<span data-ttu-id="49e31-113">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="49e31-113">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="49e31-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="49e31-114">-Profile</span></span>
<span data-ttu-id="49e31-115">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49e31-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="49e31-116">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="49e31-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49e31-117">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="49e31-117">-UserUpn</span></span>
<span data-ttu-id="49e31-118">Określa na przykład główną nazwę użytkownika (UPN) użytkownika PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="49e31-118">Specifies the User Principal Name (UPN) of a user, for example PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="49e31-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e31-119">CommonParameters</span></span>
<span data-ttu-id="49e31-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49e31-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49e31-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49e31-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e31-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49e31-122">INPUTS</span></span>

## <span data-ttu-id="49e31-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49e31-123">OUTPUTS</span></span>

## <span data-ttu-id="49e31-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49e31-124">NOTES</span></span>

## <span data-ttu-id="49e31-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49e31-125">RELATED LINKS</span></span>

[<span data-ttu-id="49e31-126">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="49e31-126">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="49e31-127">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="49e31-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="49e31-128">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="49e31-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


