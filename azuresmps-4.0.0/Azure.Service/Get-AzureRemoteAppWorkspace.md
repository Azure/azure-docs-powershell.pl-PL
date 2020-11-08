---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 035B294E-6A1B-41E9-ACFF-D66F9C1A0B11
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9218862bb1e61abe548a94ed5297a6ce69237d54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054585"
---
# <span data-ttu-id="44c14-101">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="44c14-101">Get-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="44c14-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44c14-102">SYNOPSIS</span></span>
<span data-ttu-id="44c14-103">Pobiera informacje o obszarze roboczym usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="44c14-103">Retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="44c14-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44c14-104">SYNTAX</span></span>

```
Get-AzureRemoteAppWorkspace [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="44c14-105">Opis</span><span class="sxs-lookup"><span data-stu-id="44c14-105">DESCRIPTION</span></span>
<span data-ttu-id="44c14-106">Polecenie cmdlet **Get-AzureRemoteAppWorkspace** pobiera informacje o obszarze roboczym usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="44c14-106">The **Get-AzureRemoteAppWorkspace** cmdlet retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="44c14-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44c14-107">EXAMPLES</span></span>

### <span data-ttu-id="44c14-108">Przykład 1: pobieranie informacji o obszarze roboczym</span><span class="sxs-lookup"><span data-stu-id="44c14-108">Example 1: Retrieve information about a workspace</span></span>
```
PS C:\> Get-AzureRemoteAppWorkspace
ClientUrl                               EndUserFeedName
---------                               ---------------
https://www.remoteapp.windowsazure.com/ Contoso Work Applications
```

<span data-ttu-id="44c14-109">To polecenie pobiera informacje o obszarze roboczym usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="44c14-109">This command retrieves information about the Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="44c14-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44c14-110">PARAMETERS</span></span>

### <span data-ttu-id="44c14-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="44c14-111">-Profile</span></span>
<span data-ttu-id="44c14-112">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44c14-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="44c14-113">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="44c14-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44c14-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c14-114">CommonParameters</span></span>
<span data-ttu-id="44c14-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44c14-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c14-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44c14-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c14-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44c14-117">INPUTS</span></span>

## <span data-ttu-id="44c14-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44c14-118">OUTPUTS</span></span>

## <span data-ttu-id="44c14-119">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44c14-119">NOTES</span></span>

## <span data-ttu-id="44c14-120">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44c14-120">RELATED LINKS</span></span>

[<span data-ttu-id="44c14-121">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="44c14-121">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)


