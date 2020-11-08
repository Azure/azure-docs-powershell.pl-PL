---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055545"
---
# <span data-ttu-id="bc624-101">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="bc624-101">Get-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="bc624-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc624-102">SYNOPSIS</span></span>
<span data-ttu-id="bc624-103">Pobiera informacje o obrazach szablonów usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="bc624-103">Retrieves information about Azure RemoteApp template images.</span></span>

## <span data-ttu-id="bc624-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc624-104">SYNTAX</span></span>

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bc624-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bc624-105">DESCRIPTION</span></span>
<span data-ttu-id="bc624-106">Polecenie cmdlet **Get-AzureRemoteAppTemplateImage** pobiera informacje o obrazach szablonów usługi Azure RemoteApp na platformie Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bc624-106">The **Get-AzureRemoteAppTemplateImage** cmdlet retrieves information about Azure RemoteApp template images in Microsoft Azure.</span></span>
<span data-ttu-id="bc624-107">To polecenie cmdlet zwraca obiekt zawierający informacje o określonym obrazie szablonu.</span><span class="sxs-lookup"><span data-stu-id="bc624-107">This cmdlet returns an object containing information about a specified template image.</span></span>
<span data-ttu-id="bc624-108">Jeśli nie określono żadnego obrazu szablonu, pobiera on informacje o wszystkich obrazach szablonów w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bc624-108">If no template image is specified, it retrieves information about all the template images in the current subscription.</span></span>

## <span data-ttu-id="bc624-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc624-109">EXAMPLES</span></span>

### <span data-ttu-id="bc624-110">Przykład 1. Pobieranie listy wszystkich obrazów szablonów</span><span class="sxs-lookup"><span data-stu-id="bc624-110">Example 1: Get a list of all template images</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

<span data-ttu-id="bc624-111">To polecenie zwraca listę wszystkich obrazów szablonów.</span><span class="sxs-lookup"><span data-stu-id="bc624-111">This command returns the list of all template images.</span></span>

### <span data-ttu-id="bc624-112">Przykład 2: uzyskiwanie informacji o określonym obrazie szablonu</span><span class="sxs-lookup"><span data-stu-id="bc624-112">Example 2: Retrieve information about a specified template image</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="bc624-113">To polecenie pobiera informacje o obrazie szablonu o nazwie ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="bc624-113">This command retrieves information about the template image named ContosoApps.</span></span>

## <span data-ttu-id="bc624-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc624-114">PARAMETERS</span></span>

### <span data-ttu-id="bc624-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="bc624-115">-ImageName</span></span>
<span data-ttu-id="bc624-116">Określa nazwę obrazu szablonu usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="bc624-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="bc624-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="bc624-117">-Profile</span></span>
<span data-ttu-id="bc624-118">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc624-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bc624-119">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="bc624-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bc624-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc624-120">CommonParameters</span></span>
<span data-ttu-id="bc624-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc624-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc624-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc624-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc624-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc624-123">INPUTS</span></span>

## <span data-ttu-id="bc624-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc624-124">OUTPUTS</span></span>

## <span data-ttu-id="bc624-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc624-125">NOTES</span></span>

## <span data-ttu-id="bc624-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc624-126">RELATED LINKS</span></span>

[<span data-ttu-id="bc624-127">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="bc624-127">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="bc624-128">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="bc624-128">Get-AzureRemoteAppStartMenuProgram</span></span>](./Get-AzureRemoteAppStartMenuProgram.md)


