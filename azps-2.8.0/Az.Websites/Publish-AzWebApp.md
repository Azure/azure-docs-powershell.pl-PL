---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 07ec4223414bbdbab8e3fa4d11641d040d918209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888281"
---
# <span data-ttu-id="5d007-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5d007-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="5d007-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d007-102">SYNOPSIS</span></span>
<span data-ttu-id="5d007-103">Wdrażanie aplikacji Azure Web App z pliku ZIP, JAR lub WAR przy użyciu zipdeploy.</span><span class="sxs-lookup"><span data-stu-id="5d007-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="5d007-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d007-104">SYNTAX</span></span>

### <span data-ttu-id="5d007-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="5d007-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d007-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="5d007-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d007-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5d007-107">DESCRIPTION</span></span>
<span data-ttu-id="5d007-108">Polecenie cmdlet **Publish-AzWebApp** umożliwia przekazywanie zawartości do istniejącej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5d007-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="5d007-109">Zawartość powinna zostać spakowana w pliku ZIP, jeśli korzystasz ze stosów, takich jak .NET, Python lub Node, lub pliku WAR lub JAR, jeśli korzystasz z języka Java.</span><span class="sxs-lookup"><span data-stu-id="5d007-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="5d007-110">Zawartość powinna być wstępnie zbudowana i gotowa do uruchomienia bez dodatkowych kroków kompilacji podczas wdrażania.</span><span class="sxs-lookup"><span data-stu-id="5d007-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="5d007-111">To polecenie cmdlet umożliwia wdrożenie zawartości przy użyciu funkcji kudu zipdeploy i wardeploy.</span><span class="sxs-lookup"><span data-stu-id="5d007-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="5d007-112">Zapoznaj się z kudu wiki, aby uzyskać szczegółowe informacje na temat działania zipdeploy i wardeploy oraz jak poprawnie spakować aplikację sieci Web do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5d007-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="5d007-113"> https://aka.ms/kuduzipdeploy i https://aka.ms/kuduwardeploy zawierające pomocne informacje na temat zipdeploy i wardeploy.</span><span class="sxs-lookup"><span data-stu-id="5d007-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="5d007-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d007-114">EXAMPLES</span></span>

### <span data-ttu-id="5d007-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5d007-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="5d007-116">Umożliwia przekazywanie zawartości app.zip do aplikacji sieci Web o nazwie MojaApl należącej do grupy zasobów Default — w sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5d007-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="5d007-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5d007-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="5d007-118">Umożliwia przekazywanie zawartości javaproject. War do miejsca przemieszczania aplikacji sieci Web o nazwie ContosoApp należącej do ContosoRG grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d007-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="5d007-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="5d007-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="5d007-120">Umożliwia przekazywanie zawartości app.zip do aplikacji sieci Web o nazwie ContosoApp należącej do ContosoRG grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d007-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="5d007-121">Polecenie cmdlet zostanie uruchomione w tle zadania.</span><span class="sxs-lookup"><span data-stu-id="5d007-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="5d007-122">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="5d007-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```

<span data-ttu-id="5d007-123">Umożliwia przekazywanie zawartości java_app. jar do aplikacji sieci Web o nazwie ContosoApp należącej do ContosoRG grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d007-123">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="5d007-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d007-124">PARAMETERS</span></span>

### <span data-ttu-id="5d007-125">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="5d007-125">-ArchivePath</span></span>
<span data-ttu-id="5d007-126">Ścieżka pliku archiwum.</span><span class="sxs-lookup"><span data-stu-id="5d007-126">The path of the archive file.</span></span> <span data-ttu-id="5d007-127">Obsługa ZIP, wojny i JAR.</span><span class="sxs-lookup"><span data-stu-id="5d007-127">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="5d007-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d007-128">-AsJob</span></span>
<span data-ttu-id="5d007-129">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5d007-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d007-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d007-130">-DefaultProfile</span></span>
<span data-ttu-id="5d007-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5d007-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d007-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5d007-132">-Name</span></span>
<span data-ttu-id="5d007-133">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5d007-133">The name of the web app.</span></span>

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

### <span data-ttu-id="5d007-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d007-134">-ResourceGroupName</span></span>
<span data-ttu-id="5d007-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5d007-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="5d007-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="5d007-136">-Slot</span></span>
<span data-ttu-id="5d007-137">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5d007-137">The name of the web app slot.</span></span>

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

### <span data-ttu-id="5d007-138">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="5d007-138">-WebApp</span></span>
<span data-ttu-id="5d007-139">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="5d007-139">The web app object</span></span>

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

### <span data-ttu-id="5d007-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d007-140">CommonParameters</span></span>
<span data-ttu-id="5d007-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d007-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d007-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d007-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d007-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d007-143">INPUTS</span></span>

### <span data-ttu-id="5d007-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5d007-144">System.String</span></span>

### <span data-ttu-id="5d007-145">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="5d007-145">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5d007-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d007-146">OUTPUTS</span></span>

### <span data-ttu-id="5d007-147">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="5d007-147">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5d007-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d007-148">NOTES</span></span>

## <span data-ttu-id="5d007-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d007-149">RELATED LINKS</span></span>
