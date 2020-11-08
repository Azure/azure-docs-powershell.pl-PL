---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: FCDEA955-EB64-4EEA-9F4A-04E2C1F0A831
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83664e8be9241782e42d7ba7634691668ed575f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055281"
---
# <span data-ttu-id="fe9a4-101">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="fe9a4-101">Get-AzureRemoteAppStartMenuProgram</span></span>

## <span data-ttu-id="fe9a4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe9a4-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9a4-103">Wyświetla listę programów menu Start w kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="fe9a4-103">Lists the Start Menu programs in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="fe9a4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe9a4-104">SYNTAX</span></span>

```
Get-AzureRemoteAppStartMenuProgram [-CollectionName] <String> [[-ProgramName] <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fe9a4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fe9a4-105">DESCRIPTION</span></span>
<span data-ttu-id="fe9a4-106">Polecenie cmdlet **Get-AzureRemoteAppStartMenuProgram** zawiera listę programów menu Start znajdujących się na obrazie szablonu używanym przez kolekcję funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="fe9a4-106">The **Get-AzureRemoteAppStartMenuProgram** cmdlet lists the Start Menu programs in the template image that an Azure RemoteApp collection uses.</span></span>

## <span data-ttu-id="fe9a4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe9a4-107">EXAMPLES</span></span>

### <span data-ttu-id="fe9a4-108">Przykład 1: Wyświetlanie programów menu Start dla kolekcji</span><span class="sxs-lookup"><span data-stu-id="fe9a4-108">Example 1: List the Start Menu programs for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppStartMenuProgram -CollectionName "ContosoApps"
```

<span data-ttu-id="fe9a4-109">To polecenie zwraca listę programów menu Start dla kolekcji ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="fe9a4-109">This command returns the list of Start Menu programs for the ContosoApps collection.</span></span>

## <span data-ttu-id="fe9a4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe9a4-110">PARAMETERS</span></span>

### <span data-ttu-id="fe9a4-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="fe9a4-111">-CollectionName</span></span>
<span data-ttu-id="fe9a4-112">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="fe9a4-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="fe9a4-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="fe9a4-113">-Profile</span></span>
<span data-ttu-id="fe9a4-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe9a4-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fe9a4-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="fe9a4-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fe9a4-116">-ProgramName</span><span class="sxs-lookup"><span data-stu-id="fe9a4-116">-ProgramName</span></span>
<span data-ttu-id="fe9a4-117">Określa nazwę programu, dla którego należy wyświetlić informacje.</span><span class="sxs-lookup"><span data-stu-id="fe9a4-117">Specifies the name of a program for which to list information.</span></span>

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

### <span data-ttu-id="fe9a4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9a4-118">CommonParameters</span></span>
<span data-ttu-id="fe9a4-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe9a4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9a4-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe9a4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9a4-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe9a4-121">INPUTS</span></span>

## <span data-ttu-id="fe9a4-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe9a4-122">OUTPUTS</span></span>

## <span data-ttu-id="fe9a4-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe9a4-123">NOTES</span></span>

## <span data-ttu-id="fe9a4-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe9a4-124">RELATED LINKS</span></span>

[<span data-ttu-id="fe9a4-125">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="fe9a4-125">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)


