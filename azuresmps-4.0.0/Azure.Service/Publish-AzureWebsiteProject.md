---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D866554F-78B0-4691-BA06-F625F9B0DFC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 366941504c020910735015e3d8b282af376d54d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054843"
---
# <span data-ttu-id="1a7d4-101">Publish-AzureWebsiteProject</span><span class="sxs-lookup"><span data-stu-id="1a7d4-101">Publish-AzureWebsiteProject</span></span>

## <span data-ttu-id="1a7d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1a7d4-102">SYNOPSIS</span></span>
<span data-ttu-id="1a7d4-103">Publikowanie projektu programu Visual Studio w sieci Web w witrynie usługi Microsoft Azure w sieci Web za pomocą aplikacji webdeploy.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-103">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>

## <span data-ttu-id="1a7d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1a7d4-104">SYNTAX</span></span>

### <span data-ttu-id="1a7d4-105">ProjectFile</span><span class="sxs-lookup"><span data-stu-id="1a7d4-105">ProjectFile</span></span>
```
Publish-AzureWebsiteProject -ProjectFile <String> [-Configuration <String>] [-ConnectionString <Hashtable>]
 [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a7d4-106">Pakietu</span><span class="sxs-lookup"><span data-stu-id="1a7d4-106">Package</span></span>
```
Publish-AzureWebsiteProject -Package <String> [-ConnectionString <Hashtable>] [-Tokens <String>]
 [-SetParametersFile <String>] [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1a7d4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1a7d4-107">DESCRIPTION</span></span>
<span data-ttu-id="1a7d4-108">Publikowanie projektu programu Visual Studio w sieci Web w witrynie usługi Microsoft Azure w sieci Web za pomocą aplikacji webdeploy.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-108">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>
<span data-ttu-id="1a7d4-109">Może wykonać pakiet webdeploy i opublikować go bezpośrednio albo utworzyć projekt w sieci Web programu Visual Studio, zbudować projekt i publikować.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-109">It can either take a WebDeploy package and publish directly, or take a Visual Studio web project, build the project and publish.</span></span>
<span data-ttu-id="1a7d4-110">Może także zastąpić parametry połączenia w Web.config podczas publikowania.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-110">It can also replace the connection strings in the Web.config during publish.</span></span>

## <span data-ttu-id="1a7d4-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1a7d4-111">EXAMPLES</span></span>

### <span data-ttu-id="1a7d4-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1a7d4-112">Example 1</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -Configuration Debug
```

<span data-ttu-id="1a7d4-113">Tworzenie projektu programu Visual Studio w sieci Web z konfiguracją "Debugowanie" (oznacza używanie Web.Debug.config) i publikowanie w witrynie Microsoft Azure w sieci Web za pomocą aplikacji webdeploy.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-113">Build a Visual Studio web project with "Debug" configuration (meaning use Web.Debug.config) and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="1a7d4-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1a7d4-114">Example 2</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1.zip
```

<span data-ttu-id="1a7d4-115">Publikowanie pliku. zip pakietu webdeploy w witrynie sieci Web platformy Microsoft Azure za pomocą aplikacji webdeploy.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-115">Publish a WebDeploy Package .zip file to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="1a7d4-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="1a7d4-116">Example 3</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1
```

<span data-ttu-id="1a7d4-117">Publikowanie folderu pakietu webdeploy w witrynie sieci Web platformy Microsoft Azure za pomocą aplikacji webdeploy.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-117">Publish a WebDeploy Package folder to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="1a7d4-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="1a7d4-118">Example 4</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -ConnectionString @{ DefaultConnection = "my connection string" }
```

<span data-ttu-id="1a7d4-119">Utwórz projekt programu Visual Studio w sieci Web, Zastąp ciąg połączenia "DefaultConnection" w Web.config i opublikuj go w witrynie sieci Web platformy Microsoft Azure za pomocą narzędzia webdeploy.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-119">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="1a7d4-120">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="1a7d4-120">Example 5</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -DefaultConnection "my connection string"
```

<span data-ttu-id="1a7d4-121">Utwórz projekt programu Visual Studio w sieci Web, Zastąp ciąg połączenia "DefaultConnection" w Web.config i opublikuj go w witrynie sieci Web platformy Microsoft Azure za pomocą narzędzia webdeploy.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-121">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>
<span data-ttu-id="1a7d4-122">Zwróć uwagę, że DefaultConnection jest parametrem dynamicznym, który zostanie dodany przez przeanalizowanie Web.config.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-122">Notice that -DefaultConnection is a dynamic parameter which gets added by parsing Web.config.</span></span>

## <span data-ttu-id="1a7d4-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a7d4-123">PARAMETERS</span></span>

### <span data-ttu-id="1a7d4-124">— Konfiguracja</span><span class="sxs-lookup"><span data-stu-id="1a7d4-124">-Configuration</span></span>
<span data-ttu-id="1a7d4-125">Konfiguracja używana do konstruowania projektu aplikacji sieci Web programu Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-125">The configuration used to build the Visual Studio web application project.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a7d4-126">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1a7d4-126">-ConnectionString</span></span>
<span data-ttu-id="1a7d4-127">Parametry połączenia używane do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-127">The connection strings to use for the deployment.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a7d4-128">-DoNotDelete</span><span class="sxs-lookup"><span data-stu-id="1a7d4-128">-DoNotDelete</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a7d4-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1a7d4-129">-Name</span></span>
<span data-ttu-id="1a7d4-130">Nazwa witryny sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-130">The web site name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a7d4-131">-Package</span><span class="sxs-lookup"><span data-stu-id="1a7d4-131">-Package</span></span>
<span data-ttu-id="1a7d4-132">Folder pakietu webdeploy na potrzeby publikowania pliku zip projektu aplikacji sieci Web programu Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-132">The WebDeploy package folder for zip file of the Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a7d4-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="1a7d4-133">-Profile</span></span>
<span data-ttu-id="1a7d4-134">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1a7d4-135">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1a7d4-136">-ProjectFile</span><span class="sxs-lookup"><span data-stu-id="1a7d4-136">-ProjectFile</span></span>
<span data-ttu-id="1a7d4-137">Projekt aplikacji sieci Web Visual Studio, który ma zostać opublikowany.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-137">The Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a7d4-138">-SetParametersFile</span><span class="sxs-lookup"><span data-stu-id="1a7d4-138">-SetParametersFile</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a7d4-139">-SkipAppData</span><span class="sxs-lookup"><span data-stu-id="1a7d4-139">-SkipAppData</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a7d4-140">-Slot</span><span class="sxs-lookup"><span data-stu-id="1a7d4-140">-Slot</span></span>
<span data-ttu-id="1a7d4-141">Nazwa miejsca w witrynie sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-141">The web site slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a7d4-142">-Tokens</span><span class="sxs-lookup"><span data-stu-id="1a7d4-142">-Tokens</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a7d4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a7d4-143">CommonParameters</span></span>
<span data-ttu-id="1a7d4-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a7d4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a7d4-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a7d4-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a7d4-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a7d4-146">INPUTS</span></span>

## <span data-ttu-id="1a7d4-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1a7d4-147">OUTPUTS</span></span>

## <span data-ttu-id="1a7d4-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1a7d4-148">NOTES</span></span>

## <span data-ttu-id="1a7d4-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a7d4-149">RELATED LINKS</span></span>

[<span data-ttu-id="1a7d4-150">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1a7d4-150">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="1a7d4-151">Nowe — AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1a7d4-151">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="1a7d4-152">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1a7d4-152">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="1a7d4-153">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1a7d4-153">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


