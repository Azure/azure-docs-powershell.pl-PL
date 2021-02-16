---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: 7cffc754e2662216aef10f163601e5d5a5339663
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195459"
---
# <span data-ttu-id="1497c-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1497c-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="1497c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1497c-102">SYNOPSIS</span></span>
<span data-ttu-id="1497c-103">Przywraca usuniętą aplikację sieci Web do nowej lub istniejącej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1497c-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="1497c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1497c-104">SYNTAX</span></span>

### <span data-ttu-id="1497c-105">FromDeletedResourceName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="1497c-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-DeletedId <String>] [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1497c-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="1497c-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-DeletedId <String>] [-TargetName <String>] 
 [-TargetSlot <String>] [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> 
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1497c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1497c-107">DESCRIPTION</span></span>
<span data-ttu-id="1497c-108">Polecenie **cmdlet Restore-AzDeletedWebApp** przywraca usuniętą aplikację sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1497c-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="1497c-109">Aplikacja sieci Web określona przez targetResourceGroupName, TargetName i TargetSlot zostanie zastąpiona zawartością i ustawieniami usuniętej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1497c-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="1497c-110">Jeśli parametry docelowe nie zostaną określone, zostaną one automatycznie wypełnione grupą zasobów, nazwą i slotem usuniętej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="1497c-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="1497c-111">Jeśli docelowa aplikacja sieci Web nie istnieje, zostanie automatycznie utworzona w planie usługi aplikacji określonym przez parametr TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="1497c-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="1497c-112">Parametr RestoreContentOnly switch może być używany do przywracania tylko plików usuniętych aplikacji bez ustawień aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1497c-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="1497c-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1497c-113">EXAMPLES</span></span>

### <span data-ttu-id="1497c-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1497c-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="1497c-115">Przywraca usuniętą aplikację o nazwie ContosoApp należącą do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="1497c-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="1497c-116">W planie usług aplikacji o nazwie ContosoPlan zostanie utworzona nowa aplikacja o tej samej nazwie i grupie zasobów, a pliki i ustawienia usuniętej aplikacji zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="1497c-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="1497c-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1497c-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="1497c-118">Przywraca miejsce tymczasowe usuniętej aplikacji o nazwie ContosoApp należącej do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="1497c-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="1497c-119">Aplikacja sieci Web o nazwie ContosoRestore należąca do grupy zasobów Default-Web-EastUS zostanie zastąpiona.</span><span class="sxs-lookup"><span data-stu-id="1497c-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="1497c-120">Usunięte ustawienia aplikacji sieci Web nie zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="1497c-120">The deleted web app settings will not be restored.</span></span>

###<span data-ttu-id="1497c-121">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="1497c-121">Example 3</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -DeletedId /subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Web/locations/location/deletedSites/1234 -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="1497c-122">Jeśli istnieją 2 usunięte aplikacje o tej samej nazwie (ContosoApp), wówczas otrzymamy szczegółowe informacje dotyczące obu witryn i przywrócimy aplikację o nazwie ContosoRestore z wybranej przez nas aplikacji, wywołując przywracanie za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="1497c-122">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with Id.</span></span>

###<span data-ttu-id="1497c-123">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="1497c-123">Example 4</span></span>
```powershell
PS C:\> $deletedSite = Get-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp
PS C:\> Restore-AzDeletedWebApp -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -TargetAppServicePlanName ContosoPlan -InputObject $deletedSite[0]
```

<span data-ttu-id="1497c-124">Jeśli istnieją 2 usunięte aplikacje o takiej samej nazwie (ContosoApp), wówczas pozyskamy szczegóły dotyczące obu witryn i przywrócimy aplikację o nazwie ContosoRestore z wybranej przez nas aplikacji, wywołując przywracanie za pomocą szczegółów InputObject(Deletedsite)</span><span class="sxs-lookup"><span data-stu-id="1497c-124">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with InputObject(Deletedsite) details</span></span> 

## <span data-ttu-id="1497c-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1497c-125">PARAMETERS</span></span>

### <span data-ttu-id="1497c-126">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1497c-126">-AsJob</span></span>
<span data-ttu-id="1497c-127">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1497c-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1497c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1497c-128">-DefaultProfile</span></span>
<span data-ttu-id="1497c-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1497c-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1497c-130">-DeletedId</span><span class="sxs-lookup"><span data-stu-id="1497c-130">-DeletedId</span></span>
<span data-ttu-id="1497c-131">Identyfikator usuniętej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1497c-131">The Id of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1497c-132">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="1497c-132">-Force</span></span>
<span data-ttu-id="1497c-133">Wykonaj przywracanie bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1497c-133">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1497c-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1497c-134">-InputObject</span></span>
<span data-ttu-id="1497c-135">Usunięta aplikacja Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1497c-135">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1497c-136">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1497c-136">-Location</span></span>
<span data-ttu-id="1497c-137">Lokalizacja usuniętej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1497c-137">The location of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1497c-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1497c-138">-Name</span></span>
<span data-ttu-id="1497c-139">Nazwa usuniętej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1497c-139">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1497c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1497c-140">-ResourceGroupName</span></span>
<span data-ttu-id="1497c-141">Grupa zasobów usuniętej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1497c-141">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1497c-142">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="1497c-142">-RestoreContentOnly</span></span>
<span data-ttu-id="1497c-143">Przywróć pliki aplikacji sieci Web, ale nie przywracaj ustawień.</span><span class="sxs-lookup"><span data-stu-id="1497c-143">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="1497c-144">— Slot</span><span class="sxs-lookup"><span data-stu-id="1497c-144">-Slot</span></span>
<span data-ttu-id="1497c-145">Usunięto miejsce na aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1497c-145">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="1497c-146">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="1497c-146">-TargetAppServicePlanName</span></span>
<span data-ttu-id="1497c-147">Plan usługi aplikacji dla nowej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1497c-147">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="1497c-148">-TargetName</span><span class="sxs-lookup"><span data-stu-id="1497c-148">-TargetName</span></span>
<span data-ttu-id="1497c-149">Nazwa nowej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1497c-149">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="1497c-150">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1497c-150">-TargetResourceGroupName</span></span>
<span data-ttu-id="1497c-151">Grupa zasobów zawierająca nową aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1497c-151">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="1497c-152">- TargetSlot</span><span class="sxs-lookup"><span data-stu-id="1497c-152">-TargetSlot</span></span>
<span data-ttu-id="1497c-153">Nazwa nowego miejsca aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1497c-153">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="1497c-154">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="1497c-154">-UseDisasterRecovery</span></span>
<span data-ttu-id="1497c-155">Umożliwia odzyskanie usuniętej aplikacji z jednostki skali, która jest w trybie offline.</span><span class="sxs-lookup"><span data-stu-id="1497c-155">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="1497c-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1497c-156">-Confirm</span></span>
<span data-ttu-id="1497c-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1497c-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1497c-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1497c-158">-WhatIf</span></span>
<span data-ttu-id="1497c-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1497c-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1497c-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1497c-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1497c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1497c-161">CommonParameters</span></span>
<span data-ttu-id="1497c-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1497c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1497c-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1497c-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1497c-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1497c-164">INPUTS</span></span>

### <span data-ttu-id="1497c-165">Microsoft.Azure.Commands.WebApps.Cmdlet.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1497c-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="1497c-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1497c-166">OUTPUTS</span></span>

### <span data-ttu-id="1497c-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="1497c-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1497c-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1497c-168">NOTES</span></span>

## <span data-ttu-id="1497c-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1497c-169">RELATED LINKS</span></span>

[<span data-ttu-id="1497c-170">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1497c-170">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)