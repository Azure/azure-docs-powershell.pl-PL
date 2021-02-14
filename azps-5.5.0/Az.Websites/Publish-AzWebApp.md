---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 6080f9a5c8ceb18aa2bf6a37a034372d3bfb40a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241523"
---
# <span data-ttu-id="555fd-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="555fd-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="555fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="555fd-102">SYNOPSIS</span></span>
<span data-ttu-id="555fd-103">Wdraża aplikację Azure Web App z pliku ZIP, JAR lub WAR przy użyciu zipdeploy.</span><span class="sxs-lookup"><span data-stu-id="555fd-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="555fd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="555fd-104">SYNTAX</span></span>

### <span data-ttu-id="555fd-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="555fd-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="555fd-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="555fd-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="555fd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="555fd-107">DESCRIPTION</span></span>
<span data-ttu-id="555fd-108">Polecenie **cmdlet Publish-AzWebApp** umożliwia przekazywanie zawartości do istniejącej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="555fd-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="555fd-109">Zawartość powinna zostać spakowana do pliku ZIP, jeśli używasz stosów, takich jak .NET, Python, Node lub plik WAR lub JAR, jeśli używasz języka Java.</span><span class="sxs-lookup"><span data-stu-id="555fd-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="555fd-110">Zawartość powinna być wstępnie wbudowana i gotowa do użycia bez dodatkowych kroków kompilacji podczas wdrażania.</span><span class="sxs-lookup"><span data-stu-id="555fd-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="555fd-111">To polecenie cmdlet używa funkcji zipdeploy i wardeploy kudu do wdrażania zawartości.</span><span class="sxs-lookup"><span data-stu-id="555fd-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="555fd-112">Aby uzyskać szczegółowe informacje o tym, jak działają aplikacje zipdeploy i wardeploy oraz jak poprawnie spakować aplikację sieci Web do wdrożenia, zobacz witrynę typu wiki firmy Kudu.</span><span class="sxs-lookup"><span data-stu-id="555fd-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="555fd-113"> https://aka.ms/kuduzipdeploy i https://aka.ms/kuduwardeploy zawierają pomocne informacje na temat zipdeploy i wardeploy.</span><span class="sxs-lookup"><span data-stu-id="555fd-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="555fd-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="555fd-114">EXAMPLES</span></span>

### <span data-ttu-id="555fd-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="555fd-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="555fd-116">Przekazanie zawartości pliku app.zip do aplikacji sieci Web o nazwie MyApp należącej do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="555fd-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="555fd-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="555fd-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="555fd-118">Przekazanie zawartości pliku javaproject.war do miejsca tymczasowego aplikacji sieci Web o nazwie ContosoApp należącej do grupy zasobów ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="555fd-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="555fd-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="555fd-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="555fd-120">Przekazanie zawartości pliku app.zip do aplikacji sieci Web o nazwie ContosoApp należącej do grupy zasobów ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="555fd-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="555fd-121">Polecenie cmdlet zostanie uruchomione w zadaniu w tle.</span><span class="sxs-lookup"><span data-stu-id="555fd-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="555fd-122">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="555fd-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="555fd-123">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="555fd-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="555fd-124">Przekazanie zawartości pliku java_app.jar do aplikacji sieci Web o nazwie ContosoApp należącej do grupy zasobów ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="555fd-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="555fd-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="555fd-125">PARAMETERS</span></span>

### <span data-ttu-id="555fd-126">- ArchivePath</span><span class="sxs-lookup"><span data-stu-id="555fd-126">-ArchivePath</span></span>
<span data-ttu-id="555fd-127">Ścieżka pliku archiwum.</span><span class="sxs-lookup"><span data-stu-id="555fd-127">The path of the archive file.</span></span> <span data-ttu-id="555fd-128">Obsługiwane są kody ZIP, WAR i JAR.</span><span class="sxs-lookup"><span data-stu-id="555fd-128">ZIP, WAR, and JAR are supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555fd-129">— AsJob</span><span class="sxs-lookup"><span data-stu-id="555fd-129">-AsJob</span></span>
<span data-ttu-id="555fd-130">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="555fd-130">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555fd-131">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="555fd-131">-Force</span></span>
<span data-ttu-id="555fd-132">Wymuszanie usuwania opcji</span><span class="sxs-lookup"><span data-stu-id="555fd-132">Forcefully Remove Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555fd-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="555fd-133">-DefaultProfile</span></span>
<span data-ttu-id="555fd-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="555fd-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555fd-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="555fd-135">-Name</span></span>
<span data-ttu-id="555fd-136">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="555fd-136">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="555fd-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="555fd-137">-ResourceGroupName</span></span>
<span data-ttu-id="555fd-138">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="555fd-138">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="555fd-139">— Slot</span><span class="sxs-lookup"><span data-stu-id="555fd-139">-Slot</span></span>
<span data-ttu-id="555fd-140">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="555fd-140">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="555fd-141">— WebApp</span><span class="sxs-lookup"><span data-stu-id="555fd-141">-WebApp</span></span>
<span data-ttu-id="555fd-142">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="555fd-142">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="555fd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="555fd-143">CommonParameters</span></span>
<span data-ttu-id="555fd-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="555fd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="555fd-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="555fd-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="555fd-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="555fd-146">INPUTS</span></span>

### <span data-ttu-id="555fd-147">System.String</span><span class="sxs-lookup"><span data-stu-id="555fd-147">System.String</span></span>

### <span data-ttu-id="555fd-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="555fd-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="555fd-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="555fd-149">OUTPUTS</span></span>

### <span data-ttu-id="555fd-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="555fd-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="555fd-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="555fd-151">NOTES</span></span>

## <span data-ttu-id="555fd-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="555fd-152">RELATED LINKS</span></span>
