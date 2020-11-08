---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F101382E-B015-4913-B4A0-8827EC423319
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37c4bf3ad2c2aaf74f268b18d17b6af71f4f2fc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054850"
---
# <span data-ttu-id="7130f-101">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="7130f-101">Publish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="7130f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7130f-102">SYNOPSIS</span></span>
<span data-ttu-id="7130f-103">Publikuje Program Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="7130f-103">Publishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="7130f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7130f-104">SYNTAX</span></span>

### <span data-ttu-id="7130f-105">Identyfikator aplikacji (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7130f-105">App Id (Default)</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-StartMenuAppId] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7130f-106">Ścieżka aplikacji</span><span class="sxs-lookup"><span data-stu-id="7130f-106">App Path</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-FileVirtualPath] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7130f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7130f-107">DESCRIPTION</span></span>
<span data-ttu-id="7130f-108">Polecenie cmdlet **Publish-AzureRemoteAppProgram** publikuje Program Azure RemoteApp, który udostępnia go użytkownikom kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="7130f-108">The **Publish-AzureRemoteAppProgram** cmdlet publishes an Azure RemoteApp program, which makes it available to users of the Azure RemoteApp collection.</span></span>

## <span data-ttu-id="7130f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7130f-109">EXAMPLES</span></span>

### <span data-ttu-id="7130f-110">Przykład 1: publikowanie programu w kolekcji</span><span class="sxs-lookup"><span data-stu-id="7130f-110">Example 1: Publish a program in a collection</span></span>
```
PS C:\> Publish-AzureRemoteAppProgram -CollectionName "ContosoApps" -StartMenuAppId "a3732322-89a5-4cbc-9844-9634c74d337f" -DisplayName "Finance App"
```

<span data-ttu-id="7130f-111">To polecenie publikuje program w kolekcji ContosoApps z określonym *StartMenuAppId* w celu dodania programu do menu Start.</span><span class="sxs-lookup"><span data-stu-id="7130f-111">This command publishes the program in the ContosoApps collection with the specified *StartMenuAppId* to add the program to the Start Menu.</span></span>
<span data-ttu-id="7130f-112">Opublikowana aplikacja będzie mieć nazwę wyświetlaną "aplikacja finansowa".</span><span class="sxs-lookup"><span data-stu-id="7130f-112">The published app will have a display name of "Finance App".</span></span>

## <span data-ttu-id="7130f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7130f-113">PARAMETERS</span></span>

### <span data-ttu-id="7130f-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="7130f-114">-CollectionName</span></span>
<span data-ttu-id="7130f-115">Określa nazwę kolekcji funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="7130f-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="7130f-116">-CommandLine</span><span class="sxs-lookup"><span data-stu-id="7130f-116">-CommandLine</span></span>
<span data-ttu-id="7130f-117">Określa argumenty wiersza polecenia dla programu, który jest publikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7130f-117">Specifies command-line arguments for the program that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="7130f-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7130f-118">-DisplayName</span></span>
<span data-ttu-id="7130f-119">Określa przyjazną dla użytkownika nazwę wyświetlaną programu Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="7130f-119">Specifies the user-friendly display name of the Azure RemoteApp program.</span></span>
<span data-ttu-id="7130f-120">Użytkownicy widzą tę nazwę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="7130f-120">Users see this as the name of the application.</span></span>

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

### <span data-ttu-id="7130f-121">-FileVirtualPath</span><span class="sxs-lookup"><span data-stu-id="7130f-121">-FileVirtualPath</span></span>
<span data-ttu-id="7130f-122">Określa ścieżkę programu w obrazie szablonu programu.</span><span class="sxs-lookup"><span data-stu-id="7130f-122">Specifies the path of the program within the template image of the program.</span></span>

```yaml
Type: String
Parameter Sets: App Path
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7130f-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="7130f-123">-Profile</span></span>
<span data-ttu-id="7130f-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7130f-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7130f-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="7130f-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7130f-126">-StartMenuAppId</span><span class="sxs-lookup"><span data-stu-id="7130f-126">-StartMenuAppId</span></span>
<span data-ttu-id="7130f-127">Określa identyfikator GUID, którego używa polecenie cmdlet w celu dodania programu do menu Start.</span><span class="sxs-lookup"><span data-stu-id="7130f-127">Specifies a GUID that this cmdlet uses to add the program to the Start Menu.</span></span>

```yaml
Type: String
Parameter Sets: App Id
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7130f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7130f-128">CommonParameters</span></span>
<span data-ttu-id="7130f-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7130f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7130f-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7130f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7130f-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7130f-131">INPUTS</span></span>

## <span data-ttu-id="7130f-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7130f-132">OUTPUTS</span></span>

## <span data-ttu-id="7130f-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7130f-133">NOTES</span></span>

## <span data-ttu-id="7130f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7130f-134">RELATED LINKS</span></span>

[<span data-ttu-id="7130f-135">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="7130f-135">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="7130f-136">Cofnięcie publikowania — AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="7130f-136">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


