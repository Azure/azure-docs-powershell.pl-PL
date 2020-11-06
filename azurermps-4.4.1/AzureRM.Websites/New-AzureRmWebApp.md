---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebApp.md
ms.openlocfilehash: 4948de891815345efdc0b3f4ec39fb1874e510b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553736"
---
# <span data-ttu-id="21ecf-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="21ecf-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="21ecf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="21ecf-103">Tworzy aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="21ecf-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21ecf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21ecf-104">SYNTAX</span></span>

### <span data-ttu-id="21ecf-105">S1 (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="21ecf-105">S1 (Default)</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileId] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21ecf-106">S2</span><span class="sxs-lookup"><span data-stu-id="21ecf-106">S2</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [[-TrafficManagerProfileName] <String>]
 [-IgnoreSourceControl] [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21ecf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="21ecf-107">DESCRIPTION</span></span>
<span data-ttu-id="21ecf-108">Polecenie cmdlet **New-AzureRmWebApp** umożliwia utworzenie aplikacji sieci Web platformy Azure w danej grupie zasobów korzystającej z określonego planu usługi App Service i centrum danych.</span><span class="sxs-lookup"><span data-stu-id="21ecf-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="21ecf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21ecf-109">EXAMPLES</span></span>

### <span data-ttu-id="21ecf-110">Przykład 1: Tworzenie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="21ecf-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="21ecf-111">To polecenie tworzy aplikację Azure Web App o nazwie ContosoSite w istniejącej grupie zasobów o nazwie Default-Web-Zachodnia w centrum danych w Stanach Zjednoczonych na zachód.</span><span class="sxs-lookup"><span data-stu-id="21ecf-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="21ecf-112">W poleceniu użyto istniejącego planu usługi App Service o nazwie ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="21ecf-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="21ecf-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21ecf-113">PARAMETERS</span></span>

### <span data-ttu-id="21ecf-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="21ecf-114">-AppServicePlan</span></span>
<span data-ttu-id="21ecf-115">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="21ecf-115">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ecf-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="21ecf-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="21ecf-117">Ustawienia aplikacji zastępuje obiekt HashTable</span><span class="sxs-lookup"><span data-stu-id="21ecf-117">App Settings Overrides HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ecf-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="21ecf-118">-AseName</span></span>
<span data-ttu-id="21ecf-119">Nazwa środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="21ecf-119">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ecf-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21ecf-120">-AseResourceGroupName</span></span>
<span data-ttu-id="21ecf-121">Nazwa grupy zasobów środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="21ecf-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ecf-122">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="21ecf-122">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="21ecf-123">Ignorowanie opcji niestandardowych nazw hostów</span><span class="sxs-lookup"><span data-stu-id="21ecf-123">Ignore Custom Host Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ecf-124">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="21ecf-124">-IgnoreSourceControl</span></span>
<span data-ttu-id="21ecf-125">Opcja Ignoruj kontrolę źródła</span><span class="sxs-lookup"><span data-stu-id="21ecf-125">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ecf-126">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="21ecf-126">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="21ecf-127">Uwzględnij źródłowe gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="21ecf-127">Include Source WebApp Slots Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ecf-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="21ecf-128">-Location</span></span>
<span data-ttu-id="21ecf-129">Pozycję</span><span class="sxs-lookup"><span data-stu-id="21ecf-129">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ecf-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21ecf-130">-Name</span></span>
<span data-ttu-id="21ecf-131">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="21ecf-131">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ecf-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21ecf-132">-ResourceGroupName</span></span>
<span data-ttu-id="21ecf-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="21ecf-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ecf-134">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="21ecf-134">-SourceWebApp</span></span>
<span data-ttu-id="21ecf-135">Źródłowy obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="21ecf-135">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21ecf-136">-TrafficManagerProfileId</span><span class="sxs-lookup"><span data-stu-id="21ecf-136">-TrafficManagerProfileId</span></span>
<span data-ttu-id="21ecf-137">Identyfikator profilu w usłudze Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="21ecf-137">Traffic Manager Profile Id</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ecf-138">-TrafficManagerProfileName</span><span class="sxs-lookup"><span data-stu-id="21ecf-138">-TrafficManagerProfileName</span></span>
<span data-ttu-id="21ecf-139">Nazwa profilu w usłudze Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="21ecf-139">Traffic Manager Profile Name</span></span>

```yaml
Type: System.String
Parameter Sets: S2
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ecf-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21ecf-140">-DefaultProfile</span></span>
<span data-ttu-id="21ecf-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21ecf-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ecf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ecf-142">CommonParameters</span></span>
<span data-ttu-id="21ecf-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21ecf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ecf-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21ecf-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ecf-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21ecf-145">INPUTS</span></span>

### <span data-ttu-id="21ecf-146">Klienta</span><span class="sxs-lookup"><span data-stu-id="21ecf-146">Site</span></span>
<span data-ttu-id="21ecf-147">Parametr "SourceWebApp" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="21ecf-147">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="21ecf-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21ecf-148">OUTPUTS</span></span>

## <span data-ttu-id="21ecf-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21ecf-149">NOTES</span></span>

## <span data-ttu-id="21ecf-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21ecf-150">RELATED LINKS</span></span>

[<span data-ttu-id="21ecf-151">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="21ecf-151">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="21ecf-152">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="21ecf-152">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="21ecf-153">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="21ecf-153">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="21ecf-154">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="21ecf-154">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="21ecf-155">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="21ecf-155">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


