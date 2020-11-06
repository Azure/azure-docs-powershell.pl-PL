---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
ms.openlocfilehash: caebbe3c9b84b469e5fc357686b256aca59c2b61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546299"
---
# <span data-ttu-id="44633-101">Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="44633-101">Restore-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="44633-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="44633-102">SYNOPSIS</span></span>
<span data-ttu-id="44633-103">Przywraca usuniętą aplikację internetową do nowej lub istniejącej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="44633-103">Restores a deleted web app to a new or existing web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44633-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="44633-104">SYNTAX</span></span>

### <span data-ttu-id="44633-105">FromDeletedResourceName</span><span class="sxs-lookup"><span data-stu-id="44633-105">FromDeletedResourceName</span></span>
```
Restore-AzureRmDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44633-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="44633-106">FromDeletedApp</span></span>
```
Restore-AzureRmDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [<CommonParameters>]
```

## <span data-ttu-id="44633-107">Opis</span><span class="sxs-lookup"><span data-stu-id="44633-107">DESCRIPTION</span></span>
<span data-ttu-id="44633-108">Polecenie cmdlet **Restore-AzureRmDeletedWebApp** powoduje przywrócenie usuniętej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="44633-108">The **Restore-AzureRmDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="44633-109">Aplikacja sieci Web określona przez TargetResourceGroupName, TargetName i TargetSlot zostanie zastąpiona zawartością i ustawieniami usuniętej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="44633-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="44633-110">Jeśli parametry docelowe nie zostaną określone, zostaną automatycznie wypełnione w grupie zasobów, nazwie i gnieździe usuniętej aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="44633-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="44633-111">Jeśli docelowa aplikacja sieci Web nie istnieje, zostanie automatycznie utworzona w planie usługi App Service określonym przez TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="44633-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="44633-112">Parametr przełącznika RestoreContentOnly można użyć w celu przywrócenia tylko plików usuniętej aplikacji bez ustawień aplikacji.</span><span class="sxs-lookup"><span data-stu-id="44633-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="44633-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="44633-113">EXAMPLES</span></span>

### <span data-ttu-id="44633-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="44633-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="44633-115">Przywraca usuniętą aplikację o nazwie ContosoApp należącą do grupy zasobów Default — Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="44633-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="44633-116">W planie usługi App Service o nazwie ContosoPlan zostanie utworzona nowa aplikacja z tą samą nazwą i grupą, a pliki i ustawienia aplikacji usunięte zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="44633-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="44633-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="44633-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="44633-118">Przywraca miejsce przemieszczania usuniętej aplikacji o nazwie ContosoApp należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="44633-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="44633-119">Aplikacja sieci Web o nazwie ContosoRestore należąca do grupy zasobów domyślne — sieć Web-wschód zostanie zastąpiona.</span><span class="sxs-lookup"><span data-stu-id="44633-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="44633-120">Usunięte ustawienia aplikacji sieci Web nie zostaną przywrócone.</span><span class="sxs-lookup"><span data-stu-id="44633-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="44633-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44633-121">PARAMETERS</span></span>

### <span data-ttu-id="44633-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44633-122">-AsJob</span></span>
<span data-ttu-id="44633-123">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="44633-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44633-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44633-124">-DefaultProfile</span></span>
<span data-ttu-id="44633-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="44633-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44633-126">-Force</span><span class="sxs-lookup"><span data-stu-id="44633-126">-Force</span></span>
<span data-ttu-id="44633-127">Wykonaj przywracanie bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="44633-127">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="44633-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="44633-128">-InputObject</span></span>
<span data-ttu-id="44633-129">Usunięta aplikacja Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="44633-129">The deleted Azure Web App.</span></span>

```yaml
Type: PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44633-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="44633-130">-Name</span></span>
<span data-ttu-id="44633-131">Nazwa usuniętej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="44633-131">The name of the deleted Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44633-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44633-132">-ResourceGroupName</span></span>
<span data-ttu-id="44633-133">Grupa zasobów usuniętej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="44633-133">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44633-134">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="44633-134">-RestoreContentOnly</span></span>
<span data-ttu-id="44633-135">Przywróć pliki aplikacji sieci Web, ale nie przywracaj ustawień.</span><span class="sxs-lookup"><span data-stu-id="44633-135">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="44633-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="44633-136">-Slot</span></span>
<span data-ttu-id="44633-137">Usunięte gniazdo aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="44633-137">The deleted Azure Web App slot.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44633-138">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="44633-138">-TargetAppServicePlanName</span></span>
<span data-ttu-id="44633-139">Plan usługi App Service dla nowej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="44633-139">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="44633-140">-TargetName</span><span class="sxs-lookup"><span data-stu-id="44633-140">-TargetName</span></span>
<span data-ttu-id="44633-141">Nazwa nowej aplikacji sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="44633-141">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="44633-142">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44633-142">-TargetResourceGroupName</span></span>
<span data-ttu-id="44633-143">Grupa zasobów zawierająca nową aplikację sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="44633-143">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="44633-144">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="44633-144">-TargetSlot</span></span>
<span data-ttu-id="44633-145">Nazwa nowego miejsca w aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="44633-145">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="44633-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44633-146">CommonParameters</span></span>
<span data-ttu-id="44633-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44633-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="44633-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44633-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44633-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44633-149">INPUTS</span></span>

### <span data-ttu-id="44633-150">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="44633-150">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="44633-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="44633-151">OUTPUTS</span></span>

### <span data-ttu-id="44633-152">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="44633-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="44633-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="44633-153">NOTES</span></span>

## <span data-ttu-id="44633-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44633-154">RELATED LINKS</span></span>

[<span data-ttu-id="44633-155">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="44633-155">Get-AzureRmDeletedWebApp</span></span>](./Get-AzureRmDeletedWebApp.md)
