---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D40937C2-9BF7-4371-A64C-B44F5B6B895E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c9882e805504b2e3b2e4f4ebbe661268b2327a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055537"
---
# <span data-ttu-id="7dce2-101">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="7dce2-101">Get-AzureRemoteAppVM</span></span>

## <span data-ttu-id="7dce2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7dce2-102">SYNOPSIS</span></span>
<span data-ttu-id="7dce2-103">Pobiera maszyny wirtualne w kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="7dce2-103">Gets the virtual machines in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="7dce2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7dce2-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVM -CollectionName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7dce2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7dce2-105">DESCRIPTION</span></span>
<span data-ttu-id="7dce2-106">Polecenie cmdlet **Get-AzureRemoteAppVM** pobiera maszyny wirtualne utworzone w ramach kolekcji funkcji Azure RemoteApp na potrzeby hostingu sesji.</span><span class="sxs-lookup"><span data-stu-id="7dce2-106">The **Get-AzureRemoteAppVM** cmdlet gets the virtual machines created under an Azure RemoteApp collection for session hosting.</span></span>

## <span data-ttu-id="7dce2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7dce2-107">EXAMPLES</span></span>

### <span data-ttu-id="7dce2-108">Przykład 1: wyświetlanie maszyn wirtualnych w kolekcji</span><span class="sxs-lookup"><span data-stu-id="7dce2-108">Example 1: Display the virtual machines in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppVM -CollectionName "Contoso"
```

<span data-ttu-id="7dce2-109">To polecenie wyświetla maszyny wirtualne używane do obsługi sesji w kolekcji funkcji Azure RemoteApp o nazwie contoso.</span><span class="sxs-lookup"><span data-stu-id="7dce2-109">This command displays the virtual machines used for session hosting in an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="7dce2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7dce2-110">PARAMETERS</span></span>

### <span data-ttu-id="7dce2-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="7dce2-111">-CollectionName</span></span>
<span data-ttu-id="7dce2-112">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="7dce2-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dce2-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="7dce2-113">-Profile</span></span>
<span data-ttu-id="7dce2-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dce2-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7dce2-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="7dce2-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7dce2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dce2-116">CommonParameters</span></span>
<span data-ttu-id="7dce2-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dce2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dce2-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dce2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dce2-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7dce2-119">INPUTS</span></span>

## <span data-ttu-id="7dce2-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7dce2-120">OUTPUTS</span></span>

## <span data-ttu-id="7dce2-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7dce2-121">NOTES</span></span>

## <span data-ttu-id="7dce2-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7dce2-122">RELATED LINKS</span></span>

[<span data-ttu-id="7dce2-123">Restart-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="7dce2-123">Restart-AzureRemoteAppVM</span></span>](./Restart-AzureRemoteAppVM.md)


