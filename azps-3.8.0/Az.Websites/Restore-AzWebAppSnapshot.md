---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: 1dd84305753edc8ad639c160c9003c4c393d041e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051865"
---
# <span data-ttu-id="27a7c-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="27a7c-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="27a7c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="27a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="27a7c-103">Przywraca migawkę aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="27a7c-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="27a7c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="27a7c-104">SYNTAX</span></span>

### <span data-ttu-id="27a7c-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="27a7c-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27a7c-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="27a7c-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27a7c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="27a7c-107">DESCRIPTION</span></span>
<span data-ttu-id="27a7c-108">Przywraca migawkę aplikacji sieci Web do aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="27a7c-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="27a7c-109">Przywrócenie migawki spowoduje zastąpienie wszystkich plików w aplikacji sieci Web do plików znajdujących się w migawce.</span><span class="sxs-lookup"><span data-stu-id="27a7c-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="27a7c-110">Aby przywrócić także ustawienia, użyj parametru Switch RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="27a7c-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="27a7c-111">Migawkę z jednej aplikacji sieci Web można przywrócić do dowolnej innej aplikacji sieci Web w ramach tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="27a7c-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="27a7c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="27a7c-112">EXAMPLES</span></span>

### <span data-ttu-id="27a7c-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="27a7c-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="27a7c-114">Pobiera najnowszą migawkę aplikacji sieci Web o nazwie "ContosoApp" z miejscem o nazwie "przemieszczanie" w grupie zasobów "Default-Web-Zachodnia".</span><span class="sxs-lookup"><span data-stu-id="27a7c-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="27a7c-115">Przywraca zdjęcie do gniazda "Przywróć" aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="27a7c-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="27a7c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="27a7c-116">PARAMETERS</span></span>

### <span data-ttu-id="27a7c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27a7c-117">-AsJob</span></span>
<span data-ttu-id="27a7c-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="27a7c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27a7c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a7c-119">-DefaultProfile</span></span>
<span data-ttu-id="27a7c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="27a7c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27a7c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="27a7c-121">-Force</span></span>
<span data-ttu-id="27a7c-122">Umożliwia zastąpienie oryginalnej aplikacji sieci Web bez wyświetlania ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="27a7c-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="27a7c-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="27a7c-123">-InputObject</span></span>
<span data-ttu-id="27a7c-124">Migawka usługi Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="27a7c-124">The Azure Web App snapshot.</span></span>

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

### <span data-ttu-id="27a7c-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="27a7c-125">-Name</span></span>
<span data-ttu-id="27a7c-126">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="27a7c-126">The name of the web app.</span></span>

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

### <span data-ttu-id="27a7c-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="27a7c-127">-RecoverConfiguration</span></span>
<span data-ttu-id="27a7c-128">Odzyskiwanie konfiguracji aplikacji sieci Web oprócz plików.</span><span class="sxs-lookup"><span data-stu-id="27a7c-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="27a7c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a7c-129">-ResourceGroupName</span></span>
<span data-ttu-id="27a7c-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="27a7c-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="27a7c-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="27a7c-131">-Slot</span></span>
<span data-ttu-id="27a7c-132">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="27a7c-132">The name of the web app slot.</span></span>

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

### <span data-ttu-id="27a7c-133">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="27a7c-133">-UseDisasterRecovery</span></span>
<span data-ttu-id="27a7c-134">Umożliwia odzyskanie migawki z jednostki skali, która jest w trybie offline.</span><span class="sxs-lookup"><span data-stu-id="27a7c-134">Use to recover a snapshot from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="27a7c-135">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="27a7c-135">-WebApp</span></span>
<span data-ttu-id="27a7c-136">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="27a7c-136">The web app object</span></span>

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

### <span data-ttu-id="27a7c-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="27a7c-137">-Confirm</span></span>
<span data-ttu-id="27a7c-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27a7c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27a7c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27a7c-139">-WhatIf</span></span>
<span data-ttu-id="27a7c-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27a7c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27a7c-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="27a7c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27a7c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a7c-142">CommonParameters</span></span>
<span data-ttu-id="27a7c-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27a7c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a7c-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27a7c-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a7c-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27a7c-145">INPUTS</span></span>

### <span data-ttu-id="27a7c-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="27a7c-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="27a7c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="27a7c-147">System.String</span></span>

### <span data-ttu-id="27a7c-148">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="27a7c-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="27a7c-149">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="27a7c-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="27a7c-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="27a7c-150">OUTPUTS</span></span>

### <span data-ttu-id="27a7c-151">System. void</span><span class="sxs-lookup"><span data-stu-id="27a7c-151">System.Void</span></span>

## <span data-ttu-id="27a7c-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="27a7c-152">NOTES</span></span>

## <span data-ttu-id="27a7c-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27a7c-153">RELATED LINKS</span></span>
