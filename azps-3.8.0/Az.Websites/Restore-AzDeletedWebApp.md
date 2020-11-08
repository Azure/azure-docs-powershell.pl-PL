---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: a67fec3246d52122554f256dfeb4d0349e869573
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051881"
---
# <span data-ttu-id="5fba5-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="5fba5-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="5fba5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5fba5-102">SYNOPSIS</span></span>
<span data-ttu-id="5fba5-103">Przywraca usuniętą aplikację internetową do nowej lub istniejącej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5fba5-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="5fba5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5fba5-104">SYNTAX</span></span>

### <span data-ttu-id="5fba5-105">FromDeletedResourceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5fba5-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fba5-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="5fba5-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fba5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5fba5-107">DESCRIPTION</span></span>
<span data-ttu-id="5fba5-108">Polecenie cmdlet **Restore-AzDeletedWebApp** powoduje przywrócenie usuniętej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5fba5-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="5fba5-109">Aplikacja sieci Web określona przez TargetResourceGroupName, TargetName i TargetSlot zostanie zastąpiona zawartością i ustawieniami usuniętej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5fba5-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="5fba5-110">Jeśli parametry docelowe nie zostaną określone, zostaną automatycznie wypełnione w grupie zasobów, nazwie i gnieździe usuniętej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="5fba5-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="5fba5-111">Jeśli docelowa aplikacja sieci Web nie istnieje, zostanie automatycznie utworzona w planie usługi App Service określonym przez TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="5fba5-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="5fba5-112">Parametr przełącznika RestoreContentOnly można użyć w celu przywrócenia tylko plików usuniętej aplikacji bez ustawień aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5fba5-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="5fba5-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5fba5-113">EXAMPLES</span></span>

### <span data-ttu-id="5fba5-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5fba5-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="5fba5-115">Przywraca usuniętą aplikację o nazwie ContosoApp należącą do grupy zasobów Default — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="5fba5-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="5fba5-116">W planie usługi App Service o nazwie ContosoPlan zostanie utworzona nowa aplikacja z tą samą nazwą i grupą, a pliki i ustawienia aplikacji usunięte zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="5fba5-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="5fba5-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5fba5-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="5fba5-118">Przywraca miejsce przemieszczania usuniętej aplikacji o nazwie ContosoApp należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="5fba5-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="5fba5-119">Aplikacja sieci Web o nazwie ContosoRestore należąca do grupy zasobów domyślne — sieć Web-wschód zostanie zastąpiona.</span><span class="sxs-lookup"><span data-stu-id="5fba5-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="5fba5-120">Usunięte ustawienia aplikacji sieci Web nie zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="5fba5-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="5fba5-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5fba5-121">PARAMETERS</span></span>

### <span data-ttu-id="5fba5-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fba5-122">-AsJob</span></span>
<span data-ttu-id="5fba5-123">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5fba5-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5fba5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fba5-124">-DefaultProfile</span></span>
<span data-ttu-id="5fba5-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5fba5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fba5-126">-Force</span><span class="sxs-lookup"><span data-stu-id="5fba5-126">-Force</span></span>
<span data-ttu-id="5fba5-127">Wykonaj przywracanie bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5fba5-127">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5fba5-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5fba5-128">-InputObject</span></span>
<span data-ttu-id="5fba5-129">Usunięta aplikacja Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5fba5-129">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="5fba5-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5fba5-130">-Location</span></span>
<span data-ttu-id="5fba5-131">Lokalizacja usuniętej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5fba5-131">The location of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="5fba5-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5fba5-132">-Name</span></span>
<span data-ttu-id="5fba5-133">Nazwa usuniętej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5fba5-133">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="5fba5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fba5-134">-ResourceGroupName</span></span>
<span data-ttu-id="5fba5-135">Grupa zasobów usuniętej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5fba5-135">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="5fba5-136">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="5fba5-136">-RestoreContentOnly</span></span>
<span data-ttu-id="5fba5-137">Przywróć pliki aplikacji sieci Web, ale nie przywracaj ustawień.</span><span class="sxs-lookup"><span data-stu-id="5fba5-137">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="5fba5-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="5fba5-138">-Slot</span></span>
<span data-ttu-id="5fba5-139">Usunięte gniazdo aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5fba5-139">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="5fba5-140">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="5fba5-140">-TargetAppServicePlanName</span></span>
<span data-ttu-id="5fba5-141">Plan usługi App Service dla nowej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5fba5-141">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="5fba5-142">-TargetName</span><span class="sxs-lookup"><span data-stu-id="5fba5-142">-TargetName</span></span>
<span data-ttu-id="5fba5-143">Nazwa nowej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5fba5-143">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="5fba5-144">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fba5-144">-TargetResourceGroupName</span></span>
<span data-ttu-id="5fba5-145">Grupa zasobów zawierająca nową aplikację sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5fba5-145">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="5fba5-146">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="5fba5-146">-TargetSlot</span></span>
<span data-ttu-id="5fba5-147">Nazwa nowego miejsca w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5fba5-147">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="5fba5-148">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="5fba5-148">-UseDisasterRecovery</span></span>
<span data-ttu-id="5fba5-149">Służy do odzyskiwania usuniętej aplikacji z jednostki skali, która jest w trybie offline.</span><span class="sxs-lookup"><span data-stu-id="5fba5-149">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="5fba5-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5fba5-150">-Confirm</span></span>
<span data-ttu-id="5fba5-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fba5-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fba5-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fba5-152">-WhatIf</span></span>
<span data-ttu-id="5fba5-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fba5-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5fba5-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5fba5-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fba5-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fba5-155">CommonParameters</span></span>
<span data-ttu-id="5fba5-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fba5-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fba5-157">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fba5-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fba5-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fba5-158">INPUTS</span></span>

### <span data-ttu-id="5fba5-159">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="5fba5-159">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="5fba5-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5fba5-160">OUTPUTS</span></span>

### <span data-ttu-id="5fba5-161">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="5fba5-161">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5fba5-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5fba5-162">NOTES</span></span>

## <span data-ttu-id="5fba5-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5fba5-163">RELATED LINKS</span></span>

[<span data-ttu-id="5fba5-164">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="5fba5-164">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)