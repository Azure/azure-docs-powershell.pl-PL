---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restore-Azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: bd7c967bce709c1951cc7a61c1f8bfab9c78f28a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891841"
---
# <span data-ttu-id="82b16-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="82b16-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="82b16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82b16-102">SYNOPSIS</span></span>
<span data-ttu-id="82b16-103">Przywraca migawkę aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="82b16-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="82b16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82b16-104">SYNTAX</span></span>

### <span data-ttu-id="82b16-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="82b16-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82b16-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="82b16-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82b16-107">Opis</span><span class="sxs-lookup"><span data-stu-id="82b16-107">DESCRIPTION</span></span>
<span data-ttu-id="82b16-108">Przywraca migawkę aplikacji sieci Web do aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="82b16-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="82b16-109">Przywrócenie migawki spowoduje zastąpienie wszystkich plików w aplikacji sieci Web do plików znajdujących się w migawce.</span><span class="sxs-lookup"><span data-stu-id="82b16-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="82b16-110">Aby przywrócić także ustawienia, użyj parametru Switch RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82b16-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="82b16-111">Migawkę z jednej aplikacji sieci Web można przywrócić do dowolnej innej aplikacji sieci Web w ramach tej samej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="82b16-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="82b16-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82b16-112">EXAMPLES</span></span>

### <span data-ttu-id="82b16-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="82b16-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="82b16-114">Pobiera najnowszą migawkę aplikacji sieci Web o nazwie "ContosoApp" z miejscem o nazwie "przemieszczanie" w grupie zasobów "Default-Web-Zachodnia".</span><span class="sxs-lookup"><span data-stu-id="82b16-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="82b16-115">Przywraca zdjęcie do gniazda "Przywróć" aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="82b16-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="82b16-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82b16-116">PARAMETERS</span></span>

### <span data-ttu-id="82b16-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82b16-117">-AsJob</span></span>
<span data-ttu-id="82b16-118">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="82b16-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82b16-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b16-119">-DefaultProfile</span></span>
<span data-ttu-id="82b16-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="82b16-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b16-121">-Force</span><span class="sxs-lookup"><span data-stu-id="82b16-121">-Force</span></span>
<span data-ttu-id="82b16-122">Umożliwia zastąpienie oryginalnej aplikacji sieci Web bez wyświetlania ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="82b16-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b16-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="82b16-123">-InputObject</span></span>
<span data-ttu-id="82b16-124">Migawka usługi Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="82b16-124">The Azure Web App snapshot.</span></span>
```yaml
Type: AzureWebAppSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82b16-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="82b16-125">-Name</span></span>
<span data-ttu-id="82b16-126">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="82b16-126">The name of the web app.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b16-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="82b16-127">-RecoverConfiguration</span></span>
<span data-ttu-id="82b16-128">Odzyskiwanie konfiguracji aplikacji sieci Web oprócz plików.</span><span class="sxs-lookup"><span data-stu-id="82b16-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b16-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82b16-129">-ResourceGroupName</span></span>
<span data-ttu-id="82b16-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="82b16-130">The name of the resource group.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b16-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="82b16-131">-Slot</span></span>
<span data-ttu-id="82b16-132">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="82b16-132">The name of the web app slot.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b16-133">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="82b16-133">-WebApp</span></span>
<span data-ttu-id="82b16-134">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="82b16-134">The web app object</span></span>
```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82b16-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="82b16-135">-Confirm</span></span>
<span data-ttu-id="82b16-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82b16-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82b16-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82b16-137">-WhatIf</span></span>
<span data-ttu-id="82b16-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82b16-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82b16-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="82b16-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82b16-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b16-140">CommonParameters</span></span>
<span data-ttu-id="82b16-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82b16-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b16-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82b16-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b16-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82b16-143">INPUTS</span></span>

### <span data-ttu-id="82b16-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="82b16-144">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="82b16-145">Microsoft. Azure. Management. witryn. Web. models.... w systemie lokacji. String Microsoft. Azure. Commands. webapps. cmdlet</span><span class="sxs-lookup"><span data-stu-id="82b16-145">Microsoft.Azure.Management.WebSites.Models.Site System.String Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot System.DateTime</span></span>

## <span data-ttu-id="82b16-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82b16-146">OUTPUTS</span></span>

### <span data-ttu-id="82b16-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="82b16-147">System.Object</span></span>

## <span data-ttu-id="82b16-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82b16-148">NOTES</span></span>

## <span data-ttu-id="82b16-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82b16-149">RELATED LINKS</span></span>

