---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: a90a56417ab8b1b08d72cb9d00ebe7411a6f075c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707270"
---
# <span data-ttu-id="320e8-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="320e8-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="320e8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="320e8-102">SYNOPSIS</span></span>
<span data-ttu-id="320e8-103">Przywraca usuniętą aplikację internetową do nowej lub istniejącej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="320e8-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="320e8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="320e8-104">SYNTAX</span></span>

### <span data-ttu-id="320e8-105">FromDeletedResourceName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="320e8-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="320e8-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="320e8-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="320e8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="320e8-107">DESCRIPTION</span></span>
<span data-ttu-id="320e8-108">Polecenie cmdlet **Restore-AzDeletedWebApp** powoduje przywrócenie usuniętej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="320e8-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="320e8-109">Aplikacja sieci Web określona przez TargetResourceGroupName, TargetName i TargetSlot zostanie zastąpiona zawartością i ustawieniami usuniętej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="320e8-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="320e8-110">Jeśli parametry docelowe nie zostaną określone, zostaną automatycznie wypełnione w grupie zasobów, nazwie i gnieździe usuniętej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="320e8-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="320e8-111">Jeśli docelowa aplikacja sieci Web nie istnieje, zostanie automatycznie utworzona w planie usługi App Service określonym przez TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="320e8-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="320e8-112">Parametr przełącznika RestoreContentOnly można użyć w celu przywrócenia tylko plików usuniętej aplikacji bez ustawień aplikacji.</span><span class="sxs-lookup"><span data-stu-id="320e8-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="320e8-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="320e8-113">EXAMPLES</span></span>

### <span data-ttu-id="320e8-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="320e8-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="320e8-115">Przywraca usuniętą aplikację o nazwie ContosoApp należącą do grupy zasobów Default — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="320e8-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="320e8-116">W planie usługi App Service o nazwie ContosoPlan zostanie utworzona nowa aplikacja z tą samą nazwą i grupą, a pliki i ustawienia aplikacji usunięte zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="320e8-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="320e8-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="320e8-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="320e8-118">Przywraca miejsce przemieszczania usuniętej aplikacji o nazwie ContosoApp należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="320e8-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="320e8-119">Aplikacja sieci Web o nazwie ContosoRestore należąca do grupy zasobów domyślne — sieć Web-wschód zostanie zastąpiona.</span><span class="sxs-lookup"><span data-stu-id="320e8-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="320e8-120">Usunięte ustawienia aplikacji sieci Web nie zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="320e8-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="320e8-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="320e8-121">PARAMETERS</span></span>

### <span data-ttu-id="320e8-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="320e8-122">-AsJob</span></span>
<span data-ttu-id="320e8-123">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="320e8-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="320e8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="320e8-124">-DefaultProfile</span></span>
<span data-ttu-id="320e8-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="320e8-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="320e8-126">-Force</span><span class="sxs-lookup"><span data-stu-id="320e8-126">-Force</span></span>
<span data-ttu-id="320e8-127">Wykonaj przywracanie bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="320e8-127">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="320e8-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="320e8-128">-InputObject</span></span>
<span data-ttu-id="320e8-129">Usunięta aplikacja Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="320e8-129">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="320e8-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="320e8-130">-Name</span></span>
<span data-ttu-id="320e8-131">Nazwa usuniętej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="320e8-131">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="320e8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="320e8-132">-ResourceGroupName</span></span>
<span data-ttu-id="320e8-133">Grupa zasobów usuniętej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="320e8-133">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="320e8-134">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="320e8-134">-RestoreContentOnly</span></span>
<span data-ttu-id="320e8-135">Przywróć pliki aplikacji sieci Web, ale nie przywracaj ustawień.</span><span class="sxs-lookup"><span data-stu-id="320e8-135">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="320e8-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="320e8-136">-Slot</span></span>
<span data-ttu-id="320e8-137">Usunięte gniazdo aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="320e8-137">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="320e8-138">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="320e8-138">-TargetAppServicePlanName</span></span>
<span data-ttu-id="320e8-139">Plan usługi App Service dla nowej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="320e8-139">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="320e8-140">-TargetName</span><span class="sxs-lookup"><span data-stu-id="320e8-140">-TargetName</span></span>
<span data-ttu-id="320e8-141">Nazwa nowej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="320e8-141">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="320e8-142">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="320e8-142">-TargetResourceGroupName</span></span>
<span data-ttu-id="320e8-143">Grupa zasobów zawierająca nową aplikację sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="320e8-143">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="320e8-144">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="320e8-144">-TargetSlot</span></span>
<span data-ttu-id="320e8-145">Nazwa nowego miejsca w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="320e8-145">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="320e8-146">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="320e8-146">-UseDisasterRecovery</span></span>
<span data-ttu-id="320e8-147">Służy do odzyskiwania usuniętej aplikacji z jednostki skali, która jest w trybie offline.</span><span class="sxs-lookup"><span data-stu-id="320e8-147">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="320e8-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="320e8-148">-Confirm</span></span>
<span data-ttu-id="320e8-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="320e8-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="320e8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="320e8-150">-WhatIf</span></span>
<span data-ttu-id="320e8-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="320e8-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="320e8-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="320e8-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="320e8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320e8-153">CommonParameters</span></span>
<span data-ttu-id="320e8-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="320e8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320e8-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="320e8-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320e8-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="320e8-156">INPUTS</span></span>

### <span data-ttu-id="320e8-157">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="320e8-157">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="320e8-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="320e8-158">OUTPUTS</span></span>

### <span data-ttu-id="320e8-159">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="320e8-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="320e8-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="320e8-160">NOTES</span></span>

## <span data-ttu-id="320e8-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="320e8-161">RELATED LINKS</span></span>

[<span data-ttu-id="320e8-162">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="320e8-162">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)