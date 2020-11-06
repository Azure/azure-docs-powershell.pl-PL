---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 536d0fe0f32231bfd732698c584e02be95d5c20e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543288"
---
# <span data-ttu-id="0da5f-101">Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="0da5f-101">Restore-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="0da5f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0da5f-102">SYNOPSIS</span></span>
<span data-ttu-id="0da5f-103">Przywraca migawkę aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="0da5f-103">Restores a web app snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0da5f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0da5f-104">SYNTAX</span></span>

### <span data-ttu-id="0da5f-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="0da5f-105">FromResourceName</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0da5f-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="0da5f-106">FromWebApp</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0da5f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0da5f-107">DESCRIPTION</span></span>
<span data-ttu-id="0da5f-108">Przywraca migawkę aplikacji sieci Web do aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="0da5f-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="0da5f-109">Przywrócenie migawki spowoduje zastąpienie wszystkich plików w aplikacji sieci Web do plików znajdujących się w migawce.</span><span class="sxs-lookup"><span data-stu-id="0da5f-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="0da5f-110">Aby przywrócić także ustawienia, użyj parametru Switch RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0da5f-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="0da5f-111">Migawkę z jednej aplikacji sieci Web można przywrócić do dowolnej innej aplikacji sieci Web w ramach tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0da5f-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="0da5f-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0da5f-112">EXAMPLES</span></span>

### <span data-ttu-id="0da5f-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0da5f-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="0da5f-114">Pobiera najnowszą migawkę aplikacji sieci Web o nazwie "ContosoApp" z miejscem o nazwie "przemieszczanie" w grupie zasobów "Default-Web-Zachodnia".</span><span class="sxs-lookup"><span data-stu-id="0da5f-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="0da5f-115">Przywraca zdjęcie do gniazda "Przywróć" aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="0da5f-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="0da5f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0da5f-116">PARAMETERS</span></span>

### <span data-ttu-id="0da5f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0da5f-117">-AsJob</span></span>
<span data-ttu-id="0da5f-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0da5f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0da5f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da5f-119">-DefaultProfile</span></span>
<span data-ttu-id="0da5f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0da5f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0da5f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0da5f-121">-Force</span></span>
<span data-ttu-id="0da5f-122">Umożliwia zastąpienie oryginalnej aplikacji sieci Web bez wyświetlania ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="0da5f-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="0da5f-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0da5f-123">-InputObject</span></span>
<span data-ttu-id="0da5f-124">Migawka usługi Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0da5f-124">The Azure Web App snapshot.</span></span>

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

### <span data-ttu-id="0da5f-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0da5f-125">-Name</span></span>
<span data-ttu-id="0da5f-126">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="0da5f-126">The name of the web app.</span></span>

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

### <span data-ttu-id="0da5f-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="0da5f-127">-RecoverConfiguration</span></span>
<span data-ttu-id="0da5f-128">Odzyskiwanie konfiguracji aplikacji sieci Web oprócz plików.</span><span class="sxs-lookup"><span data-stu-id="0da5f-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="0da5f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da5f-129">-ResourceGroupName</span></span>
<span data-ttu-id="0da5f-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0da5f-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="0da5f-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="0da5f-131">-Slot</span></span>
<span data-ttu-id="0da5f-132">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="0da5f-132">The name of the web app slot.</span></span>

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

### <span data-ttu-id="0da5f-133">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="0da5f-133">-WebApp</span></span>
<span data-ttu-id="0da5f-134">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="0da5f-134">The web app object</span></span>

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

### <span data-ttu-id="0da5f-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0da5f-135">-Confirm</span></span>
<span data-ttu-id="0da5f-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0da5f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0da5f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0da5f-137">-WhatIf</span></span>
<span data-ttu-id="0da5f-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0da5f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0da5f-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0da5f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0da5f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da5f-140">CommonParameters</span></span>
<span data-ttu-id="0da5f-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0da5f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da5f-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0da5f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da5f-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0da5f-143">INPUTS</span></span>

### <span data-ttu-id="0da5f-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0da5f-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0da5f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="0da5f-145">System.String</span></span>

### <span data-ttu-id="0da5f-146">Microsoft. Azure. Management. Web. models. site</span><span class="sxs-lookup"><span data-stu-id="0da5f-146">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="0da5f-147">Parametry: aplikacji (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0da5f-147">Parameters: WebApp (ByValue)</span></span>

### <span data-ttu-id="0da5f-148">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="0da5f-148">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>
<span data-ttu-id="0da5f-149">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0da5f-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0da5f-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0da5f-150">OUTPUTS</span></span>

### <span data-ttu-id="0da5f-151">System. void</span><span class="sxs-lookup"><span data-stu-id="0da5f-151">System.Void</span></span>

## <span data-ttu-id="0da5f-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0da5f-152">NOTES</span></span>

## <span data-ttu-id="0da5f-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0da5f-153">RELATED LINKS</span></span>
