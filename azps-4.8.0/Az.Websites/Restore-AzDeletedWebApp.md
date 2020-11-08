---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: 7cffc754e2662216aef10f163601e5d5a5339663
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221404"
---
# <span data-ttu-id="c9744-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c9744-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="c9744-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9744-102">SYNOPSIS</span></span>
<span data-ttu-id="c9744-103">Przywraca usuniętą aplikację internetową do nowej lub istniejącej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c9744-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="c9744-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9744-104">SYNTAX</span></span>

### <span data-ttu-id="c9744-105">FromDeletedResourceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c9744-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-DeletedId <String>] [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9744-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="c9744-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-DeletedId <String>] [-TargetName <String>] 
 [-TargetSlot <String>] [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> 
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9744-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c9744-107">DESCRIPTION</span></span>
<span data-ttu-id="c9744-108">Polecenie cmdlet **Restore-AzDeletedWebApp** powoduje przywrócenie usuniętej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c9744-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="c9744-109">Aplikacja sieci Web określona przez TargetResourceGroupName, TargetName i TargetSlot zostanie zastąpiona zawartością i ustawieniami usuniętej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c9744-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="c9744-110">Jeśli parametry docelowe nie zostaną określone, zostaną automatycznie wypełnione w grupie zasobów, nazwie i gnieździe usuniętej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="c9744-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="c9744-111">Jeśli docelowa aplikacja sieci Web nie istnieje, zostanie automatycznie utworzona w planie usługi App Service określonym przez TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="c9744-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="c9744-112">Parametr przełącznika RestoreContentOnly można użyć w celu przywrócenia tylko plików usuniętej aplikacji bez ustawień aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c9744-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="c9744-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9744-113">EXAMPLES</span></span>

### <span data-ttu-id="c9744-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c9744-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="c9744-115">Przywraca usuniętą aplikację o nazwie ContosoApp należącą do grupy zasobów Default — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="c9744-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="c9744-116">W planie usługi App Service o nazwie ContosoPlan zostanie utworzona nowa aplikacja z tą samą nazwą i grupą, a pliki i ustawienia aplikacji usunięte zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="c9744-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="c9744-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c9744-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="c9744-118">Przywraca miejsce przemieszczania usuniętej aplikacji o nazwie ContosoApp należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="c9744-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="c9744-119">Aplikacja sieci Web o nazwie ContosoRestore należąca do grupy zasobów domyślne — sieć Web-wschód zostanie zastąpiona.</span><span class="sxs-lookup"><span data-stu-id="c9744-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="c9744-120">Usunięte ustawienia aplikacji sieci Web nie zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="c9744-120">The deleted web app settings will not be restored.</span></span>

###<span data-ttu-id="c9744-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c9744-121">Example 3</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -DeletedId /subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Web/locations/location/deletedSites/1234 -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="c9744-122">Na wypadek 2 aplikacje usunięte z tą samą nazwą (ContosoApp) są dostępne szczegółowe informacje dotyczące witryn i przywracania aplikacji o nazwie ContosoRestore przy użyciu naszej opcji przez wywołanie funkcji Przywróć z identyfikatorem.</span><span class="sxs-lookup"><span data-stu-id="c9744-122">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with Id.</span></span>

###<span data-ttu-id="c9744-123">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="c9744-123">Example 4</span></span>
```powershell
PS C:\> $deletedSite = Get-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp
PS C:\> Restore-AzDeletedWebApp -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -TargetAppServicePlanName ContosoPlan -InputObject $deletedSite[0]
```

<span data-ttu-id="c9744-124">Jeśli na liście znajdują się 2 usunięte aplikacje o tej samej nazwie (ContosoApp), w celu uzyskania szczegółowych informacji na temat witryn i przywrócenia aplikacji o nazwie ContosoRestore za pomocą tej opcji możesz zadzwonić przez wywołanie funkcji Przywróć z danymi wejściowymi (Deletedsite)</span><span class="sxs-lookup"><span data-stu-id="c9744-124">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with InputObject(Deletedsite) details</span></span> 

## <span data-ttu-id="c9744-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9744-125">PARAMETERS</span></span>

### <span data-ttu-id="c9744-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9744-126">-AsJob</span></span>
<span data-ttu-id="c9744-127">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c9744-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9744-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9744-128">-DefaultProfile</span></span>
<span data-ttu-id="c9744-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9744-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9744-130">-DeletedId</span><span class="sxs-lookup"><span data-stu-id="c9744-130">-DeletedId</span></span>
<span data-ttu-id="c9744-131">Identyfikator usuniętej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c9744-131">The Id of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9744-132">-Force</span><span class="sxs-lookup"><span data-stu-id="c9744-132">-Force</span></span>
<span data-ttu-id="c9744-133">Wykonaj przywracanie bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c9744-133">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c9744-134">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c9744-134">-InputObject</span></span>
<span data-ttu-id="c9744-135">Usunięta aplikacja Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c9744-135">The deleted Azure Web App.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9744-136">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c9744-136">-Location</span></span>
<span data-ttu-id="c9744-137">Lokalizacja usuniętej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c9744-137">The location of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9744-138">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c9744-138">-Name</span></span>
<span data-ttu-id="c9744-139">Nazwa usuniętej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c9744-139">The name of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9744-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9744-140">-ResourceGroupName</span></span>
<span data-ttu-id="c9744-141">Grupa zasobów usuniętej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c9744-141">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9744-142">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="c9744-142">-RestoreContentOnly</span></span>
<span data-ttu-id="c9744-143">Przywróć pliki aplikacji sieci Web, ale nie przywracaj ustawień.</span><span class="sxs-lookup"><span data-stu-id="c9744-143">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="c9744-144">-Slot</span><span class="sxs-lookup"><span data-stu-id="c9744-144">-Slot</span></span>
<span data-ttu-id="c9744-145">Usunięte gniazdo aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c9744-145">The deleted Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9744-146">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="c9744-146">-TargetAppServicePlanName</span></span>
<span data-ttu-id="c9744-147">Plan usługi App Service dla nowej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c9744-147">The App Service Plan for the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9744-148">-TargetName</span><span class="sxs-lookup"><span data-stu-id="c9744-148">-TargetName</span></span>
<span data-ttu-id="c9744-149">Nazwa nowej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c9744-149">The name of the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9744-150">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9744-150">-TargetResourceGroupName</span></span>
<span data-ttu-id="c9744-151">Grupa zasobów zawierająca nową aplikację sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c9744-151">The resource group containing the new Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9744-152">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="c9744-152">-TargetSlot</span></span>
<span data-ttu-id="c9744-153">Nazwa nowego miejsca w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c9744-153">The name of the new Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9744-154">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="c9744-154">-UseDisasterRecovery</span></span>
<span data-ttu-id="c9744-155">Służy do odzyskiwania usuniętej aplikacji z jednostki skali, która jest w trybie offline.</span><span class="sxs-lookup"><span data-stu-id="c9744-155">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="c9744-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9744-156">-Confirm</span></span>
<span data-ttu-id="c9744-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9744-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9744-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9744-158">-WhatIf</span></span>
<span data-ttu-id="c9744-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9744-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9744-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9744-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9744-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9744-161">CommonParameters</span></span>
<span data-ttu-id="c9744-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9744-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9744-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9744-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9744-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9744-164">INPUTS</span></span>

### <span data-ttu-id="c9744-165">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c9744-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="c9744-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9744-166">OUTPUTS</span></span>

### <span data-ttu-id="c9744-167">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="c9744-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c9744-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9744-168">NOTES</span></span>

## <span data-ttu-id="c9744-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9744-169">RELATED LINKS</span></span>

[<span data-ttu-id="c9744-170">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c9744-170">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)