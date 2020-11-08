---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 608B4B5E-5DB2-4291-966C-0B25F8D4FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 18c5f50a2804aeca545c44a5c0728bf7003e9d8e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055017"
---
# <span data-ttu-id="ed788-101">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="ed788-101">Set-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="ed788-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed788-102">SYNOPSIS</span></span>
<span data-ttu-id="ed788-103">Ustawia właściwości obszaru roboczego usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="ed788-103">Sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="ed788-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed788-104">SYNTAX</span></span>

```
Set-AzureRemoteAppWorkspace [-WorkspaceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ed788-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ed788-105">DESCRIPTION</span></span>
<span data-ttu-id="ed788-106">Polecenie cmdlet **Set-AzureRemoteAppWorkspace** ustawia właściwości obszaru roboczego usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="ed788-106">The **Set-AzureRemoteAppWorkspace** cmdlet sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="ed788-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed788-107">EXAMPLES</span></span>

### <span data-ttu-id="ed788-108">Przykład 1. Ustawianie nazwy obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="ed788-108">Example 1: Set the workspace name</span></span>
```
PS C:\> Set-AzureRemoteAppWorkspace -WorkspaceName "Contoso Work Applications"

TrackingId
----------
12345
```

<span data-ttu-id="ed788-109">To polecenie ustawia nazwę obszaru roboczego usługi Azure RemoteApp na aplikacje firm contoso.</span><span class="sxs-lookup"><span data-stu-id="ed788-109">This command sets the Azure RemoteApp workspace name to Contoso Work Applications.</span></span>

## <span data-ttu-id="ed788-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed788-110">PARAMETERS</span></span>

### <span data-ttu-id="ed788-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="ed788-111">-Profile</span></span>
<span data-ttu-id="ed788-112">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed788-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ed788-113">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ed788-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ed788-114">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="ed788-114">-WorkspaceName</span></span>
<span data-ttu-id="ed788-115">Określa nazwę obszaru roboczego funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="ed788-115">Specifies the name of the Azure RemoteApp workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed788-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed788-116">CommonParameters</span></span>
<span data-ttu-id="ed788-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed788-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed788-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed788-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed788-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed788-119">INPUTS</span></span>

## <span data-ttu-id="ed788-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed788-120">OUTPUTS</span></span>

## <span data-ttu-id="ed788-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed788-121">NOTES</span></span>
* <span data-ttu-id="ed788-122">Wszystkie kolekcje usługi Azure RemoteApp dla określonego abonamentu istnieją w udostępnionym obszarze roboczym.</span><span class="sxs-lookup"><span data-stu-id="ed788-122">All Azure RemoteApp collections for a specified subscription exist within a shared workspace.</span></span>

## <span data-ttu-id="ed788-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed788-123">RELATED LINKS</span></span>

[<span data-ttu-id="ed788-124">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="ed788-124">Get-AzureRemoteAppWorkspace</span></span>](./Get-AzureRemoteAppWorkspace.md)


