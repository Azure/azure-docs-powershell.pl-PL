---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6B274EA-7FF2-46B0-8622-0DD17E9ADDD6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5531684de38a4a42aee4c131dbe58cd143370796
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055543"
---
# <span data-ttu-id="75b16-101">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="75b16-101">Get-AzureRemoteAppSession</span></span>

## <span data-ttu-id="75b16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75b16-102">SYNOPSIS</span></span>
<span data-ttu-id="75b16-103">Lista wszystkich aktywnych i rozłączonych sesji usługi Azure RemoteApp dla kolekcji.</span><span class="sxs-lookup"><span data-stu-id="75b16-103">Lists all active and disconnected Azure RemoteApp sessions for a collection.</span></span>

## <span data-ttu-id="75b16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75b16-104">SYNTAX</span></span>

```
Get-AzureRemoteAppSession [-CollectionName] <String> [[-UserUpn] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="75b16-105">Opis</span><span class="sxs-lookup"><span data-stu-id="75b16-105">DESCRIPTION</span></span>
<span data-ttu-id="75b16-106">Polecenie cmdlet **Get-AzureRemoteAppSession** wyświetla wszystkie aktywne i rozłączone sesje usługi Azure RemoteApp dla kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="75b16-106">The **Get-AzureRemoteAppSession** cmdlet lists all active and disconnected Azure RemoteApp sessions for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="75b16-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75b16-107">EXAMPLES</span></span>

### <span data-ttu-id="75b16-108">Przykład 1. Lista wszystkich sesji w kolekcji</span><span class="sxs-lookup"><span data-stu-id="75b16-108">Example 1: List all the sessions in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppSession -CollectionName "ContosoApps"
```

<span data-ttu-id="75b16-109">To polecenie wyświetla listę wszystkich sesji w kolekcji funkcji Azure RemoteApp o nazwie ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="75b16-109">This command lists all sessions in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="75b16-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75b16-110">PARAMETERS</span></span>

### <span data-ttu-id="75b16-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="75b16-111">-CollectionName</span></span>
<span data-ttu-id="75b16-112">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="75b16-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="75b16-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="75b16-113">-Profile</span></span>
<span data-ttu-id="75b16-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75b16-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="75b16-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="75b16-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="75b16-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="75b16-116">-UserUpn</span></span>
<span data-ttu-id="75b16-117">Określa główną nazwę użytkownika (UPN) użytkownika, dla którego chcesz uzyskać sesje usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="75b16-117">Specifies the user Principal Name (UPN) of a user for which to get Azure RemoteApp sessions.</span></span>
<span data-ttu-id="75b16-118">Na przykład nazwa UPN może mieć następujący format: PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="75b16-118">For example, the UPN can be in the following format: PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="75b16-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b16-119">CommonParameters</span></span>
<span data-ttu-id="75b16-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75b16-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b16-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75b16-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b16-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75b16-122">INPUTS</span></span>

## <span data-ttu-id="75b16-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75b16-123">OUTPUTS</span></span>

## <span data-ttu-id="75b16-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75b16-124">NOTES</span></span>

## <span data-ttu-id="75b16-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75b16-125">RELATED LINKS</span></span>

[<span data-ttu-id="75b16-126">Disconnect-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="75b16-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="75b16-127">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="75b16-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="75b16-128">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="75b16-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


