---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 636280D6-32C3-48EF-A271-A4E032F8B334
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0dab3720a4680805e16f695a1ab1b2350554e8f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055285"
---
# <span data-ttu-id="1837e-101">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="1837e-101">Get-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="1837e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1837e-102">SYNOPSIS</span></span>
<span data-ttu-id="1837e-103">Pobiera właściwości jednego lub większej liczby opublikowanych programów RemoteApp usługi Azure dla kolekcji.</span><span class="sxs-lookup"><span data-stu-id="1837e-103">Retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="1837e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1837e-104">SYNTAX</span></span>

### <span data-ttu-id="1837e-105">FilterByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1837e-105">FilterByName (Default)</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-RemoteAppProgram] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="1837e-106">FilterByAlias</span><span class="sxs-lookup"><span data-stu-id="1837e-106">FilterByAlias</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1837e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1837e-107">DESCRIPTION</span></span>
<span data-ttu-id="1837e-108">Polecenie cmdlet **Get-AzureRemoteAppProgram** pobiera właściwości jednego lub większej liczby opublikowanych programów funkcji Azure RemoteApp dla kolekcji.</span><span class="sxs-lookup"><span data-stu-id="1837e-108">The **Get-AzureRemoteAppProgram** cmdlet retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="1837e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1837e-109">EXAMPLES</span></span>

### <span data-ttu-id="1837e-110">Przykład 1: pobieranie właściwości programu</span><span class="sxs-lookup"><span data-stu-id="1837e-110">Example 1: Retrieve the properties of a program</span></span>
```
PS C:\> Get-AzureRemoteAppProgram -CollectionName "ContosoApps" -RemoteAppProgram "Finance App"

Alias                : edc85816-4b9e-4284-b3dc-faedb505f5d9

AvailableToUsers     : True

CommandLineArguments : 

IconPngUris          : Microsoft.Azure.Management.RemoteApp.Models.IconPngUrisType

IconUri              : https://liverdcxstorage.blob.core.windows.net/icons/12345678-1234-1234-1234-123412341234.ico?se=2015-03-01T17%3A29%3A51Z&amp;amp;sr=b&amp;amp;sp=r&amp;amp;sig=abcdCCavbcF%2asY4RascaBauishCasd2FasdBHtasd2BPasdi5dasdD

Name                 : Contoso Finance

Status               : Published

VirtualPath          : %SYSTEMDRIVE%\Program Files (x86)\Contoso Finance\Finance.exe
```

<span data-ttu-id="1837e-111">To polecenie wyświetla właściwości programu usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="1837e-111">This command displays the properties of an Azure RemoteApp program.</span></span>
<span data-ttu-id="1837e-112">Program o nazwie aplikacja finansowa znajduje się w kolekcji funkcji Azure RemoteApp o nazwie ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="1837e-112">The program, named Finance App, is in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="1837e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1837e-113">PARAMETERS</span></span>

### <span data-ttu-id="1837e-114">-Alias</span><span class="sxs-lookup"><span data-stu-id="1837e-114">-Alias</span></span>
<span data-ttu-id="1837e-115">Określa alias programu, dla którego mają zostać pobrane właściwości.</span><span class="sxs-lookup"><span data-stu-id="1837e-115">Specifies the alias of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByAlias
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1837e-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="1837e-116">-CollectionName</span></span>
<span data-ttu-id="1837e-117">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="1837e-117">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="1837e-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="1837e-118">-Profile</span></span>
<span data-ttu-id="1837e-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1837e-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1837e-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1837e-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1837e-121">-RemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="1837e-121">-RemoteAppProgram</span></span>
<span data-ttu-id="1837e-122">Określa nazwę programu, dla którego mają zostać pobrane właściwości.</span><span class="sxs-lookup"><span data-stu-id="1837e-122">Specifies the name of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="1837e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1837e-123">CommonParameters</span></span>
<span data-ttu-id="1837e-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1837e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1837e-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1837e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1837e-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1837e-126">INPUTS</span></span>

## <span data-ttu-id="1837e-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1837e-127">OUTPUTS</span></span>

## <span data-ttu-id="1837e-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1837e-128">NOTES</span></span>

## <span data-ttu-id="1837e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1837e-129">RELATED LINKS</span></span>

[<span data-ttu-id="1837e-130">Publikowanie — AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="1837e-130">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)

[<span data-ttu-id="1837e-131">Cofnięcie publikowania — AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="1837e-131">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


