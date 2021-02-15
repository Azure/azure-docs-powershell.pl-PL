---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: 1dd84305753edc8ad639c160c9003c4c393d041e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182426"
---
# <span data-ttu-id="ae799-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="ae799-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="ae799-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae799-102">SYNOPSIS</span></span>
<span data-ttu-id="ae799-103">Pozwala przywrócić migawkę aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ae799-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="ae799-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae799-104">SYNTAX</span></span>

### <span data-ttu-id="ae799-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ae799-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae799-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ae799-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae799-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae799-107">DESCRIPTION</span></span>
<span data-ttu-id="ae799-108">Pozwala przywrócić migawkę aplikacji sieci Web do aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ae799-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="ae799-109">Przywracanie migawki powoduje zastąpienie wszystkich plików w aplikacji sieci Web plikami zawartymi w tej migawki.</span><span class="sxs-lookup"><span data-stu-id="ae799-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="ae799-110">Aby przywrócić także ustawienia, użyj parametru przełącznika RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ae799-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="ae799-111">Migawkę z jednej aplikacji sieci Web można przywrócić do dowolnej innej aplikacji sieci Web w ramach tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ae799-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="ae799-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae799-112">EXAMPLES</span></span>

### <span data-ttu-id="ae799-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae799-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="ae799-114">Pobiera najnowszą migawkę aplikacji sieci Web o nazwie "ContosoApp" z slotem o nazwie "Staging" w grupie zasobów "Default-Web-WestUS".</span><span class="sxs-lookup"><span data-stu-id="ae799-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="ae799-115">Przywraca migawkę do miejsca "Przywróć" aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ae799-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="ae799-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae799-116">PARAMETERS</span></span>

### <span data-ttu-id="ae799-117">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ae799-117">-AsJob</span></span>
<span data-ttu-id="ae799-118">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ae799-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae799-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae799-119">-DefaultProfile</span></span>
<span data-ttu-id="ae799-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae799-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae799-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ae799-121">-Force</span></span>
<span data-ttu-id="ae799-122">Umożliwia nadpisane pierwotnej aplikacji sieci Web bez wyświetlania ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="ae799-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae799-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae799-123">-InputObject</span></span>
<span data-ttu-id="ae799-124">Migawka aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ae799-124">The Azure Web App snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae799-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ae799-125">-Name</span></span>
<span data-ttu-id="ae799-126">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ae799-126">The name of the web app.</span></span>

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

### <span data-ttu-id="ae799-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae799-127">-RecoverConfiguration</span></span>
<span data-ttu-id="ae799-128">Odzyskiwanie konfiguracji aplikacji sieci Web oprócz plików.</span><span class="sxs-lookup"><span data-stu-id="ae799-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae799-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae799-129">-ResourceGroupName</span></span>
<span data-ttu-id="ae799-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae799-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="ae799-131">— Slot</span><span class="sxs-lookup"><span data-stu-id="ae799-131">-Slot</span></span>
<span data-ttu-id="ae799-132">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="ae799-132">The name of the web app slot.</span></span>

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

### <span data-ttu-id="ae799-133">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="ae799-133">-UseDisasterRecovery</span></span>
<span data-ttu-id="ae799-134">Użyj, aby odzyskać migawkę z jednostki skalowania, która jest w trybie offline.</span><span class="sxs-lookup"><span data-stu-id="ae799-134">Use to recover a snapshot from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="ae799-135">- WebApp</span><span class="sxs-lookup"><span data-stu-id="ae799-135">-WebApp</span></span>
<span data-ttu-id="ae799-136">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="ae799-136">The web app object</span></span>

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

### <span data-ttu-id="ae799-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae799-137">-Confirm</span></span>
<span data-ttu-id="ae799-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ae799-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae799-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae799-139">-WhatIf</span></span>
<span data-ttu-id="ae799-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae799-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae799-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ae799-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae799-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae799-142">CommonParameters</span></span>
<span data-ttu-id="ae799-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae799-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae799-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae799-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae799-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae799-145">INPUTS</span></span>

### <span data-ttu-id="ae799-146">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="ae799-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ae799-147">System.String</span><span class="sxs-lookup"><span data-stu-id="ae799-147">System.String</span></span>

### <span data-ttu-id="ae799-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ae799-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="ae799-149">Microsoft.Azure.Commands.WebApps.Cmdlet.BackupRestore.AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="ae799-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="ae799-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae799-150">OUTPUTS</span></span>

### <span data-ttu-id="ae799-151">System.Void</span><span class="sxs-lookup"><span data-stu-id="ae799-151">System.Void</span></span>

## <span data-ttu-id="ae799-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae799-152">NOTES</span></span>

## <span data-ttu-id="ae799-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae799-153">RELATED LINKS</span></span>
