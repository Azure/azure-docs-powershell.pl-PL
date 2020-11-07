---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D6D4E733-31AE-4ABE-8C78-583EC48C56B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: 03aca295edc9a0c7d1a2b2bde7a78419158209dc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897522"
---
# <span data-ttu-id="63db1-101">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="63db1-101">New-AzureRmWebApp</span></span>

## <span data-ttu-id="63db1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63db1-102">SYNOPSIS</span></span>
<span data-ttu-id="63db1-103">Tworzy aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="63db1-103">Creates an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63db1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63db1-104">SYNTAX</span></span>

### <span data-ttu-id="63db1-105">SimpleParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="63db1-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmWebApp [[-ResourceGroupName] <String>] [-Name] <String> [[-Location] <String>]
 [[-AppServicePlan] <String>] [-AsJob] [-GitRepositoryPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63db1-106">WebAppParameterSet</span><span class="sxs-lookup"><span data-stu-id="63db1-106">WebAppParameterSet</span></span>
```
New-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-AppServicePlan] <String>] [-SourceWebApp] <Site> [[-TrafficManagerProfile] <String>] [-IgnoreSourceControl]
 [-IgnoreCustomHostNames] [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>]
 [[-AseResourceGroupName] <String>] [-IncludeSourceWebAppSlots] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63db1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="63db1-107">DESCRIPTION</span></span>
<span data-ttu-id="63db1-108">Polecenie cmdlet **New-AzureRmWebApp** umożliwia utworzenie aplikacji sieci Web platformy Azure w danej grupie zasobów korzystającej z określonego planu usługi App Service i centrum danych.</span><span class="sxs-lookup"><span data-stu-id="63db1-108">The **New-AzureRmWebApp** cmdlet creates an Azure Web App in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="63db1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63db1-109">EXAMPLES</span></span>

### <span data-ttu-id="63db1-110">Przykład 1: Tworzenie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="63db1-110">Example 1: Create a Web App</span></span>
```
PS C:\>New-AzureRmWebApp -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -Location "West US" -AppServicePlan "ContosoServicePlan"
```

<span data-ttu-id="63db1-111">To polecenie tworzy aplikację Azure Web App o nazwie ContosoSite w istniejącej grupie zasobów o nazwie Default-Web-Zachodnia w centrum danych w Stanach Zjednoczonych na zachód.</span><span class="sxs-lookup"><span data-stu-id="63db1-111">This command creates an Azure Web App named ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="63db1-112">W poleceniu użyto istniejącego planu usługi App Service o nazwie ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="63db1-112">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="63db1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63db1-113">PARAMETERS</span></span>

### <span data-ttu-id="63db1-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="63db1-114">-AppServicePlan</span></span>
<span data-ttu-id="63db1-115">Nazwa planu usługi App Service</span><span class="sxs-lookup"><span data-stu-id="63db1-115">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63db1-116">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="63db1-116">-AppSettingsOverrides</span></span>
<span data-ttu-id="63db1-117">Ustawienia aplikacji zastępuje obiekt HashTable</span><span class="sxs-lookup"><span data-stu-id="63db1-117">App Settings Overrides HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63db1-118">-AseName</span><span class="sxs-lookup"><span data-stu-id="63db1-118">-AseName</span></span>
<span data-ttu-id="63db1-119">Nazwa środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="63db1-119">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63db1-120">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63db1-120">-AseResourceGroupName</span></span>
<span data-ttu-id="63db1-121">Nazwa grupy zasobów środowiska App Service Environment</span><span class="sxs-lookup"><span data-stu-id="63db1-121">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63db1-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63db1-122">-AsJob</span></span>
<span data-ttu-id="63db1-123">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="63db1-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63db1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63db1-124">-DefaultProfile</span></span>
<span data-ttu-id="63db1-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63db1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63db1-126">-GitRepositoryPath</span><span class="sxs-lookup"><span data-stu-id="63db1-126">-GitRepositoryPath</span></span>
<span data-ttu-id="63db1-127">Ścieżka do repozytorium GitHub containign aplikacji sieci Web do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="63db1-127">Path to the GitHub repository containign the web application to deploy.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63db1-128">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="63db1-128">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="63db1-129">Ignorowanie opcji niestandardowych nazw hostów</span><span class="sxs-lookup"><span data-stu-id="63db1-129">Ignore Custom Host Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63db1-130">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="63db1-130">-IgnoreSourceControl</span></span>
<span data-ttu-id="63db1-131">Opcja Ignoruj kontrolę źródła</span><span class="sxs-lookup"><span data-stu-id="63db1-131">Ignore Source Control Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63db1-132">-IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="63db1-132">-IncludeSourceWebAppSlots</span></span>
<span data-ttu-id="63db1-133">Uwzględnij źródłowe gniazda aplikacji</span><span class="sxs-lookup"><span data-stu-id="63db1-133">Include Source WebApp Slots Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebAppParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63db1-134">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="63db1-134">-Location</span></span>
<span data-ttu-id="63db1-135">Pozycję</span><span class="sxs-lookup"><span data-stu-id="63db1-135">Location</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63db1-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="63db1-136">-Name</span></span>
<span data-ttu-id="63db1-137">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="63db1-137">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebAppName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63db1-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63db1-138">-ResourceGroupName</span></span>
<span data-ttu-id="63db1-139">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="63db1-139">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63db1-140">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="63db1-140">-SourceWebApp</span></span>
<span data-ttu-id="63db1-141">Źródłowy obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="63db1-141">Source WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: WebAppParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63db1-142">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="63db1-142">-TrafficManagerProfile</span></span>
<span data-ttu-id="63db1-143">Identyfikator zasobu istniejącego profilu Menedżera ruchu</span><span class="sxs-lookup"><span data-stu-id="63db1-143">Resource Id of existing traffic manager profile</span></span>

```yaml
Type: String
Parameter Sets: WebAppParameterSet
Aliases: TrafficManagerProfileName, TrafficManagerProfileId

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63db1-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="63db1-144">-Confirm</span></span>
<span data-ttu-id="63db1-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63db1-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63db1-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63db1-146">-WhatIf</span></span>
<span data-ttu-id="63db1-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63db1-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63db1-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="63db1-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63db1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63db1-149">CommonParameters</span></span>
<span data-ttu-id="63db1-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63db1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63db1-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63db1-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63db1-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63db1-152">INPUTS</span></span>

### <span data-ttu-id="63db1-153">Klienta</span><span class="sxs-lookup"><span data-stu-id="63db1-153">Site</span></span>
<span data-ttu-id="63db1-154">Parametr "SourceWebApp" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="63db1-154">Parameter 'SourceWebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="63db1-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63db1-155">OUTPUTS</span></span>

### <span data-ttu-id="63db1-156">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="63db1-156">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="63db1-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63db1-157">NOTES</span></span>

## <span data-ttu-id="63db1-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63db1-158">RELATED LINKS</span></span>

[<span data-ttu-id="63db1-159">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="63db1-159">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="63db1-160">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="63db1-160">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="63db1-161">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="63db1-161">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="63db1-162">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="63db1-162">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="63db1-163">Zatrzymaj — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="63db1-163">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


